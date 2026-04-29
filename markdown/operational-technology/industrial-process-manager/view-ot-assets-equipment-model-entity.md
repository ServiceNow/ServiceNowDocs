---
title: Add OT devices that are associated with the selected equipment model entity
description: Use OT devices to review the OT devices that are associated with the selected equipment model entity and its child entities. You can also select and associate other OT devices to the selected equipment model entity.
locale: en-US
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Review and update the equipment model details, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Add OT devices that are associated with the selected equipment model entity

Use OT devices to review the OT devices that are associated with the selected equipment model entity and its child entities. You can also select and associate other OT devices to the selected equipment model entity.

## Before you begin

To associate additional OT devices to the selected equipment model entity, both the Operational Technology Manager and Industrial Process Manager applications must be installed.

Role required: To add OT devices, the logged in user has to have a combination of the following assigned roles:

-   cmdb\_ot\_viewer, cmdb\_ot\_editor or cmdb\_ot\_admin role
-   cmdb\_ot\_isa\_editor or cmdb\_ot\_isa\_admin role

**Note:** To learn more about assigning user roles, see [Assign Industrial Process Manager user roles](../task/assign-manufacturing-process-manager-roles.md).

## About this task

Users with an assigned cmdb\_ot\_isa\_admin role can view equipment model entities for any site. However, users with assigned cmdb\_ot\_isa\_editor or cmdb\_ot\_isa\_viewer roles can only access those sites that an administrator has granted access to for specific users. To learn more about granting site access, see [Assign or remove equipment model site access for non-administrators](../task/create-user-criteria-for-equipment-model-entity-site-users.md).

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **Equipment Model Manager**.

    You can search for a site by typing in the site name or its short code.

2.  In the **Equipment model view for** field, select the site you want to view equipment model information for.

3.  In the selector pane, expand the equipment model hierarchy, and then click the entity that you want to view.

4.  To view the associated OT devices for the equipment model entity and its child entities, click **Mapped OT Devices**.

5.  Review the associated OT devices or the associate additional OT devices to the selected equipment model entity.

<table id="choicetable_nnq_bxc_3qb"><thead><tr><th align="left" id="d89541e151">

Task

</th><th align="left" id="d89541e154">

Description

</th></tr></thead><tbody><tr><td id="d89541e160">

**Review the associated OT devices for the selected equipment model entity**

</td><td>

Proceed to the next step and review the OT devices form.

</td></tr><tr><td id="d89541e169">

**Associate the additional OT devices to the selected equipment model entity**

</td><td>

1.  Click **Add**.
2.  In the OT devices form, select the additional OT devices that you want to associate with the equipment model entity.
3.  Click **Add** to add them to the OT devices form.
4.  To edit the columns on the table, select the List Actions \(![List Actions icon](../../../common/image/List_PersonalizeListIcon.png)\) icon. Select **Edit columns** to choose the columns you want to display. For example, if you want to display the IP address column for the OT devices, select **IP Address** from the Available columns and click **OK**.


</td></tr><tr><td id="d89541e214">

**Remove the OT devices from the selected equipment model entity**

</td><td>

1.  In the Mapped OT Devices list view, select the OT devices that you want to remove.
2.  Click **Remove**.


</td></tr></tbody>
</table>6.  Click **Save**.


**Parent Topic:**[Review and update the equipment model details](../task/equipment-model-workspace.md)

