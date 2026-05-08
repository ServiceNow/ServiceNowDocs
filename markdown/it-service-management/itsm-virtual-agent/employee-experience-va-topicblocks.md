---
title: Employee Experience topic blocks
description: ITSM Virtual Agent helps you manage meetings in Microsoft Exchange Online. Using the Manage Meetings EXO v1.0 topic, you can schedule, reschedule, and cancel a meeting.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Reusable ITSM Virtual Agent pre-built topic blocks, Using ITSM Virtual Agent pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Employee Experience topic blocks

ITSM Virtual Agent helps you manage meetings in Microsoft Exchange Online. Using the Manage Meetings EXO v1.0 topic, you can schedule, reschedule, and cancel a meeting.

Use the **Category** list on the Topics page in Virtual Agent Designer to sort by **Self Service** to view all Employee Experience topics blocks.

For detailed information about topic blocks, see Maximizing code reuse with topic blocks.

## Cancel Meeting EXO

Users can send a message to Virtual Agent requesting to cancel a meeting.

<table id="table_o52_2wr_dwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Input parameters

</td></tr><tr><td>

Start Date Time

</td><td>

Start date and time of the meeting in UTC.

</td></tr><tr><td>

End Date Time

</td><td>

End date and time of the meeting in UTC.

</td></tr><tr><td class="sub-head" colspan="2">

Output parameters

</td></tr><tr><td>

status

</td><td>

Returns a cancel status for the meeting.

</td></tr><tr><td>

status\_code

</td><td>

Returns one of the following status codes for the meeting:-   MEETING\_CANCELLED
-   TECHNICAL\_ISSUE
-   INFORMATION\_PROVIDED

</td></tr></tbody>
</table>## Conference Room Availability

Users can choose an available conference room for their meeting.

<table id="table_a1j_mwr_dwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Input parameters

</td></tr><tr><td>

Room Location

</td><td>

Location of the conference room.

</td></tr><tr><td>

Room Capacity

</td><td>

Number of people the conference room holds.

</td></tr><tr><td>

Start Date Time

</td><td>

Start date and time of the meeting in UTC.

</td></tr><tr><td>

Duration

</td><td>

Duration of the meeting in minutes. Values increment by 15 minute segments, from **15** to **1440** \(1 day\).

</td></tr><tr><td class="sub-head" colspan="2">

Output parameters

</td></tr><tr><td>

selected\_room\_info

</td><td>

Name of the selected conference room.

</td></tr><tr><td>

booking\_info

</td><td>

JSON string denoting additional booking information \(location, start time, and duration of meeting\).

</td></tr><tr><td>

status

</td><td>

Returns the status for the meeting.

</td></tr><tr><td>

status\_code

</td><td>

Returns one of the following status codes for the meeting:-   NO\_EMAIL\_FOUND
-   TECHNICAL\_ISSUE
-   INVALID\_SCHEDULE\_INFO
-   INVALID\_EMAIL
-   NO\_ROOMS\_AVAILABLE
-   ROOMS\_SELECTED
-   ROOMS\_VIEWED

</td></tr></tbody>
</table>## Get MS Teams Meeting Link

If the Microsoft Teams Communication spoke \(sn\_msteams\_com\_spk\) is installed on the instance, users can send a Microsoft Teams meeting link with their invitation.

|Name|Description|
|----|-----------|
|Input parameters|
|email\_id|Email address of the meeting organizer.|
|meeting\_subject|Subject of the meeting.|
|silent\_mode|Determines whether the topic block produces a message output. When the value is **true**, the topic block doesn't produce an output message.|
|service\_user\_azure|Service account Azure ID for the user. This will be used to initiate the meeting in Microsoft Teams meetings. Use a script variable to pass the user ID.|
|Output parameters|
|url|Microsoft Teams meeting URL.|
|meeting\_id|Microsoft Teams meeting ID.|
|output\_status|Indicates whether the action was successfully completed.|
|output\_error\_message|Error message indicating that the meeting link didn't get generated.|

## Reschedule a Meeting EXO

Users can send a message to Virtual Agent requesting to reschedule a meeting, or the user can select the desired template and select **Reschedule Meeting**.

<table id="table_o1n_gxr_dwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Input parameters

</td></tr><tr><td>

Start Date Time

</td><td>

Current start date and time of the meeting in UTC.

</td></tr><tr><td>

End Date Time

</td><td>

Current end date and time of the meeting in UTC.

</td></tr><tr><td>

Rescheduled Date

</td><td>

New date and time of the meeting in UTC.

</td></tr><tr><td>

Duration

</td><td>

Duration of the meeting in minutes. Values increment by 15 minute segments, from **15** to **1440** \(1 day\).

</td></tr><tr><td class="sub-head" colspan="2">

Output parameters

</td></tr><tr><td>

status

</td><td>

Returns a rescheduled status for the meeting.

</td></tr><tr><td>

status\_code

</td><td>

Returns one of the following status codes for the meeting:-   MEETING\_RESCHEDULED
-   TECHNICAL\_ISSUE
-   INFORMATION\_PROVIDED

</td></tr></tbody>
</table>## Schedule a Meeting EXO

Users can send a message to Virtual Agent requesting to schedule a meeting, or the user can select the desired template and select **Set up meeting**.

<table id="table_ojs_q5r_dwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Input parameters

</td></tr><tr><td>

Attendees

</td><td>

Email addresses of the people invited to the meeting. Multiple attendee email addresses are separated by a comma.

</td></tr><tr><td>

Subject

</td><td>

Subject of the meeting.

</td></tr><tr><td>

Meeting Date

