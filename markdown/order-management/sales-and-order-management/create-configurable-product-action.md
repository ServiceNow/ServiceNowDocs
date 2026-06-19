---
title: Create a configurable product action
description: Create a configurable product action to link a child blueprint to a parent blueprint so that a child configuration is created when the action's condition is met.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/create-configurable-product-action.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 2
keywords: [configurable product action, child blueprint, parent blueprint, admin]
breadcrumb: [Enable solution configuration, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a configurable product action

Create a configurable product action to link a child blueprint to a parent blueprint so that a child configuration is created when the action's condition is met.

## Before you begin

-   Solution configuration is enabled in your environment. For more information, see [Enable solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/enable-solution-configuration.md).
-   The parent blueprint and child blueprint are created and deployed.
-   The configurable product associated with the child blueprint exists and has the correct blueprint assigned to it.

Role required: admin

## About this task

A configurable product action is a type of product action that, when its condition evaluates to true, creates a child configuration using the specified blueprint. Each configurable product action adds one child configuration. To add multiple child configurations from a single rule, add multiple configurable product actions to that rule.

**Important:** Once you mark a product action as configurable, you cannot change it back to a standard product action.

## Procedure

1.  Open the parent blueprint in the admin.

2.  Navigate to the Rules section and open the rule where you want to add the configurable product action.

3.  Add a product action and set the action type to **Configurable Product Action**.

4.  In the **Product ID** field, enter the product ID of the configurable product that the child configuration represents.

5.  In the **Blueprint** field, select the child blueprint to use for the child configuration.

    If you are creating an advanced configurable product action, set the **Product ID** and **Blueprint** fields outside the advanced script.

6.  Set the condition for the action.

    When the condition evaluates to true, the child configuration is created. When it evaluates to false, the child configuration is removed.

7.  Save and deploy the blueprint.


## Result

When the condition is met during a buyer's configuration session, a child configuration using the specified blueprint is added to the solution. The solution navigation sidebar appears in the buyer's session when the first child configuration is added.

## Field descriptions

|Field|Description|
|-----|-----------|
|Product ID|Product identifier of the configurable product to add when the condition is true. The configurable product must have the target blueprint associated with it.|
|Blueprint|Child blueprint used to create the child configuration. The blueprint must be deployed.|
|Condition|Rule condition that triggers creation of the child configuration when it evaluates to true, and removes the configuration when it evaluates to false.|

## What to do next

After creating a configurable product action:

-   To pass field values from the parent blueprint to the child, see [Define field mappings for a solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/define-field-mappings-sol-config.md).
-   To test the action, launch the product in the quoting application and verify that the child configuration is created. See [Launch a solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/launch-solution.md).

**Related information**  


[Field mapping in solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/field-mapping-in-solution-configuration.md)

[Solution configuration limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Add configurable products to a solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/add-configurable-products-solution.md)

