---
title: Components installed with AIOps Experience
description: Several types of components are installed with activation of the AIOps Experience \[sn\_sow\_aiops\] application, including user role and plugins.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Operations Workspace for ITOM reference, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Components installed with AIOps Experience

Several types of components are installed with activation of the AIOps Experience \[sn\_sow\_aiops\] application, including user role and plugins.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

evt\_mgmt\_user

</td><td>

Manages the alert lifecycle and performs basic operations, such as viewing alerts.

</td><td>

itil

</td></tr><tr><td>

evt\_mgmt\_operator

</td><td>

Manages alerts, including tasks such as closing and acknowledging them.

</td><td>

evt\_mgmt\_user

</td></tr><tr><td>

evt\_team\_operator

</td><td>

Manages Event Management operations within a specific team as defined in the **Assignment Group** field. This role allows the operator to read and write alerts exclusively for their assigned team. Additionally, the operator can make configuration changes specific to their team, including updates to Alert Automation and the Integrations Launchpad.**Note:** The evt\_team\_operator role must be assigned to an assignment group to view and manage alerts for that group. If the role is created but not associated with any groups that have alerts assigned, the operator cannot see any alerts.

</td><td>

sn\_sow\_alert\_rules.automation\_create\_nonglobal

 sn\_sow\_alert\_rules.automation\_delete\_nonglobal

</td></tr><tr><td>

evt\_mgmt\_admin

</td><td>

Configures and sets up Event Management properties and rules.

</td><td>

evt\_mgmt\_user and evt\_mgmt\_operator

</td></tr></tbody>
</table>## Plugins installed

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
</table>To return to the procedure, see [Install Service Operations Workspace for ITOM application](../task/install-sow-itom-apps.md).

**Parent Topic:**[Service Operations Workspace for ITOM reference](../concept/sow-reference-itom.md)

