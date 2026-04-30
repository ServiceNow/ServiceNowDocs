---
title: Components installed with Care Team Operations for Healthcare IT
description: Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations plugin.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Care Team Operations for Healthcare IT, Healthcare Operations, Healthcare and Life Sciences]
---

# Components installed with Care Team Operations for Healthcare IT

Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations plugin.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).

## Tables installed with Care Team Operations for Healthcare IT

**Tables installed with Care Team Operations for Healthcare IT**

<table id="table_rqh_dgm_c2c"><tbody><tr><td>

**Table name**

</td><td>

**Description**

</td></tr><tr><td>

Care Team Operations for Healthcare IT case \(sn\_cto\_hcit\_case\)

</td><td>

Abstract case type that provides a foundation to extend from when building your own operational request types.

</td></tr></tbody>
</table>## Base roles installed with Care Team Operations for Healthcare IT

<table id="id_bwq_gqw_ngc"><tbody><tr><td>

sn\_cto\_hcit.admin

</td><td>

IT Admin

</td><td>

IT Admin role for Care Team Operations for Healthcare IT.

</td></tr><tr><td>

sn\_cto\_hcit.loc\_support\_agent

</td><td>

IT Support Agent

</td><td>

Views/resolves all cases under their assignment group. Tracks and fulfills cases.

</td></tr><tr><td>

sn\_cto\_hcit.viewer

</td><td>

IT Viewer

</td><td>

Views all IT and HCLS foundation data.

 **Note:**If users need access to incidents, the sn\_incident\_read role can be added to this role.

</td></tr><tr><td>

sn\_cto\_hcit.loc\_contributor

</td><td>

CTO IT location contributor role

</td><td>

Reports cases, respond to cases, track cases at business location, views cases under their team.**Note:** This role is automatically inherited into the Care Team Member role when the Care Team Operations for Healthcare IT plugin is installed.

</td></tr></tbody>
</table>## Plugins installed with Care Team Operations for Healthcare IT

<table id="table_rdz_tgm_c2c"><tbody><tr><td>

**Plugin name**

</td><td>

**Description**

</td></tr><tr><td>

Care Team Portal

 \(com.sn\_cto\_sp​\)

</td><td>

Provides a portal experience for Care Team Operations for Healthcare IT users to create requests for supporting departments, manage teams, and gain visibility into submitted requests.

</td></tr><tr><td>

Healthcare Operations Core

 \[com.sn\_hco\]

</td><td>

Healthcare Operations Core provides clinicians an uniform interface to report and track issues related to their day-to-day operations. This helps hospitals eliminate inefficient manual processes, reduce patient safety risks and increase patient satisfaction through timely resolution of issues and completion of important tasks.

</td></tr></tbody>
</table>