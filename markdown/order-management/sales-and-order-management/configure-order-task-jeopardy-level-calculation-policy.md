---
title: Configure the Order Task Jeopardy Level Calculation Policy
description: Configure the Order Task Jeopardy Level Calculation Policy using Workflow Studio to set the risk levels for the minimum and maximum Service Level Agreement \(SLA\) percentage completion for order tasks.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Jeopardy Management, Order management, Configure, Sales and Order Management]
---

# Configure the Order Task Jeopardy Level Calculation Policy

Configure the Order Task Jeopardy Level Calculation Policy using Workflow Studio to set the risk levels for the minimum and maximum Service Level Agreement \(SLA\) percentage completion for order tasks.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Order Task Jeopardy Level Calculation Policy**.

    ![The image shows the Task Jeopardy Level Calculation Policy window in Workflow Studio.](../image/jm-order-task-jeopardy-lvl-calc-policy.png)

3.  On the Order Task Jeopardy Level Calculation Policy decision table, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |SLA progression|Set the minimum and maximum percentage for the order task.|
    |Order task request type|Select the order task request type. A request task is part of a jeopardy-enabled workflow.|
    |Order line item account|Select the order line item account. The account is linked with the order and order line item.|
    |Jeopardy level|Assign the jeopardy level to associate with the SLA progression percentage minimum and maximum values.|

4.  Select **Save**.


## What to do next

[Configure the Order Jeopardy Enablement Policy](enable-jeopardy-management.md)

