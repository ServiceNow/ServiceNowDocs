---
title: Review the child entities for the equipment model entity
description: Review the child entities that are associated with the selected equipment model entity. You can review the relationships of the associated entities that are subordinate to a higher-level entity.
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Review and update the equipment model details, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Review the child entities for the equipment model entity

Review the child entities that are associated with the selected equipment model entity. You can review the relationships of the associated entities that are subordinate to a higher-level entity.

## Before you begin

Role required: cmdb\_ot\_isa\_editor, cmdb\_ot\_isa\_admin.

## About this task

You can view equipment model entities for any site, if the cmdb\_ot\_isa\_admin role is assigned to you. However, you can only access those sites that an administrator has granted access to, if the cmdb\_ot\_isa\_editor role is assigned to you. To learn more about granting site access, see [Assign or remove equipment model site access for non-administrators](create-user-criteria-for-equipment-model-entity-site-users.md).

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **Equipment Model Manager**.

2.  In the **Equipment model view for** field, select the site that you want to view the equipment model information for.

    You can search for a site by entering in the site name or its short code.

3.  In the selector pane, expand the equipment model hierarchy, and then select the entity that you want to view.

4.  To create a child entity, select the **Create new entity** button and fill in the details in the Create new entity form.

    To learn more, see [Create an entity for a new equipment model](create-entity-new-equipment-model.md).

5.  To view the child entities for the equipment model entity, select **Child Entities**.

6.  Additionally, in the **Related Lists** section you can assign a value in the **Processing Order** field to prioritize a child entity for a given site.

    **Note:** The **Processing Order** value enables you to sort and prioritize a child entity according to its importance and functionality:

    -   In an equipment model hierarchy, a lower Processing Order value is prioritized. If the value assigned to one or more child entities are the same, the child entities are sorted alphabetically.
    -   In the Equipment Model menu of the Industrial Workspace, the hierarchy of an equipment model entity is based on the Processing Order value assigned to the child entities.
    -   In the OT Risk Management tab, all equipment model entities are in sequence according to the Processing Order value assigned to the child entities.

**Parent Topic:**[Review and update the equipment model details](equipment-model-workspace.md)

