---
title: Configure the Order Line Jeopardy Level Calculation Policy
description: Configure the Order Line Jeopardy Level Calculation Policy using Workflow Studio to set the jeopardy risk level for order line items.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Jeopardy Management, Order management, Configure, Sales and Order Management]
---

# Configure the Order Line Jeopardy Level Calculation Policy

Configure the Order Line Jeopardy Level Calculation Policy using Workflow Studio to set the jeopardy risk level for order line items.

## Before you begin

Role required: admin

## About this task

You must provide a time range for each jeopardy level. When the time range is reached, the linked jeopardy alert level is displayed.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Order Line Item Jeopardy Level Calculation Policy**.

    ![The image shows the Order Line Item Jeopardy Level Calculation policy window in Workflow Studio.](../image/jm-order-line-item-jeopardy-level-calc.png)

3.  On the Order Line Item Jeopardy Level Calculation Policy decision table, fill in the fields.

<table id="table_wfc_vbj_1yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Delayed Percentage

</td><td>

Set the minimum and maximum delayed percentage for the order line item \(OLI\).

</td></tr><tr><td>

Order Line Items \(OLI\) Specification

</td><td>

Select the order line item to attach to the **Delayed Percentage**.

</td></tr><tr><td>

Jeopardy Level

</td><td>

Set the jeopardy level for the values indicated in the **Delayed Percentage** field. In the example:-   Less than 10% delayed percentage = the lowest jeopardy level.
-   10–25% completion, Jeopardy level moves to a medium alert.
For example, if the minimum and maximum values in the **Delayed Percentage** field are 5% and 10% respectively, you can assign that value range a Low Jeopardy Level.

</td></tr></tbody>
</table>4.  Select **Save**.


## What to do next

[Configure the Order Task Jeopardy Level Calculation Policy](configure-order-task-jeopardy-level-calculation-policy.md)

