---
title: Components installed with Healthcare Computerized Maintenance Management System
description: Several types of components are installed with installation of the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application, including tables, user roles, plugins, ServiceNow Store applications, and business rules.
locale: en-US
release: zurich
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Healthcare Computerized Maintenance Management System, Clinical Device Management, Healthcare and Life Sciences]
---

# Components installed with Healthcare Computerized Maintenance Management System

Several types of components are installed with installation of the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application, including tables, user roles, plugins, ServiceNow Store applications, and business rules.

**Important:** Healthcare Computerized Maintenance Management System is now deprecated and no longer supported or available for new activation. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](../concept/clinical-device-mgmt-overview.md).

Demo data is available for this feature.

## Roles installed

<table id="table_bpg_lcv_55b"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_hcls\_cmms.case\_creator

</td><td>

Grants access to create medical device cases.

</td><td>

sn\_hcls\_cmms.case\_viewer

</td></tr><tr><td>

sn\_hcls\_cmms.case\_viewer

</td><td>

Grants access to view medical device cases.

</td><td>

None

</td></tr><tr><td>

sn\_hcls\_cmms.clinical\_engineer

</td><td>

Creates and updates maintenance plans for medical device models and install base items for medical devices. Works on medical device cases.

</td><td>

-   sn\_customerservice\_agent
-   sn\_hcls\_cmms.sm\_agent

</td></tr><tr><td>

sn\_hcls\_cmms.clinical\_engineering\_admin

</td><td>

Administers who can access the Healthcare CMMS application.

</td><td>

-   sn\_hcls\_cmms.clinical\_engineer
-   sn\_risk\_advanced.ara\_admin
-   wm\_admin

</td></tr><tr><td>

sn\_hcls\_cmms.clinical\_engineering\_technician

</td><td>

Works at medical device locations and records details in the work order form, including parts used and incidental expenses.

</td><td>

-   sn\_hcls.device\_data\_viewer
-   sn\_hcls.foundation\_data\_viewer
-   sn\_hcls\_cmms.case\_viewer
-   wm\_agent

</td></tr><tr><td>

sn\_hcls\_cmms.device\_service\_org\_contributor

</td><td>

Creates medical device cases for a organization as a clinician.

 **Note:** To create medical device cases for a organization \(business location\), a user with the sn\_hcls\_cmms.device\_service\_org\_contributor role must be the member of the organization and assigned the **Location Contributor** responsibility type. The mapping of a organization and its members is included in the Organization Member \[sn\_csm\_service\_organization\_member\] table.

</td><td>

-   sn\_customerservice.service\_organization\_contributor
-   sn\_hcls.device\_data\_viewer
-   sn\_hcls.foundation\_data\_viewer
-   sn\_hcls\_cmms.case\_creator

</td></tr><tr><td>

sn\_hcls\_cmms.sm\_agent

</td><td>

Accesses and views all device data and medical device cases.

</td><td>

-   model\_manager
-   sn\_fsm\_planned\_wm.planned\_work\_admin
-   sn\_hcls.device\_data\_writer
-   sn\_hcls.foundation\_data\_writer
-   sn\_hcls\_cmms.case\_creator
-   sn\_risk\_advanced.ara\_assessor
-   sn\_risk\_advanced.ara\_creator

</td></tr></tbody>
</table>## Tables installed

<table id="table_xvw_ddv_55b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Medical device case \[sn\_hcls\_cmms\_case\]

</td><td>

Stores the medical device cases.

</td></tr></tbody>
</table>## Plugins installed

<table id="table_y2q_sdv_55b"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Service with Field Service Management \(com.snc.csm\_fsm\_integration\)

</td><td>

Enables the integration between the Healthcare CMMS and Field Service Management applications and makes available account, contact, partner, partner contact, and consumer information from Customer Service in Field Service Management.

</td></tr></tbody>
</table>## ServiceNow Store applications installed

<table id="table_ldj_jhj_sqb"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Healthcare and Life Sciences Service Management Core \(sn\_hcls\)

</td><td>

Provides a data model and critical digital health capabilities including patient 360-degree view, consent management, and digital documentation to better address healthcare services.

</td></tr><tr><td>

GRC: Advanced Risk \(com.sn\_risk\_advanced\)

</td><td>

Enables decision makers to avoid any negative impact on business operations by identifying, assessing, responding to, and continuously monitoring risks.

</td></tr><tr><td>

GRC: Common Workspace Elements \(sn\_grc\_workspace\)

</td><td>

Enables the use of the Advanced Risk feature in the CSM Configurable Workspace.

</td></tr><tr><td>

Performance Analytics Content Pack for Healthcare CDM \(sn\_hcls\)

</td><td>

Install the Performance Analytics Content Pack for Healthcare CDM separately from ServiceNow Store.

 Provides Performance Analytics capabilities and dashboard for healthcare clinical device management applications. The dashboard provides visibility to the clinical engineering team to refer to all the metrics of the CMMS application.

</td></tr></tbody>
</table>## Business rules installed

<table id="table_lyf_vdl_4pb"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Rule criteria

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create inspect WOs

</td><td>

Medical device case \[sn\_hcls\_cmms\_case\]

</td><td>

Async update

</td><td>

Creates work orders for the initial inspection of a medical device when the state of the associated medical device in-service case is set to **Device setup**.

</td></tr><tr><td>

Mark devices as installed

</td><td>

Medical device case \[sn\_hcls\_cmms\_case\]

</td><td>

Async update

</td><td>

Sets the install state of a medical device to **Installed** or **Canceled** when the state of the associated medical device in-service case is set to **Closed complete** or **Canceled**, respectively.

</td></tr><tr><td>

Setup medical device model

</td><td>

Medical device case \[sn\_hcls\_cmms\_case\]

</td><td>

Before update

</td><td>

Creates a medical device model when none exists for a medical device and the state of the associated medical device in-service case is set to **Model setup**.

</td></tr><tr><td>

Trigger medical device AEM approval

</td><td>

Medical device case \[sn\_hcls\_cmms\_case\]

</td><td>

Async update

</td><td>

Triggers the approval workflow, if available, for an alternative equipment maintenance \(AEM\) request.

</td></tr></tbody>
</table>