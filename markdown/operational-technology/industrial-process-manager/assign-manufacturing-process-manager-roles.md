---
title: Assign Industrial Process Manager user roles
description: Assign roles to your users so that you can control their access to the features, capabilities, and data in the Industrial Process Manager application.
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Industrial Process Manager, Operational Technology]
---

# Assign Industrial Process Manager user roles

Assign roles to your users so that you can control their access to the features, capabilities, and data in the Industrial Process Manager application.

## Before you begin

Role required: admin

## About this task

Users with the roles that are listed in the following table can use the Industrial Process Manager application.

<table id="table_q55_vpq_4nb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Equipment Model Viewer \[cmdb\_ot\_isa\_viewer\]

</td><td>

Can only view the assigned ISA Equipment Model \[cmdb\_ci\_ot\_isa\_entity\] table records. To learn more, see [Using Industrial Process Manager with the Operational Technology Manager](../concept/using-manufacturing-process-manager.md) and [Managing equipment models](managing-equipment-models-after-data-import.md).

</td></tr><tr><td>

Equipment Model Editor \[cmdb\_ot\_isa\_editor\]

</td><td>

Can view and edit the assigned ISA Equipment Model \[cmdb\_ci\_ot\_isa\_entity\] records.To learn more, see [Using Industrial Process Manager with the Operational Technology Manager](../concept/using-manufacturing-process-manager.md) and [Managing equipment models](managing-equipment-models-after-data-import.md).

</td></tr><tr><td>

Equipment Model Admin \[cmdb\_ot\_isa\_admin\]

</td><td>

Inherit the cmdb\_ot\_isa\_editor role and can also do the following actions: -   Use the Industrial Guided Setup to set up the Industrial Process Manager and the Operational Technology Manager.
-   Edit the Equipment Model Template \[isa\_entity\_template\], \[isa\_entity\_level\], and Equipment Entity type \[isa\_entity\_type\] table records.

 To learn more, see [Industrial Workspace Admin application menu and Guided Setup](manufacturing-app-menu-guided-setup.md).

</td></tr><tr><td>

Equipment Model Downtime Planner \[sn\_isa\_schedule\_admin\]

</td><td>

Can create, modify, and delete equipment entity schedules. Can also associate schedules with equipment entities.

</td></tr><tr><td>

Equipment Model Viewer All \[cmdb\_ot\_isa\_viewer\_all\]

</td><td>

Can view all ISA Equipment Model records \(cmdb\_ci\_ot\_isa\_entity\) and associated Equipment Model Template records \(isa\_entity\_template, isa\_entity\_level, isa\_entity\_type\). Role included with cmdb\_ot\_admin.

</td></tr><tr><td>

Amazing Admin \[sn\_ot\_amazing\_admin\]

</td><td>

Can create, modify and delete OT subnet records \(ot\_subnet\_mapping\) for all the equipment model entity OT subnet system properties.

</td></tr><tr><td>

Amazing Editor \[sn\_ot\_amazing\_write\]

</td><td>

Can create, modify and delete OT subnet records \(ot\_subnet\_mapping\) for all the equipment model entities associated with the user.

</td></tr><tr><td>

Amazing Viewer \[sn\_ot\_amazing\_read\]

</td><td>

Can view OT subnet records \(ot\_subnet\_mapping\) for all the equipment model entities.

</td></tr></tbody>
</table>## Procedure

1.  Assign roles to users and groups by using the ServiceNow AI Platform user administration feature.

    |Task|User administration feature|
    |----|---------------------------|
    |**Assign a role to a user**|See [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).|
    |**Assign a role to a group**|See [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).|


**Parent Topic:**[Configuring the Industrial Process Manager](../concept/configuring-manufacturing-process-mgr.md)

