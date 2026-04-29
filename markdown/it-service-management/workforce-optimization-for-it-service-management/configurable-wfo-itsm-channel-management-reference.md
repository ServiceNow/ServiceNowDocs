---
title: Channel Management components in Workforce Optimization for ITSM
description: Workforce Optimization for ITSM has roles to administer channels and queues, properties to configure default behavior, and reports to analyze data in Workforce Optimization for ITSM.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Channels, Workforce Optimization for ITSM, IT Service Management]
---

# Channel Management components in Workforce Optimization for ITSM

Workforce Optimization for ITSM has roles to administer channels and queues, properties to configure default behavior, and reports to analyze data in Workforce Optimization for ITSM.

## Roles

<table id="table_yny_rvc_llb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Channel Management User \[sn\_channel\_mgmt.user\]

</td><td>

Grants read access to channel reports, channel view, and queue report tables.

</td><td>

awa\_manager

</td></tr><tr><td>

Channel Management Admin \[sn\_channel\_mgmt.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) channel reports, channel view, and queue report tables.

</td><td>

-   sn\_channel\_mgmt.user
-   awa\_admin
-   sn\_wfo.admin
-   report\_admin

</td></tr></tbody>
</table>## Properties

**Note:** To use channel management properties, they must be added to the System Property \[sys\_properties\] table. For information on how to add a system property, refer to [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

<table id="table_whl_zfk_twb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_channel\_mgmt.list\_auto\_refresh.enable

</td><td>

Set this property to **false** to disable auto-refresh of lists in Channel Management.-   **Type**: True or False
-   **Default value**: True

</td></tr><tr><td>

sn\_channel\_mgmt.channels\_card\_auto\_refresh.enable

</td><td>

Set this property to **false** to disable auto-refresh of lists in Channel Management.-   **Type**: True or False
-   **Default value**: True

</td></tr><tr><td>

sn\_channel\_mgmt.list\_auto\_refresh.interval.seconds

</td><td>

Sets the frequency for refreshing the channel management list data.-   **Type**: Integer
-   **Default value**: 30

</td></tr><tr><td>

sn\_channel\_mgmt.kpi\_auto\_refresh.interval.seconds

</td><td>

Sets the frequency for refreshing the channel management indicator data.-   **Type**: Integer
-   **Default value**: 5

</td></tr><tr><td>

sn\_channel\_mgmt.channel\_card\_auto\_refresh.interval.seconds

</td><td>

Sets the auto-refresh interval for the cards on channel management overview container.-   **Type**: Integer
-   **Default value**: 120

</td></tr><tr><td>

sn\_channel\_mgmt.filter\_config.enable

</td><td>

When set to **true**, displays the **Assignment Group** interactive filter in channels.-   **Type**: True or False
-   **Default value**: True

</td></tr><tr><td>

sn\_channel\_mgmt.awa\_agent\_temporary\_override\_time.minutes

</td><td>

Overrides the duration set for the channel capacity.-   **Type**: Integer
-   **Default value**: 12 hours

</td></tr></tbody>
</table>## Reports

|Report name|Description|
|-----------|-----------|
|Interaction Work Items Assigned Today|Number of interaction work items assigned on a given day.|
|Abandoned Interaction Work Items|Number of abandoned interaction work items.|
|Unassigned Interaction Work Items|Number of interaction work items not assigned to agents.|
|Average Work Item CSAT Score|Customer Satisfaction score for an average work item.|
|Unassigned Incident Work Items|Number of incident work items not assigned to agents.|
|Completed Interaction Work Items|Number of interaction work items completed by agents.|
|Today's Average Interaction Service Time|Average time it takes to close an interaction.|
|Interaction Work Items Resolved Today|Average number of interaction work items resolved on a given day.|
|New Incident Work Items Created Today|New work items created for incidents on a given day.|
|Average Handling time for Interaction Work Items|Average time taken to resolve interaction work items.|
|Agents Available to take Interaction Work Items|Number of agents available to work on the interaction work items.|
|Breached SLA Incident Work Items|Number of work items with breached SLAs.|
|Open P1 Incident Work Items|Number of work items open for P1 incidents.|
|Incident Work Items Resolved Today|Number of work items resolved on a given day.|
|Average Walkup Interaction Wait Time|The average time a user is in queue before starting a walk-up interaction.|
|Currently Waiting Interaction Work Item|Work items currently in queue waiting to be processed.|

## Interactive Filters for Reports

|Name of the interactive filter|Description|Reference table|
|------------------------------|-----------|---------------|
|Channel Management Agent Filter|Filters the reports based on an agent.|\[sys\_user\]|
|Channel Management Group Filter|Filters the reports based on groups.|\[sys\_user\_group\]|
|Channel Management Queues Filter|Filters reports based on queues.|\[awa\_queue\]|
|Channel Management Service Channel Filter|Filters reports based on service channels.|\[awa\_service\_channel\]|

