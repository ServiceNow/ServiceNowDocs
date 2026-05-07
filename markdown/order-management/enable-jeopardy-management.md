---
title: Configure the Order Jeopardy Enablement Policy
description: Add Jeopardy Management workflows to product and service specifications using the Order Jeopardy Enablement Policy in Workflow Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Jeopardy Management, Order management, Configure, Sales Customer Relationship Management]
---

# Configure the Order Jeopardy Enablement Policy

Add Jeopardy Management workflows to product and service specifications using the Order Jeopardy Enablement Policy in Workflow Studio.

## Before you begin

Role required: admin

## About this task

Use Workflow Studio to define which product, service, or resource specification is jeopardy-enabled.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Order Jeopardy Enablement Policy**.

3.  In the **Specification** column under the **Conditions** section, select a product or service specification to link to Jeopardy Management.

4.  In the **results** column, set the **Jeopardy Enabled** field to **True**.![Order Jeopardy Enablement Policy in Workflow Studio.](../image/jm-enablement-policy.png)

    **Note:** Entries in this decision table are for top-level product or service specifications. In a single order, customers can purchase multiple top-level products or services. However, if any one of the products or services isn’t jeopardy-enabled, the entire order is treated as a non-jeopardy-enabled order.

5.  Select **Save**.

    The product specification workflow is jeopardy-enabled. Jeopardy logic begins when the specification workflow starts.


## What to do next

After configuring Jeopardy Management, see [Monitoring order jeopardy](monitoring-jeopardy-management.md) to review different ways to monitor Jeopardy Management.

