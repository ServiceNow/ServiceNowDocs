---
title: Components installed with the Incident plugin
description: Several types of components are installed with activation of the Incident plugin in Incident Management.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate Incident, Incident Management plugins, Reference section for Incident Management, Incident Management, IT Service Management]
---

# Components installed with the Incident plugin

Several types of components are installed with activation of the Incident plugin in Incident Management.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[role name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Incident task assigned user\[sn\_incident\_task\_assigned\_user\]

</td><td>

Provides read and write operation privileges to an incident task record for an agent when the record is assigned to the agent.**Note:**

-   You must install and activate the ITSM Roles plugin \(com.snc.itsm.roles\) to use the base system ACLs related to this role.
-   When the ITSM Roles plugin \(com.snc.itsm.roles\) isn't installed and activated on the instance, you can still use the Assigned incident user role \[sn\_incident\_task\_assigned\_user\] but with the following limitations:
    -   The agent has the read access to the assigned incident task record except for the **Work notes** and **Work notes list** fields.
    -   The agent has the write access to the assigned task record except for the following fields:
        -   Assigned to
        -   Short description
        -   Description
        -   Priority
        -   State
        -   Work notes
        -   Work notes list

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Incident\[incident\]

</td><td>

The Incident table is extended from the Task \[task\] table. It inherits all the fields, rules, and policies from the Task table.

</td></tr></tbody>
</table>**Parent Topic:**[Activate Incident](../task/activate-incident-plugin.md)

