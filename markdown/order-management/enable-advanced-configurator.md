---
title: Enable the ServiceNow CPQ Configurator
description: Use the sn\_prd\_pm.enable\_advanced\_configuration system property to turn on the ServiceNow CPQ Configurator, an interface for adding customizable products to Sales Customer Relationship Management transactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/enable-advanced-configurator.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Without guided setup, ServiceNow CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Enable the ServiceNow CPQ Configurator

Use the **sn\_prd\_pm.enable\_advanced\_configuration** system property to turn on the ServiceNow CPQ Configurator, an interface for adding customizable products to Sales Customer Relationship Management transactions.

## Before you begin

Role required: admin

## About this task

If you have been using the configurator for Sales Customer Relationship Management, but you want to use the ServiceNow CPQ Configurator instead, set the **sn\_prd\_pm.enable\_advanced\_configuration** property to true. The ServiceNow CPQ Configurator is installed with the ServiceNow CPQ Integration application.

## Procedure

1.  Navigate to **All**, and in the filter, enter `sys_properties.list`.

2.  Open the **sn\_prd\_pm.enable\_advanced\_configuration** system property.

3.  In the **Value** field, enter `true` to turn on the Configurator.

4.  Select **Update**.

    The Configurator is displayed when:

    -   Agents are adding configurable products to opportunities, quotes, orders, sold products, and contracts.
    -   Customers are using the Business Portal for self-service features requiring configurable product selections.
    -   Product catalog admins are generating or updating blueprints for configurable products.

**Related topics**  


[Using the ServiceNow CPQ Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-servicenowcpq.md)

