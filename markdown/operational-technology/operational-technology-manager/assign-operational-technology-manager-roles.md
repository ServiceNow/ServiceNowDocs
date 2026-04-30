---
title: Assign Operational Technology Manager roles
description: Assign roles to your users so that you can control their access to the features, capabilities, and data in the Operational Technology Manager application.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Operational Technology Manager, Operational Technology]
---

# Assign Operational Technology Manager roles

Assign roles to your users so that you can control their access to the features, capabilities, and data in the Operational Technology Manager application.

## Before you begin

Role required: admin

## About this task

Users with the roles that are listed in the following table can use the Operational Technology Manager application.

If you want to configure site users, you can create and assign user criteria for equipment model entity site users. For more information, see [Assign or remove equipment model site access for non-administrators](../../mftg-manufacturing-process-mgr/task/create-user-criteria-for-equipment-model-entity-site-users.md).

|Role|Description|
|----|-----------|
|Operational Technology Discovery Administrator \[ot\_discovery\_admin\]|Can run the Discovery for Operational Technology process, but cannot access the Configuration Management Database \(CMDB\) to view the configuration items \(CIs\) and related Operational Technology \(OT\) entities that are created from discovered items. To learn more, see [Create an Operational Technology discovery schedule and run the Discovery process](run-discovery-for-operational-technology.md).|
|Operational Technology Manager Viewer \[cmdb\_ot\_viewer\]|Read-only access to Operational Technology \(OT\) device records.|
|Operational Technology Manager Editor \[cmdb\_ot\_editor\]|Create, read, update, and delete access for [Operation Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).|
|Operational Technology Manager Admin \[cmdb\_ot\_admin\]|Create, read, update, and delete access for Operational Technology \(OT\) device records. Can also edit and manage specific configurations in the OT entity type. To learn more, see [Operation Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).|

## Procedure

1.  Assign roles to users and groups by using the ServiceNow AI Platform user administration feature.

    |Task|User administration feature|
    |----|---------------------------|
    |**Assign a role to a user**|See [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).|
    |**Assign a role to a group**|See [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).|


**Parent Topic:**[Configuring the Operational Technology Manager](../concept/configuring-operational-technology-manager.md)

