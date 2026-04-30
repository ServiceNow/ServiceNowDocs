---
title: Transaction Manager use case: Calculate the total of line-level prices
description: Transaction Manager can include a determination rule that calculates the sum of line-level net prices so that it can be stored in a header-level field.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-14"
reading_time_minutes: 1
breadcrumb: [Transaction Manager: Use cases, Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager use case: Calculate the total of line-level prices

Transaction Manager can include a determination rule that calculates the sum of line-level net prices so that it can be stored in a header-level field.

In ServiceNow CPQ Transaction Manager, you can use a Determination Rule to calculate the sum of line-level total net prices and store the result in a header-level field. This is particularly useful when multiple fields need to be aggregated from line items to the transaction header.

## Example Rule Configuration

-   Rule Action Type: Determination Rule
-   Trigger Point: After line-level updates \(e.g., when line items are added, removed, or updated\)
-   Scope: Transaction Header

## Steps to create and use the rule

1.  Ensure there is a header-level field.

    Alternatively, you can create a custom field \(for example, txn.custom.totalList\) in the "Associated Field” section where the sum will be stored.

2.  Create a header level rule with the appropriate condition for which the rule will be executed.
3.  Choose action type as determination.
4.  In “Use this value”, set “Advanced” to true, and write an advanced script to calculate the fields.

    For example, calculate the sum aggregate of the “List Price” of every line item. To calculate “Total List Price”, we are using the “sumField” function to calculate all the line-level list prices into a single field.

    ![Transaction Manager Use Case: Calculate the Total of Line-Level Prices](../images/cpq-txn-mgr-use-case-calc-total-1.png)

5.  Save and activate the rule so it applies in real time during the transaction lifecycle.
6.  To test the rule, create a transaction and add line items with varying net prices.

    Verify that the sum of the line-level net prices is correctly calculated and displayed in the header-level field.


## More examples

Here are two more examples of line-level calculations stored in a header-level field.

-   Overall Discount Amount

    Advanced Script:

    `return txn.line.functions.sumField(txn.line.custom.listUnitPrice) - txn.line.functions.sumField(txn.line.pricing.extendedNet);`

    ![Transaction Manager Use Case: Calculate the Total of Line-Level Prices](../images/cpq-txn-mgr-use-case-calc-total-2.png)

-   Total Net

    Advanced Script:

    `return txn.line.functions.sumField(txn.line.pricing.extendedNet);`

    ![Transaction Manager Use Case: Calculate the Total of Line-Level Prices](../images/cpq-txn-mgr-use-case-calc-total-3.png)


**Parent Topic:**[Transaction Manager: Use cases](transaction-manager-use-cases.md)

