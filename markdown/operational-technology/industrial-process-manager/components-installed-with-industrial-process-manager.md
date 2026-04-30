---
title: Components installed with Industrial Process Manager
description: Several types of components may be installed with activation of the Industrial Process Manager application, including user roles.
locale: en-US
release: xanadu
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Reference, Industrial Process Manager, Operational Technology]
---

# Components installed with Industrial Process Manager

Several types of components may be installed with activation of the Industrial Process Manager application, including user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Roles installed

<table id="table_q55_vpq_4nb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Equipment Model Viewer \[cmdb\_ot\_isa\_viewer\]

</td><td>

Can only view the assigned ISA Equipment Model \[cmdb\_ci\_ot\_isa\_entity\] table records. To learn more, see [Using Industrial Process Manager with the Operational Technology Manager](../concept/using-manufacturing-process-manager.md) and [Managing equipment models](../task/managing-equipment-models-after-data-import.md).

</td></tr><tr><td>

Equipment Model Editor \[cmdb\_ot\_isa\_editor\]

</td><td>

Can view and edit the assigned ISA Equipment Model \[cmdb\_ci\_ot\_isa\_entity\] records.To learn more, see [Using Industrial Process Manager with the Operational Technology Manager](../concept/using-manufacturing-process-manager.md) and [Managing equipment models](../task/managing-equipment-models-after-data-import.md).

</td></tr><tr><td>

Equipment Model Admin \[cmdb\_ot\_isa\_admin\]

</td><td>

Inherit the cmdb\_ot\_isa\_editor role and can also do the following actions: -   Use the Industrial Guided Setup to set up the Industrial Process Manager and the Operational Technology Manager.
-   Edit the Equipment Model Template \[isa\_entity\_template\], \[isa\_entity\_level\], and Equipment Entity type \[isa\_entity\_type\] table records.

 To learn more, see [Industrial Workspace Admin application menu and Guided Setup](../task/manufacturing-app-menu-guided-setup.md).

</td></tr><tr><td>

ISA Site Viewer \[cmdb\_ot\_isa\_bypass\_qbr\]

</td><td>

Can view all sites in the OT Progress Scorecard.

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
</table>**Parent Topic:**[Industrial Process Manager reference](manufacturing-process-mgr-reference.md)

