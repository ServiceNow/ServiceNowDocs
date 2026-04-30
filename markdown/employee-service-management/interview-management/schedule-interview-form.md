---
title: Schedule interview form
description: The schedule interview form provides the field descriptions required to schedule an interview with an applicant.
locale: en-US
release: zurich
product: Interview Management
classification: interview-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Interview Management, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Schedule interview form

The schedule interview form provides the field descriptions required to schedule an interview with an applicant.

<table id="table_uql_2p2_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Interview phase

</td><td>

Phase you're scheduling the interview for.**Note:**

-   You must have interview phase set up for the job requisition to be able to select this. For more information, see [Add interview phase](../task/add-interview-phase.md).
-   If you select an interview phase, the associated **Interview type**, **Duration**, **Format**, **Interviewers**, **Channel**, and **Interview title** are auto-populated.
-   You can leave this field blank to schedule ad-hoc interview rounds.

</td></tr><tr><td>

Interview type

</td><td>

Type of the interview. The available options are:-   **Screening**
-   **Technical**
-   **Managerial**
-   **Executive**
-   **Cultural fit**

**Note:** This field can be configured by updating the list in the Job Interview table \(sn\_ta\_hiring\_core\_job\_interview\).

</td></tr><tr><td>

Duration

</td><td>

Duration of the interview.**Note:** This field can be configured by updating the list in the Job Interview table \(sn\_ta\_hiring\_core\_job\_interview\).

</td></tr><tr><td>

Format

</td><td>

Format of the interview, whether it's a one-to-one or a panel round.

</td></tr><tr><td>

Applicant

</td><td>

This is automatically set to the name of the applicant on the application.

</td></tr><tr><td>

Interviewers

</td><td>

Name of the interviewers.**Note:**

-   You can only add interviewers that are part of the hiring team for the job requisition. To add additional interviewers to the interview, you must first add them to the hiring team.
-   If you have selected an interview phase, the interviewers specified in the **Interviewer roster** field are automatically added. If needed, you can also add interviewers from the list of **Additional interviewer roster** specified in the interview phase.

</td></tr><tr><td>

Channel

</td><td>

Mode of conducting the interview.**Note:**

-   This field can be configured by updating the list in the Job Interview table \(sn\_ta\_hiring\_core\_job\_interview\).
-   When an interview is scheduled with Zoom selected as the format:
    -   The recruiter is added as the host of the meeting.
    -   All the interviewers are added as alternate hosts of the meeting.

</td></tr><tr><td>

Time zone

</td><td>

Time zone in which the interview is scheduled.

</td></tr><tr><td>

Time slot selection type

</td><td>

Type of time slot selection. The available options are:-   **Select from preferences**: Displays the preferred time slots shared with recruiter.
-   **All time**: Displays all the time slots for selection.
-   **Available time**: Displays available time slots in your calendar. This option is available only if Microsoft Outlook integration is activated.
-   **Custom time slot**: Enables you to select a custom time slot.

</td></tr><tr><td>

Choose time slots

</td><td>

The time slots available for selection based on the selected **Time slot selection type**. **Important:**

-   If **Available time** is selected, all attendees must belong to the same Microsoft Outlook organization account to view their calendar availability. The calendar availability of external applicant is not tracked.
-   If **Available time** or **Select from preferences** is selected, a colored banner indicating the availability of attendees appears next to each slot. You can hover over the banner to see which attendees, if any, are unavailable at that time.
-   If **Custom time slot** is selected, then you can manually select the start time.

</td></tr><tr><td>

Selected time slots

</td><td>

Selected time slots. You can select up to three slots by default.**Note:**

-   If a time slot conflicts with any attendee's availability, a warning icon \(![time slot conflict](../images/ta_slot_conflict.png)\) appears next to the slot, and an alert message is displayed.
-   You can update the **maximum\_slots\_for\_interview\_scheduling** property to enable up to 10 slot selection.

</td></tr><tr><td>

Interview title

</td><td>

Title of the interview to be scheduled.

</td></tr><tr><td>

Select template

</td><td>

Predefined interview invite email template.For more information, see [Create interview invite email template](../task/create-interview-email-template.md).

</td></tr><tr><td>

Subject

</td><td>

Subject of the interview invite email.

</td></tr><tr><td>

Meeting invite

</td><td>

Body text of the interview invite email. It’s auto-generated if you have selected an email template and can be edited.

</td></tr></tbody>
</table>**Parent Topic:**[Interview Management reference](../concept/interview-management-reference.md)

