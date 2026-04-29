---
title: Transaction Manager: Date and time fields
description: Learn about Transaction Manager fields for times and dates.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Transaction Manager: Fields, Transaction Manager, CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Transaction Manager: Date and time fields

Learn about Transaction Manager fields for times and dates.

In CPQ, dates and times are critical for determining how long a contract or subscription lasts, when renewals are due, and how pricing is applied over time.

A new date or date/time field might be introduced to support term calculations or to audit events.

Term calculations calculate contract terms, start and end dates, renewals, and lengths. Blank or null dates can affect term accuracy. System defaults, such as the current date, or error flags can handle missing dates.

Auditing events can track activities such as quotes, payments, and contract signings. Missing dates may indicate incomplete data, and must be flagged for review.

The following examples show how date and time fields appear in the end-user UI.

-   Date-only calendar display: ![Jan calendar screen](../images/cpq-txn-mgr-date-time-date-only.png)
-   Date and time input: ![Select time slot](../images/cpq-txn-mgr-date-time-date-time-input.png)
-   Date only: `YYYY-MM-DD` \(for example, `2024-11-07`\)
-   Date and \(optional\) time: `YYYY-MM-DDTHH:MM:SS` \(for example, `2024-10-22T14:30:00`\)

    Administrators can decide whether to include the time component.


Date-only fields are time-zone agnostic. To avoid time-zone discrepancies, dates and times are stored in Universal Coordinated Time \(UTC\).

## Create a new date and time field

1.  From Admin, click **Transactions**, click **Associated fields**, and then click **+ Create Field**.

    ![Create field](../images/cpq-txn-mgr-date-time-new-step-1.jpg)

2.  In the dialog box, enter the name of the field. Set the type as Date/Time, and click **Save**.

    ![Select type](../images/cpq-txn-mgr-date-time-new-step-2.jpg)

3.  Open the field, set the access based on your use case, and click **Save**.

    ![Default access](../images/cpq-txn-mgr-date-time-new-step-3.jpg)


## Display the new date and time field in the buyside interface

To appear in the end-user UI, the field must be included in the layout for the blueprint. The layout is defined by the JSON input file. Changes to the end-user UI can be made by modifying this file.

[Sample JSON file](https://logikio.atlassian.net/wiki/spaces/CS/pages/1837400082/Txn+Mgr+-+Fields+-+Date+Time)

To add a “Test date doc“ field to layout, follow these steps.

1.  From Admin, click **Transaction**, click **Layouts**, and then click the name of the stage.

    ![Transaction screen](../images/cpq-txn-mgr-date-time-display-step-1.jpeg)

2.  The layout JSON must be edited in two places.
    -   In the `fields` section, add the new date field with type, label and variableName parameters. In the example below, we add “Test date doc” below the existing field “Start date“. When you write the code for the new field, make sure the variable name exactly matches the associated field's variable name.

        **Note:** In this example, we use a field that displays only the date, so the type in the layout JSON is `“type“:”Date”`. To create a field that also displays time, the type should be `“type“:”DateTime”`.

        ![Code](../images/cpq-txn-mgr-date-time-display-step-2.jpg)

    -   In the `“layout”: “tiers”: “columnSets”:` section, define the column order of the new field in the “elements“ section. Make sure that the variable name is exactly the same.

        ![Column](../images/cpq-txn-mgr-date-time-display-step-3.png)

3.  Click **Save**, and then click **Deploy**.
4.  Create a new transaction, and click **Edit transaction**. The new field looks like the following.

    ![Column code](../images/cpq-txn-mgr-date-time-display-step-5.jpg)


## Calculating Dates in Rules

Term calculations can determine the duration of a contract, subscription, or pricing agreement. Sometimes we may need to calculate the data and display the output in another field for auditing purposes. In the following example, we consider the start date and end date available in the buyside UI and calculate the difference between the dates in terms of months and days. We display the value in another field called “Subscription term“.

1.  In CPQ Admin, click **Related Rules**, and then click **New Rule**. Enter the name of the rule and define the conditions. In this example, name the rule “Calculate subscription term date“ and its condition as “Start date.“ “End date“ should not be null.

    ![Calculate subscription screen](../images/cpq-txn-mgr-date-time-calc-step-1.png)

2.  To determine the value of another field, add a determination action and provide a script file in the advanced script section. The following script snippet performs the calculation.

    ```
    // Script calculates the difference between start and end dates in months and days and displays the output in Subscription Term (Months).
    
    var yearsDiff = txn.custom.endDate.getFullYear() - txn.custom.startDate.getFullYear();
    var monthsDiff = txn.custom.endDate.getMonth() - txn.custom.startDate.getMonth();
    var totalMonths = yearsDiff * 12 + monthsDiff;
    
    var startDay = txn.custom.startDate.getDate();
    var endDay = txn.custom.endDate.getDate();
    var daysInMonth = new Date(txn.custom.endDate.getFullYear(), txn.custom.endDate.getMonth() + 1, 0).getDate();
    var dayFraction = (endDay - startDay + 1) / daysInMonth;
    
    totalMonths += dayFraction;
    
    return Math.floor(totalMonths * 1000) / 1000;
    ```

    Enter the script in the script editor, and click **Save**.

    ![term date screen](../images/cpq-txn-mgr-date-time-calc-step-2.png)

3.  Associate the newly created rule to the blueprint. Navigate to **Rule Groupings**, and then to the name of the stage where rule should be applied \(in this case, draftStageRuleGroup\). Click **Associate Rules**, and search for the name of the rule. Drag the rule to the left pane, an click **Done** to deploy.

    ![Term date screen](../images/cpq-txn-mgr-date-time-calc-step-3.png)

4.  Test the functionality in the buyside interface by providing values for the start date and the end date. The subscription term is auto-populated based on the script.

    ![Contract info screen](../images/cpq-txn-mgr-date-time-calc-step-4.png)


## Behavior of date and time fields in scripts

Blank/null dates compare as FALSE unless compared to another blank value.

-   `date123 = ""`: TRUE
-   `date123 != ""`: FALSE

Comparisons `<, <=, >, >=, =, !=` are supported. Comparisons involving blank or null dates always evaluate to FALSE. Default values for date fields are empty \(null\) unless specified.

Aggregate operations:

-   `Max`: find latest date
-   `Min`: find earliest date
-   `Count`: counts non-empty date values

`Sum` and `Avg` are not recommended because they may trigger compile-time errors.

**Related topics**  


[Transaction Manager](transaction-manager.md)

[Transaction Manager: Fields](transaction-manager-fields.md)

[Transaction Manager: Transaction-level system fields](transaction-manager-transaction-header-level-system-fields.md)

[Transaction Manager: Line-level system fields](transaction-manager-line-level-system-fields.md)

