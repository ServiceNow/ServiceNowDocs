---
title: Components installed with Care Team Operations for Biomed
description: Several types of components such as tables, user roles, and business rules are installed when you install the Care Team Operations for Biomed plugin.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Care Team Operations for Biomed Reference, Care Team Operations for Biomed, Healthcare Operations, Healthcare and Life Sciences]
---

# Components installed with Care Team Operations for Biomed

Several types of components such as tables, user roles, and business rules are installed when you install the Care Team Operations for Biomed plugin.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).

## Tables installed with Care Team Operations for Biomed

<table id="table_i4d_1qm_c2c"><tbody><tr><td>

**Table name**

</td><td>

**Description**

</td></tr><tr><td>

Care Team Operations for Biomed case \(sn\_cto\_biomed\_case\)

</td><td>

Abstract case type that provides a foundation to extend from when building your own operational request types.

</td></tr></tbody>
</table>## Roles installed with Care Team Operations for Biomed

**Roles installed with Care Team Operations for Biomed**

<table id="table_w2z_bqm_c2c"><tbody><tr><td>

sn\_cto\_biomed.admin​

</td><td>

Biomed Admin

</td><td>

Biomed Admin role for Care team operation.

</td></tr><tr><td>

sn\_cto\_biomed.loc\_support\_agent​

</td><td>

Biomed Support Agent

</td><td>

Can view/resolve all cases under their assignment group, tracks, and fulfill cases.

</td></tr><tr><td>

sn\_cto\_biomed.viewer​

</td><td>

Biomed Viewer

</td><td>

Can view Biomed and HCLS foundation data.

</td></tr><tr><td>

sn\_cto\_biomed. loc\_contributor​

</td><td>

​CTO Biomed location contributor role for Nurse, Nurse Assistant

</td><td>

Report cases, respond to cases,​ track cases at business location, ran view cases under their team.

</td></tr></tbody>
</table>## Plugins installed with Care Team Operations for Biomed

<table id="table_rdz_tgm_c2c"><tbody><tr><td>

**Plugin name**

</td><td>

**Description**

</td></tr><tr><td>

Care Team Portal

 \(com.sn\_cto\_sp​\)

</td><td>

Provides a portal experience for Care Team Operations for Biomed users to create requests for supporting departments, manage teams, and gain visibility into submitted requests.

</td></tr><tr><td>

Healthcare Operations Core

 \[com.sn\_hco\]

</td><td>

Healthcare Operations Core provides clinicians a uniform interface to report and track issues related to their day-to-day operations. This plugin helps hospitals eliminate inefficient manual processes, reduce patient safety risks, and increase patient satisfaction through timely resolution of issues and completion of important tasks.

</td></tr></tbody>
</table>## Service definitions installed with Care Team Operations for Biomed

<table id="table_q31_fvs_1fc"><tbody><tr><td>

**Name**

</td><td>

**Description**

</td></tr><tr><td>

Biomed services

</td><td>

Service definition for Biomed service care team requests.

</td></tr></tbody>
</table>## Service definition categories installed with Care Team Operations for Biomed

<table id="table_cbd_hvs_1fc"><tbody><tr><td>

**Name**

</td><td>

**ID**

</td><td>

**Table**

</td></tr><tr><td>

Medical device issue

</td><td>

medical\_device\_issue

</td><td>

sn\_cto\_biomed\_case

</td></tr><tr><td>

Other biomed issue

</td><td>

other\_biomed\_issue

</td><td>

sn\_cto\_biomed\_case

</td></tr></tbody>
</table>## Record producers installed with Care Team Operations for Biomed

<table id="table_fsb_jvs_1fc"><tbody><tr><td>

**Name**

</td><td>

**Description**

</td></tr><tr><td>

Report a medical device issue

</td><td>

Report any issue with a medical device. For example, device malfunctioning, device not starting, etc.

</td></tr><tr><td>

Request other biomed service

</td><td>

Report any non-medical device biomed issue.

</td></tr></tbody>
</table>## Service categories installed with Care Team Operations for Biomed

<table id="table_gp3_kvs_1fc"><tbody><tr><td>

**Title**

</td><td>

**Description**

</td></tr><tr><td>

Medical device services

</td><td>

Create a request for any medical device related issues.

</td></tr><tr><td>

Other biomed services

</td><td>

Report an issue or request support for any non-medical device biomed concerns.

</td></tr></tbody>
</table>## Service catalogs installed with Care Team Operations for Biomed

<table id="table_n11_svs_1fc"><tbody><tr><td>

**Title**

</td><td>

**Description**

</td></tr><tr><td>

Biomed

</td><td>

This is a catalog for Care Team Operations for Biomed services.

</td></tr></tbody>
</table>