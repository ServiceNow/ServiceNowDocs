---
title: Add a workplace entity type
description: Create an entity type according to your organizational requirement. You can group your workplace entities under this entity type and perform various actions on all entities that belong to this type at a time.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Workplace entity and entity types, Manage, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Add a workplace entity type

Create an entity type according to your organizational requirement. You can group your workplace entities under this entity type and perform various actions on all entities that belong to this type at a time.

## Before you begin

Role required: Workplace manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Administration** &gt; **Workplace Entity Types**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the entity type. For example, Business Unit, Marketing Units, Projects and more.|
    |Entity-mapping column|Workplace entity reference column from the Workplace Entity table where the denormalized workplace entity information is stored.|
    |Order|Order of an entity type based on its level in the hierarchy. The lower the order, the higher the entity type is set in the hierarchical structure. The lowest ordered entity type is set in the highest level in the hierarchy. For example, if you set ABC with order 1000 and XYZ with order 600 then XYZ is placed on top in the hierarchy level and ABC is set to lowest.|
    |Active|Option to activate the entity type.|

4.  Select **Submit**.


## Result

The entity type is created.

## What to do next

[Add workplace entities to an entity type](add-workplace-entities-to-an-entity-type.md)

**Parent Topic:**[Configure Workplace entity and entity types](../concept/workplace-entity.md)

