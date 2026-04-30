---
title: View emergency maintenance case details
description: Workplace Event planners can view the emergency maintenance case details and the actions taken by AI agents in the case work notes.
locale: en-US
release: xanadu
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2025-09-07"
reading_time_minutes: 3
breadcrumb: [Manage Workplace cases, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# View emergency maintenance case details

Workplace Event planners can view the emergency maintenance case details and the actions taken by AI agents in the case work notes.

## Before you begin

The following applications should be installed:

-   Workplace Core
-   Workplace Case Management
-   Workplace Reservation Management
-   Workplace Concierge

Role required: sn\_wsd\_rsv.reservation\_planner, sn\_wsd\_case.case\_writer

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Cases** &gt; **All**.

    ![Workplace case for Emergency maintenance showing Workplace Event Planners assignment group.](../image/wsd-emergency-maintenance-case-details.png)

    When an emergency maintenance request is submitted, a workplace case is created. For more information about the emergency maintenance request, see [Submit an emergency maintenance request](submit-emergency-maint-request.md).

    The change event request workplace case is automatically assigned to the Workplace Event Planner assignment group. It is then assigned manually to a user in the Workplace Event Planners assignment group. When it is assigned to a Workplace Event Planner, AI agentic workflow Manage temporary space closures is triggered. AI agents block a location for maintenance and move any impacted reservations from the blocked location to an available new location. For more information, see [Manage temporary space closures agentic workflow](../../now-assist-wsd/task/maintenance-meeting-room-agent-ai.md).

    Event planners can review the notifications sent by AI agents in the Now Assist panel. AI agents notifies Workplace Event Planners about actions taken through case resolution and case summarization notes in the conversational interface. For more information, see [Review notifications in the Now Assist panel](../../now-assist-wsd/task/agentic-workflow-notifications-nowassist.md).

    The team of AI agents also update the case work notes.

2.  To review the work notes for a case, select an emergency maintenance request case \(**All** &gt; **Workplace Case Management** &gt; **Workplace Cases** &gt; **All**\).

3.  Scroll down and select the Comments and Work Notes section.

    The emergency maintenance case activities are also added to the work notes of a case. Workplace Event planners can review the work notes to understand the activities performed by AI agents. Review the activity log and resolution notes provided by AI agents for an emergency maintenance case.

    ![Comments and Work notes section showing the emergency maintenance case activity log and resolution notes.](../image/wsd-case-comments-notes.png)

    ![Emergency Maintenance request showing the agent activity notes in the Activity tab.](../image/wsd-new-emergency-maintenance-case-notes-ai.png)

4.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **All Reservations** &gt; **Workplace Reservations**.

    -   Review the multi-building or single building reservation that was canceled from a location for workplace maintenance.

        The reservation gets moved to a new location. For example, Kingston campus.

    -   Select and open the reservation \(Kingston\) that is in confirmed state and moved to a new location.
    -   From the Related List, select the **Requested Service Items** tab.

        Verify the workplace reservation services that are moved from the canceled reservation location to the new reservation location.

        ![Selected reservation showing the moved workplace services in the Requested Service Items tab.](../image/wsd-new-extra-services-added-agenticai.png)

    -   From the Related List, select the **Invitees** tab.

        Verify the invitees that are moved to the selected or moved reservation location.

    -   Navigate to the Reservation summary page to verify the canceled reservation and the updated reservation with a new location.
5.  An email notification is triggered and sent to workplace reservation administrators and event planners for the updated reservation location.

    ![Email notification.](../image/wsd-email-notification.png)


**Parent Topic:**[Manage Workplace cases](../concept/manage-workplace-cases.md)

**Related topics**  


[View and track workplace cases](view-workplace-cases.md)

[View change event reservation case details](view-case-change-event-reservation.md)

