---
title: Transaction Manager use case: Calculate prices for line-level fields
description: Transaction Manager can apply rules to line-level fields that dynamically calculate prices according to changes to the field, such as when products are added or removed.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Transaction Manager: Use cases, Transaction Manager, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager use case: Calculate prices for line-level fields

Transaction Manager can apply rules to line-level fields that dynamically calculate prices according to changes to the field, such as when products are added or removed.

In the Transaction Manager, we can apply rules on line-level fields to cover various price calculations relevant to selected products. These calculations adapt dynamically to changes, such as the addition or removal of products. This article outlines a use case involving three types of price calculations and the steps required to configure them.

The use case involves three types of price calculations:

-   Annual List Price: This is the list price multiplied by the number of months chosen in the subscription period.
-   Unit Net: The price of a product after the discount amount has been deducted.
-   Extended Net: The unit net of the product multiplied by the quantity of the product.

## Step 1: Create Custom Fields

-   Navigate to CPQ Admin &gt; Transaction &gt; Associated Fields.
-   Create all the custom fields required for your use case. For the detailed steps on how to create fields, see [Transaction Manager: Fields](transaction-manager-fields.md).

In this example, we intend to use the following fields:

-   **Start Date**

    Custom header \(dateTime type\) field that stores the subscription start date.

-   **End Date**

    Custom header field \(dateTime type\) that stores the subscription end date.

-   **Subscription Term \(Months\)**

    Custom header \(Number type\) field that calculates the difference between the start date and end date, displaying the subscription term. For the detailed steps on how to do DateTime field calculations, see [Transaction Manager: Date and time fields](transaction-manager-date-and-time-fields.md).

-   **Target Line Item Discount**

    Custom header \(Number type\) field where users select the discount rate.

-   **Quantity**

    Line-level system field specifying the quantity of the product chosen.

-   **List Price**

    Line-level system field specifying the product’s price.

-   **Discount Percent**

    Line-level system field storing the discount rate. This field is automatically populated with the value selected in the Target Line Item Discount field using a rule.

-   **Annual List Price**

    Custom field used to store results of price calculations for annual list price. This is a transaction line level custom field \(Number Type\)

-   **Unit Net**

    System field labeled as “Net Price” in the system but renamed “Unit Net” by layout definition. This field stores results of price calculations.

-   **Extended Net**

    System field that stores the total unit net price for the product in the line entry.


![Steps to Configure Line-Level Price Calculations](../images/cpq-txn-mgr-use-case-calc-prices-custom-fields.jpeg)

## Step 2: Add fields to layout

Map the configured fields into the appropriate layout for visibility. For the detailed steps, see [Transaction Manager: Layouts](transaction-manager-layouts.md).

## Step 3: Create the rules

Three rules are to be created:

-   Calculate Annual List Price
-   Calculate Unit Net Price
-   Calculate Extended Net Price

Follow these steps:

1.  In **Related Rules**, click **New Rule**.
2.  Enter the name of the rule and select **Transaction Line** as the rule type.
3.  Click **Save**.

![Steps to Configure Line-Level Price Calculations](../images/cpq-txn-mgr-use-case-calc-prices-new-rule.jpeg)

## Step 4: Create and configure rule actions

1.  Select **Determination** as the action type for the rule.
2.  Define the rule’s conditions and action items.
3.  Add the advanced script to perform the calculation for Use Case 1 \(Annual List Price\). Refer to the snapshot below.

    ![Steps to Configure Line-Level Price Calculations](../images/cpq-txn-mgr-use-case-calc-prices-case-1.jpeg)

4.  Click **Save**.
5.  Repeat steps 1 through 4 to configure rules for Use Case 2 \(Unit Net\) and Use Case 3 \(Extended Net\). Refer to the snapshots below.

Use Case 2 \(Unit Net\) - Edit Net pricing calculation:

![Use Case 2 (Unit Net): Edit Net pricing calc](../images/cpq-txn-mgr-use-case-calc-prices-case-2.jpeg)

Use Case 3 \(Extended Net\) - Edit Calculate annual extended net price:

![Use Case 3 (Extended Net): Edit Calculate annual extended net price](../images/cpq-txn-mgr-use-case-calc-prices-case-3.jpeg)

## Step 5: Associate rules to rule groupings

1.  On the Admin page, click **Rule Groupings**, and then click **Add Rule Grouping**. Enter the variable name as the stage in which rule should run \(Draftstage\), and then click **Save**.

    ![Edit Calculate annual extended net price](../images/cpq-txn-mgr-use-case-calc-prices-new-rule-grouping.png)

2.  Associate the newly created rules:

    1.  Click **Associate**.
    2.  Select the name of the rule you created.
    3.  Click **Done**.
    ![Edit Calculate annual extended net price](../images/cpq-txn-mgr-use-case-calc-prices-associate-rule.png)

3.  To link the newly created rule grouping with the stage \(Draft in the sample use case\) where your rules should run, click **Stages** on the transaction page. Click **Draft**, and then click **Rule groupings**. Search the new rule grouping, select, and then click **Save**.

    ![Edit Calculate annual extended net price](../images/cpq-txn-mgr-use-case-calc-prices-draft.png)


## Step 6: Deploy and test

Deploy the configured blueprint to make the rules active, and then test the implementation in the UI to confirm the scripts are working as expected.

Below is an example of the final implementation:

-   Use Case 1: Entering the start date and end date header fields auto-populates Annual list price \(List Price \* Subscription Term i.e. $2,500.00 \* 4 Months 11 Days = $10,885.00\)
-   Use Case 2: Setting the target line item discount as 5 %, auto-populates the unit net price \[List price - Discount/100 \* List price i.e. $2,500.00 - \(0.05 \* $2,500.00\) = $2,375.00\]
-   Use Case 3: Setting the quantity of each entry auto-changes the Extended Net price \(Unit net price \* Quantity i.e. $2,375.00 \* 10 = $23,750.00\)

[Final output](https://api.media.atlassian.com/file/0b8f679f-9b7c-4588-945d-7175d097d500/artifact/video_1280.mp4/binary/cdn?client=71a95134-cb5f-4d3c-a7e7-bf5197602cec&collection=contentId-1923481616&max-age=2592000&token=eyJhbGciOiJIUzI1NiJ9.eyJpc3MiOiI3MWE5NTEzNC1jYjVmLTRkM2MtYTdlNy1iZjUxOTc2MDJjZWMiLCJhY2Nlc3MiOnsidXJuOmZpbGVzdG9yZTpjb2xsZWN0aW9uOmNvbnRlbnRJZC0xOTIzNDgxNjE2IjpbInJlYWQiXX0sImV4cCI6MTc2MzQwMjI3MiwibmJmIjoxNzYzMzk5MzkyLCJhYUlkIjoiNzEyMDIwOmE3MmMwNDYwLWM0OWEtNDAyZS1iNWJjLWE5NWIxZjk4ZjMxNCJ9.j9CHqPDPWPN-towOqICAF484FBEZOzgkFg9upnWT7js)

**Parent Topic:**[Transaction Manager: Use cases](transaction-manager-use-cases.md)

