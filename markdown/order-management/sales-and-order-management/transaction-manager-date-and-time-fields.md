---
title: Transaction Manager: Date and Time Fields
description: Learn about the Transaction Manager fields that capture times and dates with times values.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-10"
reading_time_minutes: 5
breadcrumb: [Transaction Manager: Fields, Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Date and Time Fields

Learn about the Transaction Manager fields that capture times and dates with times values.

A date/time field in transaction manager captures important dates or dates with time value for various purposes. In CPQ, these dates are critical for determining how long a contract or subscription lasts, when renewals are due, and how pricing is applied over time. Examples of how date and date/time fields display to the End user UI:

-   Date Only: `YYYY-MM-DD` \(e.g., `2024-11-07`\)

    ![Jan calendar screen](../images/cpq-txn-mgr-date-time-date-only.png)

-   Date + Optional Time: `YYYY-MM-DDTHH:MM:SS` \(e.g., `2024-10-22T14:30:00`\).

    Administrators can decide whether to include the time component.

    ![Select time slot](../images/cpq-txn-mgr-date-time-date-time-input.png)


Date-only fields are time-zone agnostic. Dates/Times are stored in UTC to avoid time-zone discrepancies.

## Create a new date/time field

1.  Navigate to the **Logik Admin** page → Transactions → Associated fields → Create Field.

    ![Create field](../images/cpq-txn-mgr-date-time-new-step-1.jpg)

2.  In the dialog box, enter the name of the field e.g. “Test date Doc“. Enter the type as Date/Time and click **Save**.

    ![Select type](../images/cpq-txn-mgr-date-time-new-step-2.jpg)

3.  Open the created field and set the access based on your use case and click **Save**.

    ![Default access](../images/cpq-txn-mgr-date-time-new-step-3.jpg)


## Display the new date/time field in the buyside interface

To make sure that the newly created field appears in the User UI, we need to include the field in the layout defined for the blueprint. Currently, the layout is defined by the JSON input file and modifications in the same can add changes to the end user UI.

[Sample JSON file](https://logikio.atlassian.net/wiki/spaces/CS/pages/1837400082/Txn+Mgr+-+Fields+-+Date+Time)

To add the “Test date doc“ field to layout, Follow these steps.

1.  Click Logik Admin → Transaction → Layouts → the name of the stage.

    ![Transaction screen](../images/cpq-txn-mgr-date-time-display-step-1.jpeg)

2.  The layout JSON must be edited in two places.
    -   In the “fields” section, add your new date field with type, label and variableName. In the example below, we add “Test date doc” below the existing field “Start date“. While writing the code for the new field, make sure the variable name exactly matches the associated fields variable name.

        **Note:** In this example, we have used a field that displays only the date. So the type given in layout JSON is “type“:”Date”. If you want to create a field that displays time as well, then the type should be “type“:”DateTime”.

        ![Code](../images/cpq-txn-mgr-date-time-display-step-2.jpg)

    -   In the “layout”: “tiers”: “columnSets”: “elements”: section, define the column order of the new field in the “elements“ section of the same JSON layout to adjust the position of the field in the buyside UI. Ensure the variable name is exactly the same.

        ![Column](../images/cpq-txn-mgr-date-time-display-step-3.png)

3.  When the changes are done, Click **Save**, and then click **Deploy**.
4.  Create a new transaction and click **Edit transaction**. This is how the newly created Date/Time field looks.

    ![Column code](../images/cpq-txn-mgr-date-time-display-step-5.jpg)


## The purpose of Date/Time fields

A new Date field type is introduced to support:

1.  Term Calculations:
    -   Calculates contract terms, start/end dates, renewals, and lengths.
    -   Blank/null dates can impact term accuracy; system defaults \(e.g., current date\) or error flags can handle missing dates.
2.  Auditing Events:
    -   Tracks activities like quotes, payments, or contract signing.
    -   Missing dates can indicate incomplete data and must be flagged for review.

## Calculating Dates in Rules

Term calculations involve determining the duration of a contract, subscription, or pricing agreement. Sometimes we may need to calculate the data and display the output in another field which can be useful for auditing purposes. For example, we shall consider the start date and end date available in the buyside UI and calculate the difference between both the dates in terms of months and days and display the value into another field called “Subscription term“. Here is how we do it.

1.  In &lt;ph keyref="var.cpq-som"/&gt; Admin, click **Related Rules**, and then click **New Rule**. Enter the name of the rule and define the conditions. For the use case, we name the rule “Calculate subscription term date“ and its condition as “Start date.“ “End date“ should not be null. See the following example.

    ![Calculate subscription screen](../images/cpq-txn-mgr-date-time-calc-step-1.png)

2.  Since we need to determine the value of another field, add a determination action and provide the script file that would do the calculation in the advanced script section. The following script snippet performs the calculation.

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

    Enter the script in the script editor; click **Save**.

    ![term date screen](../images/cpq-txn-mgr-date-time-calc-step-2.png)

3.  Associate the newly created rule to the blueprint. Navigate to Rule Groupings → draftStageRuleGroup \(Name of the stage where rule should be applied\) → Associate Rules → Search the name of the rule → Drag to the left pane → Click **Done** → Deploy

    ![Term date screen](../images/cpq-txn-mgr-date-time-calc-step-3.png)

4.  Validate by giving values in start date and end date in the buyside interface. The subscription term will get auto-populated based on the script used.

    ![Contract info screen](../images/cpq-txn-mgr-date-time-calc-step-4.png)


## Behaviors for Date/Time fields in Scripts

-   Blank/Null Dates

    Blank/null dates compare as FALSE unless compared to another blank value.

    `date123 = ""` → TRUE

    `date123 != ""` → FALSE

-   Date Comparisons

    Supported comparisons: `<, <=, >, >=, =, !=`

    Examples show that comparisons involving blank/null dates always evaluate to FALSE.

-   Aggregates
    -   Max/Min: Find latest/earliest date.
    -   Count: Counts non-empty date values.
    -   Sum/Avg: Not recommended, as these may trigger compile-time errors while scripting.

**Note:**

-   Accurate storage of dates \(including time zones\) is critical for revenue recognition and reporting.
-   Default values for Date fields are empty/null unless specified.

**Related topics**  


[Transaction Manager](transaction-manager.md)

[Transaction Manager: Fields](transaction-manager-fields.md)

[Transaction Manager: Transaction-level system fields](transaction-manager-transaction-header-level-system-fields.md)

[Transaction Manager: Line-level system fields](transaction-manager-line-level-system-fields.md)

