---
title: View On-Call schedules
description: The tiled grouping of on-call shift schedules helps you to review shifts rather than having to search through all shifts in the system.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Viewing schedules and request time-off, On-Call Scheduling, IT Service Management]
---

# View On-Call schedules

The tiled grouping of on-call shift schedules helps you to review shifts rather than having to search through all shifts in the system.

## Before you begin

Role required: itil, rota\_manager, or rota\_admin

## About this task

Each card on the On-Call Schedules page represents a shift and identifies the on-call members. A card displays the group name, the shift name, and rosters \(Primary and Secondary\).

On-Call schedules enable you to view the presence of on-call members. For more information on presence, see [User presence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_UserPresence.md).

**Note:** By default, on-call schedules are loaded in batches of 20. You can use the **com.snc.on\_call\_rotation.landing\_page.group\_limit** property update the setting. For details, see [System properties for On-Call Scheduling](../reference/on-call-properties.md).

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **On-Call Schedules**.

    **Note:** For a group with overlapping shifts, shift cards are displayed based on the escalation setting.

    The following tabs appear:

    -   **Pinned On-Call Schedules**: Displays a personalized list of who is on-call for the groups you are most interested in. Pin groups here for fast access.
    -   **My On-Call Schedules**: Displays only the On-Call schedules that you manage or are a member of.
    -   **All On-Call Schedules**: Displays the list of all groups that have active On-Call schedules. You can also find who is on-call for groups that you have not pinned.
    Use the filter to display On-call schedules by group, schedule, or username.

2.  In the **All On-Call Schedules** tab, pin a shift card by pointing to the card and clicking the Pin icon \(![Pin icon](../image/view-pin-icon.png)\).

    **Note:** When you pin a shift card of a group with overlapping shifts, all other shift cards of that group are also pinned.

3.  In the **Pinned On-Call Schedules** tab, unpin a shift card by clicking the Pin icon.

4.  To view details of a shift, click the shift card.

    **Note:** Each shift card displays only the first two rosters.

    If you are a shift manager or roster member, the schedule opens. For more information, see [Updating an On-Call schedule](update-schedule-oncall.md). In all other cases, you are redirected to the calendar view. For more information on on-call scheduling calendars, see [Manage shifts from the Calendar view](customize-calendar-view-oncall.md).

5.  To view roster and escalation details, click **Roster and escalation details** on the shift card.

    A dialog box displays the following tabs:

    -   Roster: Displays a list of all rosters and contact number, email address, group, and the shift for the active On-Call member.
    -   Escalation Path: Displays the escalation path defined for the shift.
    **Note:** By default, the details of the on-call member of the primary roster are displayed. Click **Send a direct message** to send a direct message to the on-call member. Alternatively, call the member if the Notify WebRTC is configured. For more information on real-time messaging, see [Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/connect/c_Connect.md). For information on Notify WebRTC, see [Forward call workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/r_WorkflowActivityForwardCall.md). For information on the **Specify a valid Notify Number with voice capability** property that enables the Notify WebRTC for on-call, see [System properties for On-Call Scheduling](../reference/on-call-properties.md).

6.  To view gaps and conflicts in a shift, click the info badge on the shift card.

    -   This is applicable only for group managers, shift managers, and delegated shift managers.
    -   This information is displayed based on the setting of the **com.snc.on\_call\_rotation.landing\_page.show\_pending\_actions** property. For more information, see [System properties for On-Call Scheduling](../reference/on-call-properties.md).

**Parent Topic:**[Viewing schedules and request time-off](../../user-administration/concept/viewing-schedules-and-escalation.md)

