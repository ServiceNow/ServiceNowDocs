---
title: Change management for Field Service components
description: Various plugins, script includes, and business rules are installed with the Change Management for Field Service application.
locale: en-US
release: xanadu
product: Field Service Integrations
classification: field-service-integrations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration with Change Management, Integrating Field Service Management with other applications, Configuring Field Service Management, Field Service Management]
---

# Change management for Field Service components

Various plugins, script includes, and business rules are installed with the Change Management for Field Service application.

## Plugin

The Change Management for Field Service application \(sn\_fsm\_chg\_mng\) plugin must be activated. For more information on the steps to activate a plugin, see [Install Change Management for Field Service](../task/install-change-for-fsm.md).

<table id="table_ikv_hhv_wqb"><thead><tr><th>

Script Include

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ChangeRequestWorkOrderUtil

</td><td>

Updates the change request work notes when any of the following actions happen: -   The state of work order changes.
-   The change request is automatically closed when the work order is closed
-   The work order is deleted.

</td></tr><tr><td>

ChangeWorkOrderIntegration

</td><td>

Provides the default implementation that helps integrating the change requests with work orders using the extension point.

</td></tr></tbody>
</table>## Business rules

Change Management for Field Service adds the following new business rules.

<table id="table_xrp_phv_wqb"><thead><tr><th>

Business Rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cancel Work Order

</td><td>

Change Request \[change\_request\]

</td><td>

Cancels the work order when the change request is canceled.

</td></tr><tr><td>

Populate Window Start/End with Change

</td><td>

Service Order Task \[sm\_task\]

</td><td>

Populates the window start and end dates of the work order task with the planned start and end dates that are defined in the change request.

</td></tr><tr><td>

Update Change with Work Order Changes

</td><td>

Work Order \[wm\_order\]

</td><td>

Updates the change request when the state of the work order changes. Automatically closes the change request if the work order is Closed Complete.

</td></tr><tr><td>

Update Work order deletion to Change

</td><td>

Work Order \[wm\_order\]

</td><td>

Updates the work notes of the change request if the work order is deleted.

</td></tr><tr><td>

Validate Requested Due By with Change

</td><td>

Work Order \[wm\_order\]

</td><td>

Validates whether the requested due by date that is defined on the work order is before the planned end date of the change request.

</td></tr><tr><td>

ValidateWindowStartEndDatewithChange

</td><td>

Work Order Task \[wm\_task\]

</td><td>

Validates whether the window start and end date of the work order task is scheduled within the start and end dates of the change request.

</td></tr></tbody>
</table>## Roles

Change Management for Field Service modifies the following existing role.

<table id="table_uqn_gpb_jvb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Field Service Management Agent\[wm\_agent\]

</td><td>

Manages actual task time and performs work on site. Agents can view parent change request details from the work order task.

</td><td>

sn\_change\_read

</td></tr></tbody>
</table>