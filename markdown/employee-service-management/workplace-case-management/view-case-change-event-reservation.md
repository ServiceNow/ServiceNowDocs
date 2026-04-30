---
title: View change event reservation case details
description: Workplace Event planners can view the change event reservation case details and the actions taken by AI agents in the case work notes.
locale: en-US
release: xanadu
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-04-15"
reading_time_minutes: 2
breadcrumb: [Manage Workplace cases, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# View change event reservation case details

Workplace Event planners can view the change event reservation case details and the actions taken by AI agents in the case work notes.

## Before you begin

The following applications should be installed:

-   Workplace Core
-   Workplace Case Management
-   Workplace Reservation Management
-   Workplace Concierge

Role required: sn\_wsd\_rsv.reservation\_planner, sn\_wsd\_case.case\_writer

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Cases** &gt; **All**.

    Select and review the work notes details for a change event reservation case. For more information, see [Submit a change event request for a reservation](submit-change-event-reservation.md).

    ![Workplace case notes showing activity log by AI agentic workflow for updating a change event planned reservation.](../image/wsd-case-notes-change-event-request.png)

    When a change event reservation request is submitted by a workplace user, a workplace case is created. The workplace case is assigned automatically to the Workplace Event Planners group. It is then assigned manually to a user in the Workplace Event Planners assignment group. When the case is assigned to a Workplace Event planner, the AI agentic workflow Help manage workplace reservations is triggered. AI agents autonomously retrieve the reservation from the case details and analyze the reservation to update it to a new date, time, and duration. For more information, see [Help manage workplace reservations agentic workflow](../../now-assist-wsd/task/manage-workplace-reservations-agent-ai.md).

    AI agents notifies the Workplace Event Planners using the Now Assist panel conversational interface. For more information, see [Review notifications in the Now Assist panel](../../now-assist-wsd/task/agentic-workflow-notifications-nowassist.md). The workplace notes are also added for a change event request case.

    The team of AI agents also update the case work notes.

2.  To review the workplace case notes, select a change event request case \(**All** &gt; **Workplace Case Management** &gt; **Workplace Cases** &gt; **All**\).

3.  Scroll down and review the Comments and Work Notes section.

    Review the activity log and resolution notes provided by AI agents for a change event request case.

    ![Workplace case notes activity by AI agentic workflow for change event reservation request showing changed dates for a reservation and reservation retrieval for a location with a new date.](../image/wsd-case-notes-change-event-request.png)


**Parent Topic:**[Manage Workplace cases](../concept/manage-workplace-cases.md)

**Related topics**  


[View and track workplace cases](view-workplace-cases.md)

[View emergency maintenance case details](view-emergency-maint-case.md)

