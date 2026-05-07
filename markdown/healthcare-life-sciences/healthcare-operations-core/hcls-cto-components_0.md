---
title: Components installed with Healthcare Operations Core
description: Several types of components such as tables, user roles, and business rules are installed when you activate the Care Team Operations plugin.
locale: en-US
release: australia
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
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

Admin

sn\_hco.admin

</td><td>

-   sn\_csm\_agent
-   sn\_service\_org.writer
-   sn\_bus\_loc.ibl\_writer
-   sn\_csm\_case\_types.service\_definition\_admin
-   sn\_hcls.foundation\_data\_writer

</td><td>

This is the administrator role for Healthcare Operations Core.

</td></tr><tr><td>

Team Member

sn\_hco.care\_team\_member

</td><td>

-   sn\_customerservice.service\_organization\_contributor
-   sn\_hcls.foundation\_data\_viewer

</td><td>

This role has access to create and view HCO cases and can add members to the care unit.

</td></tr><tr><td>

Team Manager

sn\_hco.care\_team\_manager

</td><td>

-   sn\_hco.care\_team\_member
-   sn\_customerservice.svc\_location\_manager\_contributor

</td><td>

This role can view HCO cases and HCLS foundation data.

</td></tr><tr><td>

Viewer

sn\_hco.viewer

</td><td>

sn\_hcls.foundation\_data\_viewer

</td><td>

This role can view HCO cases and HCLS foundation data.

</td></tr><tr><td>

Support Agent

sn\_hco.loc\_support\_agent

</td><td>

sn\_bus\_loc.svc\_location\_support\_agent

</td><td>

This role can view, track, resolve, and fulfill all cases under their assignment group.

</td></tr><tr><td>

sn\_hco.loc\_manager

</td><td>

 

</td><td>

Monitors the tasks within their organizations.

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
</table>## Record producers installed with Healthcare Operations Core

<table id="table_record_producers_hco"><tbody><tr><td>

**Record producer name**

</td><td>

**Description**

</td></tr><tr><td>

Add a member

</td><td>

Adds an existing user to a team and assigns their responsibility. Requires the sn\_hco.care\_team\_manager role.

</td></tr><tr><td>

Remove a member

</td><td>

Removes an existing member from a team. Requires the sn\_hco.care\_team\_manager role.

</td></tr></tbody>
</table>## Script includes installed with Healthcare Operations Core

<table id="table_script_includes_hco"><tbody><tr><td>

**Script include name**

</td><td>

**Description**

</td></tr><tr><td>

Asset

</td><td>

 

</td></tr><tr><td>

AssetDAO

</td><td>

Performs data access operations on the asset table.

</td></tr><tr><td>

HCOBase

</td><td>

 

</td></tr><tr><td>

HCOBaseActionUtil

</td><td>

Base utilities for UI actions. All HCO child applications inherit from this class.

</td></tr><tr><td>

HCOBaseDAO

</td><td>

 

</td></tr><tr><td>

HCOObject

</td><td>

Helper for creating and operating on HCO objects.

</td></tr><tr><td>

HCOObjectBuilder

</td><td>

 

</td></tr><tr><td>

HealthcareOperationsAJAX

</td><td>

 

</td></tr><tr><td>

HealthcareOperationsConstants

</td><td>

 

</td></tr><tr><td>

HealthcareOperationsDAO

</td><td>

 

</td></tr><tr><td>

HealthcareOperationsQueryRules

</td><td>

 

</td></tr><tr><td>

JournalField

</td><td>

Service layer for journal field operations, used in work order to case synchronization.

</td></tr><tr><td>

JournalFieldDAO

</td><td>

Performs data access operations on journal fields, used in work order to case synchronization.

</td></tr><tr><td>

Location

</td><td>

Service layer for location queries.

</td></tr><tr><td>

LocationDAO

</td><td>

Performs data access operations on locations.

</td></tr><tr><td>

ServiceDefinition

</td><td>

 

</td></tr><tr><td>

ServiceDefinitionDAO

</td><td>

 

</td></tr><tr><td>

ServiceOrg

</td><td>

Service layer for service organization queries.

</td></tr><tr><td>

ServiceOrgDAO

</td><td>

Performs data access operations on service organizations and organization members.

</td></tr><tr><td>

ServiceOrgSB

</td><td>

Houses reference qualifiers for HCO service organizations.

</td></tr><tr><td>

WorkOrder

</td><td>

 

</td></tr><tr><td>

WorkOrderDAO

</td><td>

Performs data access operations on the work order table.

</td></tr><tr><td>

WorkOrderSB

</td><td>

 

</td></tr></tbody>
</table>