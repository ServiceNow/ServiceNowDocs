---
title: Create an entity for a new equipment model
description: Create an entity for a new equipment model. You do this task when you want to manually create a new equipment model entity directly in the ServiceNow AI Platform rather than import the equipment model data from an external source.
locale: en-US
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Review and update the equipment model details, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Create an entity for a new equipment model

Create an entity for a new equipment model. You do this task when you want to manually create a new equipment model entity directly in the ServiceNow AI Platform rather than import the equipment model data from an external source.

## Before you begin

Role required: cmdb\_ot\_isa\_editor, cmdb\_ot\_isa\_admin.

## About this task

Users with an assigned cmdb\_ot\_isa\_admin role can view equipment model entities for any site. However, users with an assigned cmdb\_ot\_isa\_editor role can only access those sites that an administrator has granted access to for specific users. To learn more about granting site access, see [Assign or remove equipment model site access for non-administrators](create-user-criteria-for-equipment-model-entity-site-users.md).

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **Equipment Model Manager**.

2.  In the **Equipment model view for** field, select the site that you want to view the equipment model information for.

    You can search for a site by typing in the site name or its short code.

3.  Select **Create new entity**.

4.  In the **Create new entity** window, search for and select the parent entity.

    **Note:** You can search the parent entity by short code or name.

5.  On the form, fill in the fields.

<table id="table_xw1_t4c_3qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Parent

</td><td>

Name of the entity, if any, that is the parent to this entity. The currently selected equipment model appears as the parent entity. To change the parent, search for and select the entity that is a parent to the entity that you are creating.

</td></tr><tr><td>

Entity name

</td><td>

Name of the equipment model entity.

</td></tr><tr><td>

Short Code

</td><td>

Short code that is assigned to this entity.

</td></tr><tr><td>

Entity type

</td><td>

Name of the level type that is assigned to the equipment model template level. For example, Material Assembly or Production Cell for a Work Center level. Search for and select an entity type. To learn more, see [Create equipment model level types](create-equipment-model-template-type.md).

</td></tr></tbody>
</table>6.  Select **Save**.

7.  In the Details form, enter the remaining details for the new equipment model entity.

    To learn more, see [Review and update the equipment model details](equipment-model-workspace.md).


**Parent Topic:**[Review and update the equipment model details](equipment-model-workspace.md)

