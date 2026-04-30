---
title: Updating an On-Call schedule
description: Shift managers and members can use the Schedules tabs to view and update the on-call schedules of a group. Shift managers can review, manage, and resolve gaps or conflicts in your On-Call schedule from a single view.
locale: en-US
release: xanadu
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure or update an On-Call schedule, Manage schedules and shifts, On-Call Scheduling, IT Service Management]
---

# Updating an On-Call schedule

Shift managers and members can use the **Schedules** tabs to view and update the on-call schedules of a group. Shift managers can review, manage, and resolve gaps or conflicts in your On-Call schedule from a single view.

## Opening the Schedules page

To open and start working on a schedule, navigate to **On-Call Scheduling** &gt; **On-Call Schedules** and then click the card for the group.

Edit an on-call schedule

## Overview tab

This tab gives an overview of the current shift. The following sections are available:

-   **On-Call**: Displays information about the current on-call shift. From here, you can:
    -   Navigate to the previous and next shifts.
    -   View the roster and escalation details of the current shift. When you click **Roster and escalation details**, a dialog box displays the following tabs:
        -   Roster: Displays a list of all rosters along with its active on-call member. Information of the on-call member such as the contact number, email address, group, and the shift to which the user belongs to is also available.
        -   Escalation Path: Displays the escalation path defined for the shift.
        -   Profile: Displays the user profile of the primary on-call member. You can send a direct message to the on-call member by clicking **Send a direct message** or call the member if Notify WebRTC for on-call is set up. For more information on real-time messaging, see [Connect](https://www.servicenow.com/docs/access?context=c_Connect&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). For information on Notify webrtc, see [Forward to notify client workflow activity](https://www.servicenow.com/docs/access?context=r_WflowActivConnNotifClient&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). For information on the **Specify a valid Notify Number with voice capability** property that enables the Notify WebRTC for on-call, see [System properties for On-Call Scheduling](../reference/on-call-properties.md).
        -   Contact Preferences: The contact preferences set for the primary on-call member. ![On-Call Scheduling roster and escalation settings](../image/roster-escalation-settings.png)
-   **Pending Actions**: Displays the pending actions for the group’s on-call schedule. You can review gaps, conflicts, and time-off requests to find a replacement and ensure proper support coverage. For information on resolving the pending actions, see [Resolve gaps, conflicts, and time-off requests in a shift](resolv-gap-conflct-timeoff-oncall.md) and [Resolve gaps, conflicts, and time-off requests in a shift](resolv-gap-conflct-timeoff-oncall.md).

    **Note:** This section is displayed only for a shift manager.

-   **Your Upcoming Shifts**: Displays your upcoming shifts in a calendar view.

    **Note:** This section is displayed for a shift member or a Shift Manager who is a shift member.

-   **On-call calendar**: This section displays the calendar view of all shifts of the group. By default, the week view is displayed. For more information on on-call calendar, see [Manage shifts from the Calendar view](customize-calendar-view-oncall.md).

## Shifts tab

This tab displays all shifts defined for the user group. From here, you can edit a shift or create a custom escalation policy to override the default policy. For information on editing the escalation type, see [Create an escalation policy](create-custom-esc-policy-oncall.md).

You can also edit contact preferences from this tab. For more information on configuring a contact preference, see [Configure my availability and contact preferences](config-my-contact-prefs-oncall.md)

## Settings tab

This tab displays the group preferences set for your group's on-call shift. If not already set, click **Create Custom Group Settings** to set the group preferences. For more information about group preferences, see [Configure preferences for a user group](config-group-prefs-oncall.md).

**Note:** The group preferences set here affect only this group. These settings override the global settings.

To view on-call properties, click **View Global Settings**.

**Note:** **View Global Settings** is only visible to rota\_admin.

**Parent Topic:**[Configure or update an On-Call schedule](create-update-schedule-oncall.md)

