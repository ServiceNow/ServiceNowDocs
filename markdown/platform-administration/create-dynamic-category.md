---
title: Create a dynamic category
description: Create a container for organizing dynamic attributes.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with Dynamic Schema, Dynamic Schema, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Create a dynamic category

Create a container for organizing dynamic attributes.

## Before you begin

Role required: dynamic\_schema\_writer

## About this task

After defining your dynamic attributes, you can organize them into categories.

Dynamic categories inherit the dynamic attributes of their extended hierarchy. For example, a Televisions category could inherit the volts, amps, and watts attributes associated with its parent category, Electronics.

## Procedure

1.  Navigate to **All** &gt; **Dynamic Schema** &gt; **Dynamic Namespaces**.

2.  In the Dynamic Categories related list, select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Namespace|Namespace to which the dynamic category belongs.|
    |Label|Label used for displaying the dynamic category.|
    |Name|Internal name for the dynamic category.|
    |Description|A brief summary of what the category contains.|
    |Parent|Parent category from which this category extends.|
    |Active|Option to activate the dynamic category.|


## Create a dynamic category for capturing everything about electronics

![A dynamic category for capturing everything about Electronics.](../image/dynamic-parent-category-example.png)

## Create a dynamic category called Televisions that extends from the Electronics dynamic category

![A dynamic category that extends from Electronics for capturing everything about televisions.](../image/dynamic-child-category-example.png)

## What to do next

Add more dynamic categories as needed. For example, you might add parent categories for store departments like Health and Beauty, Automotive, and Sporting Goods and child categories for Body Soap, Shampoo, Motor Oil, and Fishing Poles.

If you determine that you need dynamic attributes for multiple products in different dynamic categories, you can define the dynamic attributes in a broader, parent dynamic category. When you add attributes to a parent, they're automatically inherited by a child category.

For example, you might need attributes for capturing Volts, Amps, and Watts in a product record. You can add these attributes to the Electronics category. When you create the Televisions category and select Electronics as the parent category, the Volts, Amps, and Watts attributes are automatically inherited by the Televisions category.

