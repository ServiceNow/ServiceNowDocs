---
title: Enable AI Search in product catalog
description: Use the enable\_ai\_search\_in\_catalog property to enable AI Search in the product catalog interface for Sales Customer Relationship Management.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-11-17"
reading_time_minutes: 1
breadcrumb: [AI Search for product catalog, Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Enable AI Search in product catalog

Use the **enable\_ai\_search\_in\_catalog** property to enable AI Search in the product catalog interface for Sales Customer Relationship Management.

## Before you begin

Role required: Role required: sn\_prd\_pm\_product\_catalog\_admin

## About this task

The **enable\_ai\_search\_in\_catalog** system property checks that the Product Offering \[sn\_prd\_pm\_product\_offering\] and the Product Specification \[sn\_prd\_pm\_product\_specification\] tables are indexed for use in AI Search. This property also verifies that the AI Search plugin is installed. If you're upgrading from an earlier release, use this property to enable AI Search.

## Procedure

1.  Navigate to **All** and in the filter enter `sys_properties.list`.

2.  Open the **enable\_ai\_search\_in\_catalog** system property.

3.  Set the property value for enabling AI Search in the **Value** field.

    -   Enter `true` to enable AI Search.
    -   Enter `false` to suppress AI Search if it's currently enabled. If this property is set to `false`, the simple keyword search feature is used in the product catalog interface.
4.  Select **Update**.

    If you enable this property, AI Search features are available in the product catalog interface.


