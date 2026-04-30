---
title: Components installed with Healthcare Operations Core
description: Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations plugin.
locale: en-US
release: yokohama
product: Care Team Operations
classification: care-team-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Healthcare Operations Core Reference, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Components installed with Healthcare Operations Core

Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations plugin.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).

## Tables installed with Healthcare Operations Core

<table id="table_yny_cml_c2c"><tbody><tr><td>

**Table name**

</td><td>

**Description**

</td></tr><tr><td>

Healthcare Operations Core case \(hco\_case\)

</td><td>

Abstract case type that provides a foundation to extend from when building your own operational request types.

</td></tr></tbody>
</table>## Base roles installed with Healthcare Operations Core

<table id="table_ent_fml_c2c"><tbody><tr><td>

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
-   sn\_csm\_case\_types.service\_definition\_admin
-   sn\_hcls.foundation\_data\_writer
-   view\_changer

</td><td>

Has access to create, view, edit and manage healthcare provider, organization, location, and roles

</td></tr><tr><td>

sn\_hco.care\_team\_member

</td><td>

-   sn\_customerservice.service\_organization\_contributor
-   sn\_hcls.foundation\_data\_viewer

</td><td>

Has access to create and view healthcare cases.

</td></tr><tr><td>

sn\_hco.care\_team\_manager

</td><td>

-   sn\_hco.care\_team\_member
-   sn\_customerservice.svc\_location\_manager\_contributor

</td><td>

Has access to create and view healthcare cases.

 can add members to the care unit.

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
</table>## Plugins installed with Healthcare Operations Core

<table id="table_i4x_rml_c2c"><tbody><tr><td>

**Plugin name**

</td><td>

**Description**

</td></tr><tr><td>

Care Team Portal

 \(com.sn\_cto\_sp \)

</td><td>

Provides a portal experience for Healthcare Operations Core users to create requests for supporting departments, manage teams, and gain visibility into submitted requests.

</td></tr><tr><td>

Healthcare and Life Sciences Service Management Core

 \(sn\_hcls\)

</td><td>

Provides the Healthcare and Life Sciences data model for Healthcare and Life Sciences industry products.

</td></tr></tbody>
</table>## Business rules installed with Healthcare Operations Core

<table id="table_sg3_5ml_c2c"><tbody><tr><td>

**Business rules name**

</td><td>

**Description**

</td></tr><tr><td>

HCLS Org Loc Association duplicate check

</td><td>

Ensures that Healthcare locations are associated with healthcare organizations only once

</td></tr><tr><td>

Set HCLS location from CMN location

</td><td>

Sets the corresponding Healthcare location of selected cmn\_location.

</td></tr></tbody>
</table>