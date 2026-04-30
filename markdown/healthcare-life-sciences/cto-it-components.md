---
title: Components installed with Care Team Operations for Healthcare IT
description: Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations plugin.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Care Team Operations for Healthcare IT reference, Care Team Operations for Healthcare IT, Healthcare Operations, Healthcare and Life Sciences]
---

# Components installed with Care Team Operations for Healthcare IT

Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations plugin.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).

## Tables installed with Care Team Operations for Healthcare IT

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

<table id="table_mfg_hgm_c2c"><tbody><tr><td>

**Role**

</td><td>

**Contains**

</td><td>

**Description**

</td></tr><tr><td>

sn\_hco.admin 

</td><td>

-   sn\_csm\_agent
-   sn\_service\_org.writer
-   sn\_bus\_loc.ibl\_writer
-   sn\_hcls.foundation\_data\_writer
-   sn\_csm\_case\_types.service\_definition\_viewer

</td><td>

Has access to create, view, edit and manage healthcare provider, organization, location and roles.

</td></tr><tr><td>

sn\_hco.care\_team\_member 

</td><td>

-   sn\_customerservice.service\_organization\_contributor​
-   sn\_hcls.foundation\_data\_viewer

</td><td>

Has access to create and view healthcare cases.

</td></tr><tr><td>

sn\_hco.care\_team\_manager 

</td><td>

-   sn\_hco.care\_team\_member ​
-   sn\_customerservice.svc\_location\_manager\_contributor

</td><td>

Has access to create, view healthcare cases.

 Has ability to add members to the care unit.

</td></tr><tr><td>

sn\_hco.viewer 

</td><td>

sn\_hcls.foundation\_data\_viewer

</td><td>

Has access to view healthcare cases.

</td></tr><tr><td>

sn\_hco.loc\_support\_agen

</td><td>

sn\_bus\_loc.svc\_location\_support\_agent

</td><td>

Views, tracks, and resolves all cases within their assignment group.

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
</table>## Service definitions installed with Care Team Operations for Healthcare IT

<table id="table_q31_fvs_1fc"><tbody><tr><td>

**Name**

</td><td>

**Description**

</td></tr><tr><td>

Healthcare IT services

</td><td>

Service definition for healthcare IT service care team requests.

</td></tr></tbody>
</table>## Service definition categories installed with Care Team Operations for Healthcare IT

<table id="table_cbd_hvs_1fc"><tbody><tr><td>

**Name**

</td><td>

**ID**

</td><td>

**Table**

</td></tr><tr><td>

EMR service

</td><td>

emr\_service

</td><td>

sn\_cto\_hcit\_case

</td></tr><tr><td>

Other IT service

</td><td>

other\_it\_service

</td><td>

sn\_cto\_hcit\_case

</td></tr></tbody>
</table>## Record producers installed with Care Team Operations for Healthcare IT

<table id="table_fsb_jvs_1fc"><tbody><tr><td>

**Name**

</td><td>

**Description**

</td></tr><tr><td>

Report an EMR issue

</td><td>

Report any issue with your EMR. For example, login issues, data quality issues, attachment related issues, etc.

</td></tr><tr><td>

Request other IT service

</td><td>

Report any care team related IT issue.

</td></tr></tbody>
</table>## Service categories installed with Care Team Operations for Healthcare IT

<table id="table_gp3_kvs_1fc"><tbody><tr><td>

**Title**

</td><td>

**Description**

</td></tr><tr><td>

EMR services

</td><td>

Request EMR specific support or services here.

</td></tr><tr><td>

Other IT services

</td><td>

Report other IT or system related issues here.

</td></tr></tbody>
</table>## Service catalogs installed with Care Team Operations for Healthcare IT

<table id="table_n11_svs_1fc"><tbody><tr><td>

**Title**

</td><td>

**Description**

</td></tr><tr><td>

Healthcare IT

</td><td>

This is a catalog for Care Team Operations for Healthcare IT service.

</td></tr></tbody>
</table>