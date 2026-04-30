---
title: Incident Management for Field Service components
description: Various plugins, script includes, and business rules are installed with the Incident Management for Field Service application.
locale: en-US
release: xanadu
product: Field Service Integrations
classification: field-service-integrations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration with Incident Management, Integrating Field Service Management with other applications, Configuring Field Service Management, Field Service Management]
---

# Incident Management for Field Service components

Various plugins, script includes, and business rules are installed with the Incident Management for Field Service application.

## Plugin

The Incident Management for Field Service application \(sn\_fsm\_inc\_mng\) plugin must be activated. For more information on the steps to activate a plugin, see [Install Incident Management for Field Service](../task/Install-incident-for-fsm.md).

## Script Includes

Incident Management for Field Service adds the following new script includes.

<table id="table_ikv_hhv_wqb"><thead><tr><th>

Script Include

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IncidentWorkOrderUtil

</td><td>

Updates the incident record work notes when any the following actions happen: -   The state of work order changes.
-   The incident record is automatically resolved when the work order is closed.
-   The work order is deleted

</td></tr><tr><td>

IncidentWorkOrderIntegration

</td><td>

Provides the default implementation that helps in integrating incidents with work orders using the extension point.

</td></tr></tbody>
</table>## Business rules

Incident Management for Field Service adds the following new business rules.

<table id="table_xrp_phv_wqb"><thead><tr><th>

Business Rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cancel Work Order

</td><td>

Incident\[incident\]

</td><td>

Cancels the work order when the incident record is canceled.

</td></tr><tr><td>

Update incident with work order changes

</td><td>

Work Order \[wm\_order\]

</td><td>

Updates the incident record when the state of the work order changes. Automatically closes the incident request if work order is Closed complete.

</td></tr><tr><td>

Update Work order deletion to

</td><td>

Work Order \[wm\_order\]

</td><td>

Updates the work notes of the incident record if the work order is deleted.

</td></tr></tbody>
</table>## Roles

Incident Management for Field Service modifies the following existing role.

<table id="table_uqn_gpb_jvb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Field Service Management Agent\[wm\_agent\]

</td><td>

Manages actual task time and performs work on site. Agents can view parent incident details from the work order task.

</td><td>

sn\_incident\_read

</td></tr></tbody>
</table>**Parent Topic:**[Integration with Incident Management](../concept/incident-for-fsm.md)