</td><td>

Start date of the meeting in the user's time zone.

</td></tr><tr><td>

Meeting Time

</td><td>

Time of day for the meeting in minutes.For example, for 11:26 pm, the value is **1406**.

</td></tr><tr><td>

Duration

</td><td>

Duration of the meeting in minutes. Values increment by 15 minute segments, from **15** to **1440** \(1 day\).

</td></tr><tr><td>

Resource Type

</td><td>

Resources required for the meeting. Values include:-   **Virtual**: Requires conferencing software, such as Zoom.
-   **Conference**: Requires a room to be booked.
-   **Hybrid**: Requires both conferencing software and a room.
-   **None**: No additional resources required.

</td></tr><tr><td>

Meeting Application

</td><td>

Conferencing software tool for the meeting. Values include:-   **Teams**
-   **Webex**
-   **Zoom**
-   **None**

</td></tr><tr><td>

Body

</td><td>

Meeting agenda.

</td></tr><tr><td>

Service User Azure ID

</td><td>

Service account Azure ID for the user in Microsoft Teams meetings.

</td></tr><tr><td class="sub-head" colspan="2">

Output parameters

</td></tr><tr><td>

event\_id

</td><td>

ID for the scheduled meeting.

</td></tr><tr><td>

status

</td><td>

Returns the status for the meeting.

</td></tr><tr><td>

status\_code

</td><td>

Returns one of the following status codes for the meeting:-   MEETING\_SCHEDULED
-   TECHNICAL\_ISSUE
-   NO\_MEETING\_SELECTED

</td></tr></tbody>
</table>## Webex Meeting Actions

If the Cisco Webex Teams spoke \(sn\_cisco\_teams\_spk\) is installed on the instance, users can send a Webex meeting link with their invitation.

<table id="table_im4_pxr_dwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Input parameters

</td></tr><tr><td>

Action

</td><td>

The Webex action for the meeting. Values include:-   **Schedule**
-   **Reschedule**
-   **Cancel**

</td></tr><tr><td>

Start Date Time

</td><td>

Current start date and time of the meeting in UTC.

</td></tr><tr><td>

Duration

</td><td>

Duration of the meeting in minutes. Values increment by 15 minute segments, from **15** to **1440** \(1 day\).

</td></tr><tr><td>

User ID

</td><td>

Email address or user ID of the meeting organizer.

</td></tr><tr><td>

Meeting subject

</td><td>

Subject of the meeting.

</td></tr><tr><td>

Agenda

</td><td>

Meeting agenda.

</td></tr><tr><td>

Meeting URL

</td><td>

Join URL for the virtual meeting.

</td></tr><tr><td>

Meeting Invitees

</td><td>

Email addresses of the invited users, separated by commas.

</td></tr><tr><td class="sub-head" colspan="2">

Output parameters

</td></tr><tr><td>

meeting\_url

</td><td>

Join URL for the virtual meeting.

</td></tr><tr><td>

output\_status

</td><td>

Returns the status for the meeting.

</td></tr><tr><td>

status\_code

</td><td>

Returns one of the following status codes for the meeting:-   SCHEDULE\_ACTION\_SUCCESSFUL
-   RESCHEDULE\_ACTION\_SUCCESSFUL
-   CANCEL\_ACTION\_SUCCESSFUL
-   SCHEDULE\_ACTION\_FAILED
-   RESCHEDULE\_ACTION\_FAILED
-   CANCEL\_ACTION\_FAILED
-   INVALID\_PAYLOAD
-   INVALID\_EMAIL
-   MEETING\_ID\_MISSING

</td></tr></tbody>
</table>## Zoom Meeting Actions

If the Zoom spoke\(com.sn.zoom.spoke\) is installed on the instance, users can send a Zoom meeting link with their invitation.

<table id="table_zsx_qxr_dwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Input parameters

</td></tr><tr><td>

Action

</td><td>

Zoom action for the meeting. Values are:-   Schedule
-   Reschedule
-   Cancel

</td></tr><tr><td>

User ID

</td><td>

Account user's ID or email address.

</td></tr><tr><td>

Start date time

</td><td>

Current start date and time of the meeting in UTC.

</td></tr><tr><td>

Duration

</td><td>

Duration of the meeting in minutes. Values increment by 15 minute segments, from **15** to **1440** \(1 day\).

</td></tr><tr><td>

Meeting subject

</td><td>

Subject of the meeting.

</td></tr><tr><td>

Agenda

</td><td>

Meeting agenda.

</td></tr><tr><td>

Meeting ID

</td><td>

Unique Zoom ID assigned to the virtual meeting.

</td></tr><tr><td class="sub-head" colspan="2">

Output parameters

</td></tr><tr><td>

output\_status

</td><td>

Returns the status for the meeting.

</td></tr><tr><td>

status\_code

</td><td>

Returns one of the following status codes for the meeting:-   SCHEDULE\_ACTION\_SUCCESSFUL
-   RESCHEDULE\_ACTION\_SUCCESSFUL
-   CANCEL\_ACTION\_SUCCESSFUL
-   SCHEDULE\_ACTION\_FAILED
-   RESCHEDULE\_ACTION\_FAILED
-   CANCEL\_ACTION\_FAILED
-   INVALID\_PAYLOAD
-   INVALID\_EMAIL
-   MEETING\_ID\_MISSING

</td></tr><tr><td>

meeting\_url

</td><td>

Join URL for the virtual meeting.

</td></tr></tbody>
</table>**Parent Topic:**[Reusable ITSM Virtual Agent pre-built topic blocks](itsm-va-topic-blocks.md)

