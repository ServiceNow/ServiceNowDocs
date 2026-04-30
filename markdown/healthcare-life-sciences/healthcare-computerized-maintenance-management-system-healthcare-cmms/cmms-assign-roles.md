---
title: Assign roles for Healthcare Computerized Maintenance Management System users
description: Assign roles to control access to features, capabilities, and data in the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application.
locale: en-US
release: xanadu
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 1
breadcrumb: [Configuring Healthcare CMMS, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Assign roles for Healthcare Computerized Maintenance Management System users

Assign roles to control access to features, capabilities, and data in the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application.

## Before you begin

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](../concept/clinical-device-mgmt-overview.md).

Set the application scope to Healthcare Computerized Maintenance Management System using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: sn\_hcls\_cmms.clinical\_engineering\_admin or admin

## About this task

Users with the roles listed in the following table can use the Healthcare CMMS application.

<table id="id_xrx_wdy_qdc"><thead><tr><th>

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
</table>## Procedure

-   Assign roles to users and groups using the user administration feature in ServiceNow AI Platform.

    -   To assign a role to a user, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
    -   To assign a role to a group, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

