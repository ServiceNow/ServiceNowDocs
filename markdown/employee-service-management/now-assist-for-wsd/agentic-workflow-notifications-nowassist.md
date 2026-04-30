---
title: Review notifications in the Now Assist panel
description: Review notifications by AI agents in the Now Assist panel.
locale: en-US
release: yokohama
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2025-09-07"
reading_time_minutes: 5
keywords: [Now Assist panel]
breadcrumb: [Use, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Review notifications in the Now Assist panel

Review notifications by AI agents in the Now Assist panel.

## Before you begin

Workplace Event Planners can review the notifications and help AI agents take appropriate actions for blocking a space, moving any existing reservations to a new location, or for updating an existing reservation's date, time, or duration.

Role required: now\_assist\_panel\_role, sn\_wsd\_rsv.reservation\_planner, sn\_wsd\_case.case\_writer

## Procedure

1.  In your instance, select the Now Assist sparkle icon in the \(![Now Assist panel on the navigation menu bar showing sparkle icon with notifications.](../../workplace-case-mgmt/image/wsd-now-assist-sparkle-icon.png)\) navigation menu bar to open the Now Assist panel.

    Use the Now Assist conversational interface to receive notifications, case summarization, and resolution notes.

2.  To review the notifications by AI agents for an emergency maintenance request, select the Now Assist sparkle icon \(![Now Assist panel sparkle icon showing number of AI notifications.](../../workplace-case-mgmt/image/wsd-now-assist-sparkle-icon.png)\) in the navigation menu bar of your instance.

    AI agents notifies Workplace Event Planners about actions taken through case resolution and case summarization notes in the conversational interface. Select and open the notifications in the conversation interface to review the case summarization and resolution notes.

    For example, an emergency maintenance request is submitted and assigned to a user in the Workplace Event Planners assignment group. When an emergency meeting request is submitted, a workplace case task is created. For more information, see [Submit an emergency maintenance request](../../workplace-case-mgmt/task/submit-emergency-maint-request.md) and [View emergency maintenance case details](../../workplace-case-mgmt/task/view-emergency-maint-case.md).

    Workplace Event planners are notified by AI agents for blocking a location and moving an existing reservation from a blocked location to another. AI agents notifies the Workplace Event planner user using the Now Assist panel and performs the following activities in the conversational interface:

    -   Contacts the Workplace Event planner user and summarizes the issue.
    -   AI agent asks the Workplace Event Planner the duration for which the space should be blocked \(unavailable\) during the maintenance period.
    -   After receiving the confirmation, the AI agents creates a block location record in the sn\_wsd\_core\_block\_location table. The location is blocked or unavailable during the emergency maintenance period. It autonomously updates the existing reservation to a new location.

        ![AI agents confirming blocked locations for with Workplace Event Planners using the Now Assist panel.](../image/wsd-now-assist-blocked-reservation-successful.png)

    -   If there are no impacted reservations for a blocked location, AI agents inform the Workplace Event Planners that there are no impacted reservations for a blocked location.

        ![AI agents showing that there are no impacted reservations for a blocked location.](../image/wsd-block-a-location.png)

    -   If there are any existing reservations in the blocked location, AI agents lists the impacted reservation or reservations for Workplace Event Planners to review.
    -   AI agents asks the Workplace Event planners to confirm the impacted reservations.
    -   Workplace Event planners can confirm the location and help AI agents move the reservation or reservations to an available location.

        ![Now Assist panel showing notifications with case resolution notes for event planners to take appropriate measures.](../image/wsd-now-assist-move-reservation.png)

    -   If you want the reservation to be moved to a different location, enter your suggestion in the conversational interface. If the location is available, AI agents block the location for you.
    -   If AI agents cannot handle an impacted reservation, it provides a link to the Workplace Event planner to manually moving or updating the reservations. Workplace Event Planners can navigate to the reservation portal page and manually update or reschedule the reservations.

        ![AI agents providing a link to Workplace Event Planners to manually resolve a reservation.](../image/wsd-move-rsv-manually-now-assist-panel.png)

        **Note:** Multi-location reservations are not supported by AI agents.

    -   AI agents share case summarization and resolution notes with Workplace Event Planners.
    The emergency maintenance case activities are also added to the work notes of the emergency maintenance case. Workplace Event planners can review the work notes to understand the activities performed by AI agents. For more information, see [View emergency maintenance case details](../../workplace-case-mgmt/task/view-emergency-maint-case.md).

    Another example can be when a change event request is submitted by a workplace user. The change event request case is submitted to update an existing reservation's date, time, and duration. The change event request case is assigned to a user in the Workplace Event Planners assignment group. AI agentic workflow Help Manage workplace reservations is triggered when the case is assigned to a Workplace Event Planner.

    For more information, see [Submit a change event request for a reservation](../../workplace-case-mgmt/task/submit-change-event-reservation.md) and [View change event reservation case details](../../workplace-case-mgmt/task/view-case-change-event-reservation.md).

    Select and open the notifications in the conversation interface to review the case summarization and resolution notes.

    -   Workplace Event planners can review the notification and chat with the AI agent to answer queries for moving a reservation to another location.
    -   If the old location is available, AI agents move the reservation to the old location when updating an existing reservation's date, time, and duration.

        ![AI agents showing old location and asking for confirmation before updating a reservation.](../image/wsd-help-manage-reservation-old-location.png)

    -   If the old location is not available while updating a reservation, AI agents shows a new location and asks Workplace Event planners to confirm it. You can confirm the location or ask for a different location that you prefer.

        ![AI agent notifying Workplace Event planners after updating a reservation date, time, or duration.](../image/wsd-now-assist-panel-help-manage-reservations-a.png)

    -   AI agents then show 3 new available spaces for reservation. You can select any one of these. If you want a different location, AI agents provide a link for you to navigate to the reservation portal page and manually select the space that you want.

        ![AI agents showing three available locations to move an existing reservation to a new date, time, and duration.](../image/wsd-now-assist-panel-three-rsv-locations.png)

    -   AI agents then provide case resolution notes and summarization for Workplace Event planners to review.
    The team of AI agents updates an existing reservation with a new date, time, or duration. AI agents notifies Workplace Event Planners using the Now Assist panel conversational interface about the changed date and time for a reservation. If the old location is not available for reservation, AI agents move the reservation with updated date and time to a new location. For more information, see [Help manage workplace reservations agentic workflow](../concept/manage-workplace-reservations-agent-ai.md).


**Parent Topic:**[Using Now Assist for WSD](../concept/now-assist-wsd-using.md)

**Related topics**  


[Reserve a space using Now Assist in Virtual Agent](wsd-reserve-a-space-now-assist-va.md)

