---
title: Create a dynamic category
description: Create a container for organizing dynamic attribute groups.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Dynamic Schema, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a dynamic category

Create a container for organizing dynamic attribute groups.

## Before you begin

Role required: admin

## About this task

After defining your dynamic attribute groups, organize the groups into broader categories.

Dynamic categories inherit the group membership of their extended hierarchy. For example, a Televisions category could inherit the Electrical Specs group associated with its parent category, Electronics.

## Procedure

1.  Navigate to **All** &gt; **Dynamic Schema** &gt; **Dynamic Categories**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Label used for displaying the dynamic attribute group.|
    |Name|Internal name for the dynamic category.|
    |Parent|Parent category from which this category extends.|
    |Description|A brief summary of what the category contains.|
    |Extensible|Option to allow other categories to extend this category.|
    |Active|Option to activate the dynamic category.|


## Create a dynamic category for capturing everything about electronics

![A dynamic category for capturing everything about Electronics.](../image/dynamic-parent-category-example.png)

## Create a dynamic category called Televisions that extends from the Electronics dynamic category

![A dynamic category that extends from Electronics for capturing everything about televisions.](../image/dynamic-child-category-example.png)

## What to do next

Add more dynamic categories as needed. For example, you might add dynamic categories for other store departments like Health and Beauty, Automotive, and Sporting Goods.

If you determine that you need another dynamic attribute group for multiple products in a category, you can define the dynamic attributes, add them to a new dynamic attribute group, and then add the dynamic attribute group to a broader dynamic category. The new dynamic attribute group is automatically inherited by any dynamic category that extends from the broader dynamic category.

For example, you might need attributes for capturing Volts, Amps, and Watts in a product record. You can add the attributes to a new group called Electrical Specs, and then add the group to the Electronics category. Because the Televisions category extends from the Electronics category, the Electrical Specs group is automatically inherited by the Televisions category.

**Parent Topic:**[Dynamic Schema](../concept/dynamic-schema.md)

