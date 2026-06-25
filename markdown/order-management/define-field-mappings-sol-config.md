---
title: Define field mappings for a solution configuration
description: Define field mappings on a configurable product action to pass field values from the parent blueprint to the child blueprint when a child configuration is created.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/define-field-mappings-sol-config.html
release: australia
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 2
keywords: [field mapping, source field, target field, configurable product action, admin]
breadcrumb: [Enable solution configuration, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Define field mappings for a solution configuration

Define field mappings on a configurable product action to pass field values from the parent blueprint to the child blueprint when a child configuration is created.

## Before you begin

-   A configurable product action exists on the parent blueprint. For more information, see [Create a configurable product action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-configurable-product-action.md).
-   The source fields \(on the parent blueprint\) and the target fields \(on the child blueprint\) exist and are of the same field type.

Role required: admin

## About this task

Field mappings are defined as part of a configurable product action. Each mapping specifies a source field on the parent blueprint and a target field on the child blueprint. The value of the source field is passed to the target field when the child configuration is created, and again whenever the source field value changes during a session.

Target fields become read-only in the child configuration — the buyer can't change a mapped value directly. To continue mapping across multiple levels in a solution hierarchy, define the relevant mappings on each blueprint in the chain independently.

## Procedure

1.  Open the parent blueprint in the admin.

2.  Navigate to the configurable product action where you want to add field mappings.

3.  In the **Field Mapping** section of the configurable product action, select **Add Mapping**.

4.  In the **Source Field** column, select the field on the parent blueprint whose value you want to pass.

5.  In the **Target Field** column, select the field on the child blueprint that receives the value.

    The field type must match the source field type. For supported types, see [Field mapping supported field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

6.  Repeat steps 3–5 for each additional field you want to map.

7.  Save and deploy the blueprint.


## Result

Field values from the source fields on the parent blueprint are passed to the target fields on the child blueprint when a child configuration is created, and again when source field values change during a session.

## Field descriptions

|Field|Description|
|-----|-----------|
|Source field|Field on the parent blueprint whose value is passed to the child configuration. Supported types: Number, Text, Boolean, Picklist. System fields can be source fields.|
|Target field|Field on the child blueprint that receives the value from the source field. Must be the same type as the source field. Becomes read-only in the child configuration. System fields cannot be target fields.|

## What to do next

After defining field mappings:

-   To test mapping behavior, launch the parent product in the quoting application and verify that the target fields receive the expected values in the child configuration. See [Launch a solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/launch-solution.md).
-   To verify field type compatibility, see [Field mapping supported field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

**Related topics**  


[Create a configurable product action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-configurable-product-action.md)

[Field mapping supported field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

