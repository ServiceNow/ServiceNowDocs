---
title: Components installed with Enterprise Architecture Workspace
description: Several types of components are installed with activation of the Enterprise Architecture Workspace plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Components installed with Enterprise Architecture Workspace

Several types of components are installed with activation of the Enterprise Architecture Workspace plugin, including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_s3q_s54_c3c"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

EA read user

 sn\_apm.apm\_read

</td><td>

Access to view Enterprise Architecture dashboards provided by the base system and the underlying tables from where the data for the dashboards are retrieved.

</td><td>

View Enterprise Architecture dashboard, Application 360 dashboard, and Application Assessments dashboard.-   -   


</td></tr><tr><td>

EA user

 sn\_apm.apm\_user

</td><td>

Access to update applications, view landscape, and roadmap.

</td><td>

View or update applications. Request to create business applications. View application landscape reports and dashboards. View applications roadmap. View Application 360 dashboard.

Includes:-   pa\_viewer
-   sn\_apm\_mdtl\_com.mdtl\_com\_user
-   currency\_instance\_report\_admin
-   canvas\_user
-   sn\_gf.goal\_user
-   sn\_prod\_cap\_core.sn\_prod\_cap\_core\_delete
-   sn\_prod\_cap\_core.sn\_prod\_cap\_core\_write
-   cmdb\_query\_builder\_read
-   data\_manager\_user
-   sn\_gf.strategy\_planner
-   sn\_prod\_cap\_core.sn\_prod\_cap\_core\_read
-   certification
-   report\_user

</td></tr><tr><td>

EA admin

 sn\_apm.apm\_admin

</td><td>

Create or update application records and access administration activities.

</td><td>

Includes:

-   sn\_apm.apm\_user
-   sn\_apm\_mdtl\_com.mdtl\_com\_admin
-   certification\_admin
-   assessment\_admin

 -   Create/update/delete application categories.
-   Create/update/delete application families.
-   Create/update/delete business processes.
-   Create/update/delete application indicators.
-   Create/update/delete application score profile.
-   Create/update/delete bubble charts.
-   View application indicator scores and application scores.
-   View application assessment dashboard.
-   View Application 360 dashboard

</td></tr><tr><td>

EA Analyst

 sn\_apm.apm\_analyst

</td><td>

Create applications and access landscape and dashboards.

</td><td>

Includes:

-   sn\_apm.apm\_admin
-   data\_manager\_admin
-   treemap\_user

 -   Create/update/delete applications.
-   Create/update/delete application indicator scores.
-   Create/update/delete application scores.
-   Create/update/delete Enterprise Architecture programs and targets.
-   Create/update/delete goals.
-   Access the Enterprise Architecture Service Portal pages for program navigation, category analysis, bubble chart view, application comparisons.
-   Create demand with application strategy related attributes.
-   View Application 360 dashboard.

</td></tr></tbody>
</table>## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|Application Service Software Model Certification On Demand Policy Processor| |
|Business Application Certification On Demand Policy Processor|Certifies the data in the Business Application \[cmdb\_ci\_business\_app\] table when required.|
|Business Application Certification Quarterly Policy Processor|Certifies the data in the Business Application \[cmdb\_ci\_business\_app\] table for every quarter.|
|Software Product Lifecycle Internal Source Certification on Demand Policy Processor| |
|Update Capability Hierarchies In Grid|Updates business capabilities hierarchy in the Business Portfolio page. A hierarchy ID is assigned to the newly created capability.|

## Tables installed

<table id="table_w3q_s54_c3c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

BA Product Model Map \[sn\_apm\_ws\_ba\_product\_model\_map

\]

</td><td>

 

</td></tr><tr><td>

Business Application TRM Product Map \[sn\_apm\_ws\_business\_app\_trm\_product\_map

\]

</td><td>

 

</td></tr><tr><td>

APM EA Configuration \[sn\_apm\_ws\_ea\_configuration

\]

</td><td>

 

</td></tr><tr><td>

EA doc page \[sn\_apm\_ws\_ea\_doc\_page

\]

</td><td>

 

</td></tr><tr><td>

Certifications Elements \[cert\_element\]

</td><td>

Stores quarterly or on-demand certifications for business applications.

</td></tr></tbody>
</table>## UI policies installed

|UI policy|Table|Description|
|---------|-----|-----------|
|Manage access is false|APM EA Configuration \[sn\_apm\_ws\_ea\_configuration\]| |
|Customization type is visualization|APM EA Configuration \[sn\_apm\_ws\_ea\_configuration\]| |
|Customization type is script|APM EA Configuration \[sn\_apm\_ws\_ea\_configuration\]| |
|Manage access is true|APM EA Configuration \[sn\_apm\_ws\_ea\_configuration\]| |
| | | |

## Client scripts installed

<table id="table_mqr_msp_c3c"><thead><tr><th>

Client script

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide/Show Product Capability Related Lis

</td><td>

Business Application \[cmdb\_ci\_business\_app\]

</td><td>

Hide Product Capability related list when model\_id is empty.

</td></tr><tr><td>

Hide Type Field

</td><td>

Architectural Artifact \[sn\_apm\_architectural\_artifact\]

</td><td>

 

</td></tr><tr><td>

if manage access is false

</td><td>

APM EA Configuration \[sn\_apm\_ws\_ea\_configuration\]

</td><td>

 

</td></tr><tr><td>

if section is overview

</td><td>

APM EA Configuration \[sn\_apm\_ws\_ea\_configuration\]

</td><td>

 

</td></tr><tr><td>

Set ADR Type For Artifact Version

</td><td>

Architectural Artifact Version \[sn\_apm\_architectural\_version\]

</td><td>

 

</td></tr></tbody>
</table>## System properties installed

|System property|Description|
|---------------|-----------|
|sn\_apm\_ws.appRationalizationMaximumBubbles|Maximum number of bubbles on the bubble chart to be shown|
|sn\_apm\_ws.app\_indicator\_scoring\_profile| |
|sn\_apm\_ws.app\_rationalization\_default\_filter|Application Rationalization Default Filter|
|sn\_apm\_ws.batch\_size\_ba\_lifecycle\_gantt| |
|sn\_apm\_ws.certificationPolicyTables|Default tables used to show certification policies on enterprise architecture workspace|
|sn\_apm\_ws.record\_mention\_config|Configuration for tagging other ServiceNow records with architectural artifacts in Enterprise Architecture Workspace.|

## Business rules installed

| | | |
|---|---|---|
|Default title for doc page collection|EA doc page \[sn\_apm\_ws\_ea\_doc\_page\]| |
|Populate default values for version note|Architectural Artifact Version \[sn\_apm\_architectural\_version\]| |

**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

