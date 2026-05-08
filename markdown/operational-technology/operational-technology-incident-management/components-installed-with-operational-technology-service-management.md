---
title: Components installed with Operational Technology Incident Management
description: Several types of components may be installed with activation of the Operational Technology Incident Management \(sn\_ot\_inc\_mgmt\) plugin, including user roles.
locale: en-US
release: australia
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Operational Technology Incident Management, Operational Technology]
---

# Components installed with Operational Technology Incident Management

Several types of components may be installed with activation of the Operational Technology Incident Management \(sn\_ot\_inc\_mgmt\) plugin, including user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

OT Incident Admin \[sn\_ot\_incident\_admin\]

</td><td>

Can create, view, delete and edit OT incident records for any equipment model entities. Can configure **Priority Lookup Rules** and **OT incident system properties**.

</td><td>

-   cmdb\_ot\_isa\_viewer\_all
-   sn\_ot\_incident\_write

</td></tr><tr><td>

OT Incident Reader\[sn\_ot\_incident\_read\]

</td><td>

Can only view OT incident records.

</td><td>

-   cmdb\_ot\_viewer
-   cmdb\_ot\_isa\_viewer

</td></tr><tr><td>

OT Incident Fulfiller\[sn\_ot\_incident\_write\]

</td><td>

Can view, create, and edit OT incident records.

</td><td>

sn\_ot\_incident\_read

</td></tr></tbody>
</table>**Note:** The OT Incident User \[ot\_incident\_user\] role is deprecated. For users assigned this role, you can execute a scheduled job to assign them new Operational Technology Incident Management roles. For more information, see [Assign new roles to your users](../task/assign-operational-technology-incident-management-roles.md#).

## Tables installed

<table id="table_j1b_z3y_fwb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OT Incidents \[sn\_ot\_incident\]

</td><td>

List of OT incidents reported across sites.

</td></tr><tr><td>

OT Incident Tasks

 \[sn\_ot\_incident\_task\]

</td><td>

List of OT incident tasks created under various OT incidents.

</td></tr><tr><td>

OT Incident Priority Rule Lookup \[dl\_ot\_inc\_priority\]

</td><td>

List of rules to calculate the priority of an OT incident.

</td></tr></tbody>
</table>**Parent Topic:**[Operational Technology Incident Management reference](oper-tech-incident-management-reference.md)

