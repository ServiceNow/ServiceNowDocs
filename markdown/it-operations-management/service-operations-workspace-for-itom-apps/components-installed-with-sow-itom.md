---
title: Components installed with AIOps Experience
description: Several types of components are installed with activation of the AIOps Experience \[sn\_sow\_aiops\] application, including user role and plugins.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Operations Workspace for ITOM reference, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Components installed with AIOps Experience

Several types of components are installed with activation of the AIOps Experience \[sn\_sow\_aiops\] application, including user role and plugins.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|evt\_mgmt\_user|Can manage the lifecycle of alerts. Can perform basic operations such as viewing of alerts.|itil|
|evt\_mgmt\_operator|Can manage alerts, including closing and acknowledging them.|evt\_mgmt\_user|
|evt\_mgmt\_admin|Can configure and set up Event Management properties and rules.|evt\_mgmt\_user and evt\_mgmt\_operator|

## Plugins installed

<table id="table_ics_vsk_xsb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event Management\[com.glideapp.itom.snac\]

</td><td>

Provides service-oriented availability and monitor events through an intuitive console.

</td></tr><tr><td>

Performance Analytics - Premium\[com.snc.pa.em\]

</td><td>

Provides core out-of-the-box Key Performance Indicators \(KPIs\) to help monitor and enhance event management processes. Please note that activating this plugin on production instances may require a separate Performance Analytics license.

</td></tr><tr><td>

Performance Analytics - Content Pack - Event Management\[com.snc.pa.premium\]

</td><td>

Includes core out-of-the-box Key Performance Indicators \(KPIs\). Activating this plugin on production instances may require a separate Performance Analytics license.

</td></tr></tbody>
</table>To return to the main topic, see [Install Service Operations Workspace for ITOM application](../task/install-sow-itom-apps.md).

**Parent Topic:**[Service Operations Workspace for ITOM reference](../concept/sow-reference-itom.md)

