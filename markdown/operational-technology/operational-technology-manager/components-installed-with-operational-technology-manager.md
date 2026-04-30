---
title: Components installed with Operational Technology Manager
description: Several types of components may be installed with activation of the Operational Technology Manager application, including user roles.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Operational Technology Manager, Operational Technology]
---

# Components installed with Operational Technology Manager

Several types of components may be installed with activation of the Operational Technology Manager application, including user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Plugins installed

<table id="table_mb5_53x_cdc"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Industrial Core

</td><td>

Contains the class mappings needed for the OT Service Graph Connectors.For more information about the Industrial Core plugin, see [Industrial Core plugin](industrial-core-plugin.md).

</td></tr></tbody>
</table>## Roles installed

<table id="table_q55_vpq_4nb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operational Technology Discovery Administrator \[ot\_discovery\_admin\]

</td><td>

Can run the Discovery for Operational Technology process, but cannot access the Configuration Management Database \(CMDB\) to view the configuration items \(CIs\) and related Operational Technology \(OT\) entities that are created from discovered items. To learn more, see [Create an Operational Technology Discovery schedule and run the Discovery process](../task/run-discovery-for-operational-technology.md).

</td></tr><tr><td>

Operational Technology Manager Viewer \[cmdb\_ot\_viewer\]

</td><td>

Read-only access to Operational Technology \(OT\) device records.

</td></tr><tr><td>

Operational Technology Manager Editor \[cmdb\_ot\_editor\]

</td><td>

Create, read, update, and delete access for [Operation Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).**Note:** Users assigned the **cmdb\_ot\_editor** role can edit and delete only OT configuration items \(CIs\), and don't have the ability to edit IT CIs.

</td></tr><tr><td>

Operational Technology Manager Admin \[cmdb\_ot\_admin\]

</td><td>

Create, read, update, and delete access for Operational Technology \(OT\) device records. Can also edit and manage specific configurations in the OT entity type. To learn more, see [Operation Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).**Note:** Users assigned the **cmdb\_ot\_editor** role can edit and delete only OT configuration items \(CIs\), and don't have the ability to edit IT CIs.

</td></tr></tbody>
</table>**Parent Topic:**[Operational Technology Manager reference](operational-technology-manager-reference.md)

