---
title: Assign roles for CMDB success advisor users
description: Assign roles to control access to features, capabilities, and data in the CMDB success advisor application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-assign-roles.html
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-07-22"
reading_time_minutes: 2
keywords: [assign CMDB success advisor roles, CMDB success advisor role requirements, sn\_cmdb\_admin sn\_cmdb\_user roles, scope\_user scope\_editor roles]
breadcrumb: [Configure, CMDB success advisor, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Assign roles for CMDB success advisor users

Assign roles to control access to features, capabilities, and data in the CMDB success advisor application.

## Before you begin

Set the application scope to CMDB success advisor using the application picker. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/c_ApplicationPicker.md).

Role required: admin

## About this task

Users with the following combination of roles can use the CMDB success advisor application.

<table id="table_fqd_mng_jgc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Applies to

</th></tr></thead><tbody><tr><td>

sn\_cmdb\_admin

</td><td>

Required to access the CMDB success advisor. Users with the sn\_cmdb\_admin role can configure and improve CMDB data accuracy based on specific business use cases.

</td><td>

Data Foundations, HAM, and SAM dashboards

</td></tr><tr><td>

sn\_cmdb\_user

</td><td>

Provides read-only access to CMDB success advisor from the Insights section in Service Graph Workspace. Users with this role can view the Dashboard tab only. Users with this role can't access the Settings and Integrations tabs.

</td><td>

Data Foundations, HAM, and SAM dashboards

</td></tr><tr><td>

sn\_cmdb\_editor

</td><td>

Provides read-only access to CMDB success advisor from the Insights section in Service Graph Workspace. Users with this role can view the Dashboard tab only. Users with this role can't access the Settings and Integrations tabs.

</td><td>

Data Foundations, HAM, and SAM dashboards

</td></tr><tr><td>

sn\_cmdb\_advisor.scope\_user

</td><td>

Provides read-only access to CMDB success advisor pages and data, including the AI-generated summary and remediation actions on the HAM dashboard.**Note:** Also, requires the sn\_cmdb\_user role.

</td><td>

Data Foundations, HAM, and SAM dashboards

</td></tr><tr><td>

sn\_cmdb\_advisor.scope\_editor

</td><td>

Required to edit dashboard scope and content template settings for SAM. The sn\_cmdb\_advisor.scope\_editor role contains the sn\_cmdb\_advisor.scope\_user role.**Note:** Also, requires the sn\_cmdb\_user role. For Data Foundations and HAM dashboards, editing scope requires the sn\_cmdb\_admin role. The scope\_editor role doesn't grant scope edit access for these products.

</td><td>

SAM dashboard

</td></tr><tr><td>

sam\_user

</td><td>

Required to view the SAM advisor dashboard in read-only mode.

</td><td>

SAM dashboard

</td></tr><tr><td>

sam\_admin

</td><td>

Required to select or edit the software products in the SAM advisor scope.

</td><td>

SAM dashboard

</td></tr><tr><td>

cmdb\_inst\_admin

</td><td>

Required to manage Service Graph Connector connections in SGC Central through CMDB success advisor.**Note:** Service Graph Connector data can be read without any additional role. The cmdb\_inst\_admin role is required for creating or modifying connector configurations through CMDB success advisor.

</td><td>

Data Foundations and HAM dashboards

</td></tr><tr><td>

pd\_user

</td><td>

Required to view Discovery and Service Mapping Patterns through CMDB success advisor with read-only access.

</td><td>

Data Foundations and HAM dashboards

</td></tr><tr><td>

pd\_admin

</td><td>

Required to manage Discovery patterns with create and write access.

</td><td>

Data Foundations and HAM dashboards

</td></tr></tbody>
</table>For more information, see [Exploring CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-explore.md).

## Procedure

-   Assign roles to users and groups using the ServiceNow AI Platform user administration feature.

    -   To assign a role to a user, see [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/t_AssignARoleToAUser.md).
    -   To assign a role to a group, see [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/t_AssignRoleToGroup.md).

