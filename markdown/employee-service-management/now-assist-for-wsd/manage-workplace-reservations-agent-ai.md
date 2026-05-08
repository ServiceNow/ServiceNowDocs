---
title: Help manage workplace reservations agentic workflow
description: The Help manage workplace reservations agentic AI workflow enables Workplace Event Planners with rescheduling a planned reservation. AI Agents gather relevant information from a workplace reservation and update an existing planned reservation with a new date, time, and duration.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Help manage workplace reservations agentic workflow

The Help manage workplace reservations agentic AI workflow enables Workplace Event Planners with rescheduling a planned reservation. AI Agents gather relevant information from a workplace reservation and update an existing planned reservation with a new date, time, and duration.

AI agents retrieve the reservation from the change event reservation case details. AI agents analyze an existing reservation before updating it with a new date and time. If the old location is not available while updating an existing reservation, AI agents update and move the reservation to a new location. For more information, see [Submit a change event request for a reservation](../../workplace-case-mgmt/task/submit-change-event-reservation.md).

A change event request is submitted for updating an existing reservation by a workplace user. A workplace case is created with a new workplace service. The workplace case is assigned to a user in the Workplace Event planners assignment group.

The team of AI agents autonomously perform the following:

-   Retrieve the change event request workplace case details when it assigned to a Workplace Event planner.
-   Analyze the reservation retrieved from the previous step. If the old location is available while updating a reservation's date, time, and duration, AI agents update the reservation. If the old location is not available for reservation, AI agents move the reservation to a new location while updating the reservation date, time, and duration.
-   Send notification to Workplace Event planners using the Now Assist panel conversational interface.

    Workplace Event planners can respond to AI agents queries using the conversational interface of the Now Assist panel. AI agents take confirmation from Workplace planners before updating a reservation to another location if the old location is not available. It shows three workplace locations. You can select the location or ask the AI agents to show more locations. AI agent provide a link for you to click and navigate to the reservation page to manually select a location of your choice.

    For more information, see [Review notifications in the Now Assist panel](../task/agentic-workflow-notifications-nowassist.md).

-   Update the change event request case work notes with all the actions taken. Workplace Event planners can review the activity log to see the actions taken by AI agents to update a planned reservation event.

    For more information, see [View change event reservation case details](../../workplace-case-mgmt/task/view-case-change-event-reservation.md).


For more information, see [View change event reservation case details](../../workplace-case-mgmt/task/view-case-change-event-reservation.md).

## Help manage workplace reservations

To access the Help manage workflow reservations:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview** &gt; **Help manage workplace reservations.**.

    The Describe and Connect workflow is displayed. For more information, see [AI agents used in the Help manage workplace reservations](manage-workplace-reservations-agent-ai.md#section_llt_xtb_1fc).

2.  Select **Define Trigger** to review the trigger factor \(Emergency Meeting rooms\) for this agentic workflow. For more information, see [Triggers for Help manage workplace reservations](manage-workplace-reservations-agent-ai.md#section_eq4_15b_1fc)
3.  The **Select Display** option enables the Now Assist panel. For more information, see [Select display](manage-workplace-reservations-agent-ai.md#section_bc5_ykn_x2c).

## AI agents used in the Help manage workplace reservations

The **Connect AI agents** section in the Describe and Connect workflow displays the AI Agents that are working on the Help manage workplace reservations workflow.

The following agents are used in the Manage temporary space closures workflow:

|AI agent Name|Description|AI agent tools and resourcesR|
|-------------|-----------|-----------------------------|
|Reservation updating AI agent|Reservation updating AI agent|Update the reservation.|
|Case Retriever|Case Retriever|Get details of change event case details.|
|Reservation analyzing AI agent|Reservation analyzing AI agent|Get edit link of reservation and alternate space recommendations.|
|Workplace case notes updater|Workplace case notes updater.|Workplace case notes updated for a workplace case created for a change event request.|

## Triggers for Help manage workplace reservations

In the Define trigger workflow, the agentic workflow begins executing when the trigger meets the following conditions:

<table id="table_tdl_1zf_1fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Reservation date change

</td></tr><tr><td>

Trigger

</td><td>

Created or updatedA Change Event request is submitted and a workplace case is created. When the workplace case is assigned to Workplace Event planners, AI agentic**Help manage workplace reservations** workflow is triggered.

</td></tr><tr><td>

Table

</td><td>

Workplace Case \[sn\_wsd\_case\_workplace\_case\]

</td></tr><tr><td>

Conditions

</td><td>

\[Assigned to\] \[is not empty\]\[Workplace service\] is \[Event Planning\]

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

In the Select display workflow, select **Display** to display the Now Assist panel. Workplace users with the now\_assist\_panel\_role receive notifications for the triggered case. When the Now Assist panel option is enabled, the AI agent output or notifications are displayed in the Now Assist panel.

**Note:** To view the output from a triggered use case, you should have the now\_assist\_panel\_role.

Select this option to receive and review notifications by AI agents in the Now Assist panel. AI agents notify Event planners in the Now Assist panel with the case resolution and summarization notes. For more information, see [Review notifications in the Now Assist panel](../task/agentic-workflow-notifications-nowassist.md).

**Parent Topic:**[Using AI agent workflows in Now Assist for WSD](now-assist-wsd-using-agentic-use-cases.md)

**Related topics**  


[Manage temporary space closures agentic workflow](maintenance-meeting-room-agent-ai.md)

[Optimize cleaning activities agent overview](optimise-cleaning-agent-overview.md)

[Automate map updates agentic workflow](automate-map-updates-agent-ai.md)

[Workplace Advisor Overview](workplace-advisor-overview.md)

[Workplace Concierge agentic workflow](workplace-concierge-ai-agent.md)

[implement-autonomous-l1-agent-for-workplace.md](implement-autonomous-l1-agent-for-workplace.md)

[bundle-platai.na-ai-agents]

[bundle-platai.install-ai-agents-plugins]

[bundle-platai.ai-agent-studio]

