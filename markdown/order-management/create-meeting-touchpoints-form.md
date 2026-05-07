---
title: Create new meeting form
description: Field descriptions for editing or reviewing details on the Create New Meeting form for CRM Touchpoints.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activity Management reference, Lead and opportunity management, Reference, Sales Customer Relationship Management]
---

# Create new meeting form

Field descriptions for editing or reviewing details on the Create New Meeting form for CRM Touchpoints.

Field availability depends on the selected State and whether the Virtual meeting option is selected.

-   When State is set to Scheduled, the following fields become available: Invitees, Video software, Cadence, Location, Virtual meeting, and Meeting link.
-   When State is set to Completed or Canceled, the following fields become read-only: Meeting type, Video software, Cadence, Location, Virtual meeting, and Meeting link.
-   When State is set to Scheduled and Virtual meeting is unselected, Video software and Meeting link are unavailable.

<table id="table_rlq_mnl_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier for the meeting record, starting with the prefix CCMTG.

</td></tr><tr><td>

Source

</td><td>

This field is automatically set to the CRM touchpoint from which the meeting was created.

</td></tr><tr><td>

State

</td><td>

Current state of the meeting record. The available options are:-   Draft
-   Scheduled
-   Completed
-   Canceled

</td></tr><tr><td>

Meeting type

</td><td>

Type of meeting. The available options are:-   Ad-hoc
-   Weekly Status
-   QBR
-   Renewal

</td></tr><tr><td>

Video software

</td><td>

Video conferencing application used for the meeting.

</td></tr><tr><td>

Cadence

</td><td>

Frequency of the meeting. The available options are:-   Daily
-   Weekly
-   Biweekly
-   Monthly
-   Quarterly

</td></tr><tr><td>

Locations

</td><td>

Optional physical locations or conference rooms where the meeting takes place.

</td></tr><tr><td>

Virtual meeting

</td><td>

Option to indicate that the meeting is virtual rather than occurring in a physical location.

</td></tr><tr><td>

Meeting subject

</td><td>

Title or topic of the meeting.

</td></tr><tr><td>

Start date &amp; time

</td><td>

Date and time the meeting is scheduled to begin.

</td></tr><tr><td>

End date &amp; time

</td><td>

Date and time the meeting is scheduled to end.

</td></tr><tr><td>

Duration

</td><td>

Length of the meeting expressed in days, hours, minutes, and seconds. Automatically calculated based on the start and end date and time values when you save the meeting.

</td></tr><tr><td>

Invitees

</td><td>

People invited to the meeting.

</td></tr><tr><td>

Repeat until

</td><td>

End date for the recurring meeting series. This field is available only when a value is set in the **Cadence** field.

</td></tr><tr><td>

Meeting link

</td><td>

URL that enables participants to join a virtual video or audio meeting.

</td></tr><tr><td>

Agenda

</td><td>

Meeting agenda shared with the participants when the invite is sent. This field supports rich text formatting.

</td></tr><tr><td>

Customer notes

</td><td>

Notes or updates to share with the participants in an email. This field supports rich text formatting.

</td></tr><tr><td>

Internal notes

</td><td>

Post-meeting observations and follow-up actions for internal teams. This field supports rich text formatting.

</td></tr></tbody>
</table>**Parent Topic:**[Activity Management reference](../concept/activity-management-reference.md)

**Related topics**  


[Schedule a meeting from a touchpoint](../task/schedule-meeting-touchpoint.md)

