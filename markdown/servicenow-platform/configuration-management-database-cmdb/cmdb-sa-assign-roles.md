---
title: Assign roles for CMDB success advisor users
description: Assign roles to control access to features, capabilities, and data in the CMDB success advisor application.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Assign roles for CMDB success advisor users

Assign roles to control access to features, capabilities, and data in the CMDB success advisor application.

## Before you begin

Set the application scope to CMDB success advisor using the application picker. For more information, see Application picker.

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

Data Foundations and HAM dashboards

</td></tr><tr><td>

pa\_data\_collector

</td><td>

Required to view the last updated data timestamp on the dashboard.

</td><td>

Data Foundations and HAM dashboards

</td></tr><tr><td>

pa\_viewer

</td><td>

Required to filter data by principal classes in Data Foundations advisor dashboard and model categories in HAM advisor dashboard.

</td><td>

Data Foundations and HAM dashboards

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
</table>For more information, see [Exploring CMDB success advisor](../concept/cmdb-sa-explore.md).

## Procedure

-   Assign roles to users and groups using the ServiceNow AI Platform user administration feature.

    -   To assign a role to a user, see Assign a role to a user.
    -   To assign a role to a group, see Assign a role to a group.

