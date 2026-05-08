---
title: Manage temporary space closures agentic workflow
description: This team of AI agents temporarily block a location when there’s an emergency workplace maintenance case is submitted.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Manage temporary space closures agentic workflow

This team of AI agents temporarily block a location when there’s an emergency workplace maintenance case is submitted.

## Manage temporary space closures workflow overview

AI agent executes maintenance tasks, blocks a room for maintenance, and moves any existing reservation to another location when the emergency workplace maintenance requested is assigned to a user in the Workplace Event Planners assignment group. For more information, see [Submit an emergency maintenance request](../../workplace-case-mgmt/task/submit-emergency-maint-request.md).

The team of AI agents block a room for emergency maintenance and move any existing reservations from the blocked location to another location. Multi-building and group reservations are also handled by the agents. AI agents send notification to Workplace Event planners using the Now Assist panel. The team of AI agents autonomously perform the following:

-   Retrieves the case details from the emergency maintenance request.

    For more information, see [View emergency maintenance case details](../../workplace-case-mgmt/task/view-emergency-maint-case.md).

-   Retrieves impacted reservation from a location and blocks a location for maintenance.

    For more information, see [Block a workplace location](../../workplace-service-delivery/task/block-workplace-location.md).

-   AI agents notifies workplace event planners with case resolution and summarization using the Now Assist panel conversational interface.

    AI agents take confirmation from Workplace planners before blocking a location or before moving a reservation to another location. Workplace Event planners can respond to AI agents queries using the conversational interface of the Now Assist panel. For more information, see [Review notifications in the Now Assist panel](../task/agentic-workflow-notifications-nowassist.md).

-   Updates the emergency maintenance request case notes with all the actions taken. Workplace Event planners can review the activity log to know the actions taken by AI agents.

    For more information, see [View emergency maintenance case details](../../workplace-case-mgmt/task/view-emergency-maint-case.md).


## Manage temporary space closures workflow

To access the Maintenance Meeting rooms workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview** &gt; **Manage Temporary space closures**. For more information, see [AI agents used in the Manage temporary space closures workflow](maintenance-meeting-room-agent-ai.md#section_ifc_bby_w2c).

    The Manage temporary space closure Describe and Connect workflow opens.

2.  Select **Define Trigger** to review the trigger factor \(Emergency Meeting rooms\) for this agentic workflow. For more information, see [Triggers for the Manage temporary space closures](maintenance-meeting-room-agent-ai.md#section_df4_y1y_w2c).
3.  The **Select Display** option enables the Now Assist panel. For more information, see [Select display](maintenance-meeting-room-agent-ai.md#section_bc5_ykn_x2c).

## AI agents used in the Manage temporary space closures workflow

The **Connect AI agents** section in the Describe and Connect workflow displays the AI Agents that are working on the Manage temporary space closure workflow.

The following agents are used to Manage temporary space closures workflow:

<table id="table_cgv_crg_x2c"><thead><tr><th>

AI agent Name

</th><th>

Description

</th><th>

AI agent tools and resources

</th></tr></thead><tbody><tr><td>

Workplace Case notes

</td><td>

Workplace case notes updater

</td><td>

Workplace case notes update

</td></tr><tr><td>

Case Retriever

</td><td>

Case Retriever

</td><td>

-   Get meeting room maintenance case details.
-   Get details of change event case details.

.

</td></tr><tr><td>

Reservation resolution processing AI agent

</td><td>

Reservation resolution processing AI Agent

</td><td>

-   Auto-resolution for all the reservations.
-   Fetch Reservations for a location and time range,Block location

</td></tr></tbody>
</table>## Triggers for the Manage temporary space closures

When an emergency maintenance request is assigned to a user in the Workplace Event Planners group, AI agentic workflow Manage temporary space closures is triggered. In the Define trigger workflow, the agentic workflow begins executing when the trigger meets the following conditions:

<table id="table_tdl_1zf_1fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Emergency maintenance case

</td></tr><tr><td>

Trigger

</td><td>

Created or updatedAn emergency maintenance case is submitted and a workplace case is created. When the workplace case is assigned to Workplace Event planners, AI agentic**Manage temporary space closures** workflow is triggered.

</td></tr><tr><td>

Table

</td><td>

Workplace Case \[sn\_wsd\_case\_workplace\_case\]

</td></tr><tr><td>

Conditions

</td><td>

\[Assigned to\] \[is not empty\]\[Workplace service\] is \[Emergency maintenance\]

</td></tr><tr><td>

Run as

</td><td>

assigned\_to

</td></tr><tr><td>

Channel

</td><td>

Now Assist panel

</td></tr><tr><td>

Status

</td><td>

Active**Note:** When the status is Active, the AI agent is triggered autonomously.

</td></tr></tbody>
</table>## Select display

In the Select display workflow, select **Display** to display the Now Assist panel. Workplace users with the now\_assist\_panel\_role receive notifications for the triggered use case output. When the Now Assist panel option is enabled, the AI agent output or notifications are displayed in the Now Assist panel.

**Note:** To view the output from a triggered use case, you should have the now\_assist\_panel\_role.

Select this option to receive and review notifications send by AI agents in the Now Assist panel. AI agents send notifications to Workplace Event planners in the Now Assist panel with the case resolution and summarization notes. It asks for Workplace Event planners confirmation before blocking a location and moving any impacted reservations to another available workspace or before updating an existing reservation's date, time, and duration. For more information, see [Review notifications in the Now Assist panel](../task/agentic-workflow-notifications-nowassist.md).

**Parent Topic:**[Using AI agent workflows in Now Assist for WSD](now-assist-wsd-using-agentic-use-cases.md)

**Related topics**  


[Help manage workplace reservations agentic workflow](manage-workplace-reservations-agent-ai.md)

[Optimize cleaning activities agent overview](optimise-cleaning-agent-overview.md)

[Automate map updates agentic workflow](automate-map-updates-agent-ai.md)

[Workplace Advisor Overview](workplace-advisor-overview.md)

[Workplace Concierge agentic workflow](workplace-concierge-ai-agent.md)

[implement-autonomous-l1-agent-for-workplace.md](implement-autonomous-l1-agent-for-workplace.md)

[bundle-platai.na-ai-agents]

[bundle-platai.install-ai-agents-plugins]

[bundle-platai.ai-agent-studio]

