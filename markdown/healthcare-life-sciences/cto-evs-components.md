---
title: Components installed with Care Team Operations for Environmental Services
description: Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations for Environmental Services plugin.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Care Team Operations for Environmental Services, Healthcare Operations, Healthcare and Life Sciences]
---

# Components installed with Care Team Operations for Environmental Services

Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations for Environmental Services plugin.

|Table name|Description|
|----------|-----------|
|Healthcare EVS case \[sn\_cto\_evs\_case\]|Abstract case type that provides a foundation to extend from when building your own operational request types.|

<table id="table_xv4_wl2_1gc"><thead><tr><th>

 

</th><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

sn\_cto\_evs.admin

</td><td>

Admin

</td><td>

Configures organizations and team structure for Care Team Operations for Environmental Services.

</td></tr><tr><td>

sn\_cto\_evs.viewer

</td><td>

Case viewer

</td><td>

Can view EVS cases and all HCLS foundation data.

</td></tr><tr><td>

sn\_cto\_evs.loc\_support\_agent

</td><td>

Environmental Services support agent

</td><td>

Can view/resolve all cases under their assignment group, track cases, and fulfill cases.

</td></tr><tr><td>

sn\_cto\_evs.loc\_contributor

</td><td>

Location contributor role

</td><td>

Can report cases, respond to cases, track cases at the business location, and view cases under their team.**Note:** This role is automatically inherited into the Care Team Member role when the Care Team Operations for Environmental Services plugin is installed.

</td></tr></tbody>
</table>