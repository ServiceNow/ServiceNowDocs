---
title: Assign Pre-import OT Worksheet Entry Review roles
description: Assign roles to the users  or user groups so that you can manage the Service Graph Connector for Microsoft Excel staging table and ETL.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-02-24"
reading_time_minutes: 1
breadcrumb: [Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Assign Pre-import OT Worksheet Entry Review roles

Assign roles to the users  or user groups so that you can manage the Service Graph Connector for Microsoft Excel staging table and ETL.

## Before you begin

Role required: admin or user\_admin

## About this task

Users with the roles that are listed in the following table can use the Operational Technology Manager application.

|Role|Description|
|----|-----------|
|OT Staging User \[ot\_staging\_user\]|Can create, edit, and view records in the staging table.|
|CMDB Inst Admin \[cmdb\_inst\_admin\]|Can view and edit ETL.|
|OT Excel Import User \[ot\_excel\_import\_user\]|Can create, edit, and view Import Tasks. This is the minimum role to perform Excel SGC imports via Import Tasks. This role contains ot\_staging\_user.|
|CMDB OT Editor \[cmdb\_ot\_editor\]|Can view and reassign Excel SGC Remediation Tasks. Needs additional ot\_staging\_user role to perform Remediation Tasks.|
|CMDB OT Admin \[cmdb\_ot\_admin\]|Can perform both Import and Remediation Tasks. This role contains both ot\_excel\_import\_user and cmdb\_ot\_editor.|

## Procedure

1.  Assign roles to users and groups by using the ServiceNow AI Platform user administration feature.

    |Task|User administration feature|
    |----|---------------------------|
    |**Assign a role to a user**|See [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).|
    |**Assign a role to a group**|See [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).|


**Parent Topic:**[Configuring the Service Graph Connector for Microsoft Excel](../concept/configuring-service-graph-connector-for-excel.md)

