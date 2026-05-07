---
title: Enable the CPQ Configurator
description: Use the sn\_prd\_pm.enable\_advanced\_configuration system property to turn on the CPQ Configurator, an interface for adding customizable products to Sales Customer Relationship Management transactions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Enable the CPQ Configurator

Use the **sn\_prd\_pm.enable\_advanced\_configuration** system property to turn on the CPQ Configurator, an interface for adding customizable products to Sales Customer Relationship Management transactions.

## Before you begin

Role required: admin

## About this task

If you have been using the legacy product configurator for Sales Customer Relationship Management, but you want to use the CPQ Configurator instead, set the **sn\_prd\_pm.enable\_advanced\_configuration** property to true. The CPQ Configurator is installed with the CPQ Integration application.

## Procedure

1.  Navigate to **All**, and in the filter, enter `sys_properties.list`.

2.  Open the **sn\_prd\_pm.enable\_advanced\_configuration** system property.

3.  In the **Value** field, enter `true` to turn on the CPQ Configurator.

4.  Select **Update**.

    The CPQ Configurator is displayed when:

    -   Agents are adding configurable products to opportunities, quotes, orders, sold products, and contracts.
    -   Customers are using the Business Portal for self-service features requiring configurable product selections.
    -   Product catalog admins are generating or updating blueprints for configurable products.

**Related topics**  


[Using the CPQ Configurator](../concept/using-servicenowcpq.md)

