---
title: Recalculating the order priority
description: Manually update the priority field on customer order, order line items, domain orders, and order task forms.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Calculating the order priority, Configuring order priority and routing, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Recalculating the order priority

Manually update the priority field on customer order, order line items, domain orders, and order task forms.

## Before you begin

Role required: admin

## About this task

When a customer order is updated, all child order line items will be recalculated. If you modify the priority of one or more child order line items, the highest priority level is used to recalculate the customer order priority. You can manually modify the priority value for orders, order line items, domain orders, or order tasks and recalculate the order priority. This option recalculates the priority of the order and order line item by re-evaluating the decision tables and extension point script.

## Procedure

1.  Navigate to **All** &gt; **Customer Order Management** &gt; **Customer Orders**.

2.  Select the order that you want to recalculate.

3.  Update the Priority field in the Customer Order form or for the order line items and select **Re-calculate**.

    The decision tables are re-evaluated with the latest order, customer, and urgency data to recalculate the order priority.


