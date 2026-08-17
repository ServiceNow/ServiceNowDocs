---
title: Create an order from a quote line item
description: You can create an order from all quote line items, or from a subset of top-level line items that you select.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-management-create-order-quote-line.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Quote Management, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Create an order from a quote line item

You can create an order from all quote line items, or from a subset of top-level line items that you select.

## Before you begin

Role required: sales\_agent

You can create an order for a quote that is in the completed state. The **Create Order** button must be available on the quote layout. If you don't see the button, contact your administrator.

## About this task

When you create an order from a quote, the quote line items, along with other relevant fields, are populated on the order as order lines. You can create an order from the entire quote or from selected line items:

-   To create an order from the entire quote, don't select any line items before you select **Create Order**. All quote line items are converted to order lines.
-   To create an order from a subset of the quote, select one or more top-level \(root\) line items before you select **Create Order**. Only the selected top-level lines, along with all of their child lines, are converted to order lines.

**Note:** You can select only top-level line items. Child lines are included automatically with their selected parent line.

## Procedure

1.  In the CSM Configurable Workspace, select **List** \[Omitted image "list-outline-24.svg"\] Alt text: view and select **Quotes** &gt; **All**

2.  Select the quote, which must be in the Completed state, and select the Line items tab.

3.  Open the quote that you want to create an order from.

4.  Do one of the following:

    -   To include all line items in the order, don't select any line items.
    -   To include only specific line items, select one or more top-level line items. The **Create Order** button label updates to show the number of line items that you selected.
5.  Select **Create Order**.

    An order is created from the quote. Orders associated with the quote appear in the **Related Lists: Orders** section of the Contextual Side Panel \(CSP\).


**Parent Topic:**[Using Quote Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-mgmt-using.md)

