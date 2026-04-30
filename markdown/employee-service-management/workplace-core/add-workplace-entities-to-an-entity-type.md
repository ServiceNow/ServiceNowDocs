---
title: Add workplace entities to an entity type
description: Create workplace entities based on your organization's business structure. Specify the entity type to which they belong. You can also specify a parent to the entity based on its hierarchy.
locale: en-US
release: xanadu
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Workplace entity and entity types, Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Add workplace entities to an entity type

Create workplace entities based on your organization's business structure. Specify the entity type to which they belong. You can also specify a parent to the entity based on its hierarchy.

## Before you begin

[Add a workplace entity type](add-a-workplace-entity-type.md)

Role required: Workplace manager

## About this task

Create and associate a workplace entity with an entity type so that it can be easily classified. Assign the entity to a parent.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Administration** &gt; **Workplace Entities**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the workplace entity.|
    |Parent|Parent of the workplace entity.|
    |Entity type|Entity type to which the workplace entity belongs.|
    |Active|Option to activate the workplace entity.|
    |Managed by group|Group that manages the workplace entity. Users of the selected group receive a notification when an allocation for the entity is going to expire.|
    |Managed by|User that manages the workplace entity. The selected user receives a notification when an allocation for the entity is going to expire.|

4.  Select **Submit**.


## Result

The workplace entity is created and assigned to the selected parent and entity type.

## What to do next

For more information about how workplace entities and other allocations work, refer to [Allocation - types, setting, and impact](../../workplace-space-management/reference/setting-an-allocation-and-its-impact.md).

To populate the Entity-mapping column for existing workplace entities, the application provides you with the following flows:

-   **Set hierarchy from scratch via subflow**: Run this flow to recalculate the entity-mapping columns for the complete hierarchy.
-   **Process entity updates via subflow**: This flow runs everyday to update the workplace entity-mapping columns only for those workplace entities where the 'update\_type' column is set.

**Parent Topic:**[Configure Workplace entity and entity types](../concept/workplace-entity.md)

