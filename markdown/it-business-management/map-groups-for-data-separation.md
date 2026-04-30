---
title: Map a user group for Data Separation
description: Map a user group for Data Separation to restrict data only to the specified users of a group and sub-groups.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Data Separation, Strategic Portfolio Management]
---

# Map a user group for Data Separation

Map a user group for Data Separation to restrict data only to the specified users of a group and sub-groups.

## Before you begin

Role required: sn\_ds.ds\_admin

## About this task

You can create only one entity-group mapping per lens entity record.

For example, the following image shows that the leaf node is a Department and that IT is one of the departments. You want to restrict the data of the IT department to a specific group. Then, create an entity-group mapping for the IT department with the required user group.

![Entity-group mapping example.](../image/entity-group-mapping-example.png)

If you want to grant access to the data of the IT department for more than one group, create a parent user group and add all the other groups as sub-groups under the parent group. Then you can map the parent group in the entity-group mapping record of the IT department.

**Note:** If you want to grant access to the data of all departments for a user group, create an entity-group mapping with the parent entity of the department entity. Alternatively, you can also create one entity-group mapping per department for the user group.

## Procedure

1.  Navigate to **All** &gt; **Data Separation** &gt; **Entity-Group Mappings**.

2.  Select **New**.

3.  On the Enity-Group Mapping form, fill in the fields.

    For a description of the field values, see [Entity Group Mapping form](../reference/entity-group-mapping-form.md).

4.  Select **Submit** to save the record.

5.  Navigate to **All** &gt; **Data Separation** &gt; **Entity-Group Mappings**.

6.  From the Entity-Group Mappings list view, select **Sync data separation** to synchronize the entity-group mappings for Data Separation.


## Result

The data is restricted to the user group populated in the entity-group mapping record for the enabled entities.

**Parent Topic:**[Configuring Data Separation](../concept/configuring-data-separation.md)

