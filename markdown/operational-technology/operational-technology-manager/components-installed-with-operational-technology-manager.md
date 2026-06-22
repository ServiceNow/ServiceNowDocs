---
title: Components installed with Operational Technology Manager
description: Several types of components may be installed with activation of the Operational Technology Manager application, including user roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/operational-technology/operational-technology-manager/components-installed-with-operational-technology-manager.html
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2024-08-05"
reading_time_minutes: 1
breadcrumb: [Reference, Operational Technology Manager, Operational Technology]
---

# Components installed with Operational Technology Manager

Several types of components may be installed with activation of the Operational Technology Manager application, including user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/find-components.md).

## Plugins installed

|Plugin|Description|
|------|-----------|
|Industrial Core|Contains the class mappings needed for the OT Service Graph Connectors.|

## Roles installed

|Role|Description|
|----|-----------|
|Operational Technology Discovery Administrator \[ot\_discovery\_admin\]|Can run the Discovery for Operational Technology process, but cannot access the Configuration Management Database \(CMDB\) to view the configuration items \(CIs\) and related Operational Technology \(OT\) entities that are created from discovered items. To learn more, see [Create an Operational Technology discovery schedule and run the Discovery process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/run-discovery-for-operational-technology.md).|
|Operational Technology Manager Viewer \[cmdb\_ot\_viewer\]|Read-only access to Operational Technology \(OT\) device records.|
|Operational Technology Manager Editor \[cmdb\_ot\_editor\]|Create, read, update, and delete access for [Operation Technology \(OT\) extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-ci-class-models-operation-technology.md).|
|Operational Technology Manager Admin \[cmdb\_ot\_admin\]|Create, read, update, and delete access for Operational Technology \(OT\) device records. Can also edit and manage specific configurations in the OT entity type. To learn more, see [Operation Technology \(OT\) extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-ci-class-models-operation-technology.md).|

**Parent Topic:**[Operational Technology Manager reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/operational-technology-manager-reference.md)

