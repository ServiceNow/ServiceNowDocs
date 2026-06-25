---
title: Enable solution configuration
description: Enable solution configuration for an environment to let admins link multiple blueprints into connected configuration sessions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/enable-solution-configuration.html
release: australia
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 1
keywords: [enable solution configuration, environment setup, admin]
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Enable solution configuration

Enable solution configuration for an environment to let admins link multiple blueprints into connected configuration sessions.

## Before you begin

Solution configuration is an environment-level feature that is off by default. Contact Support with your environment details to request enablement.

Open a ticket by using the [ServiceNow Support portal](https://support.servicenow.com). For step-by-step instructions, see [Create a case on Now Support for CPQ \(Logik.ai\) Customers](https://support.servicenow.com/kb?sys_kb_id=d67d3e71475d7a90f64de825126d4326&id=kb_article_view).

Role required: admin

## About this task

Solution configuration must be enabled in each environment where you want to use it. After Support enables it, admins can create configurable product actions and define field mappings in that environment.

## Procedure

1.  Open a blueprint in the admin.

2.  Navigate to the **Rules** section and add a product action.

    Verify that **Configurable Product Action** is available in the action type selector.

    If **Configurable Product Action** does not appear, confirm with Support that the correct environment was enabled.


## Result

Configurable product actions are available in the admin for the enabled environment. You can now link blueprints to create solution configurations.

## What to do next

After enabling solution configuration:

-   To link your first parent and child blueprints, see [Create a configurable product action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-configurable-product-action.md).
-   To review structural limits before designing a solution, see [Solution configuration limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

**Related topics**  


[Solution configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/solution-configurations.md)

