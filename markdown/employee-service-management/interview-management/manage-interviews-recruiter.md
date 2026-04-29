---
title: Manage interviews
description: Manage interviews as a recruiter or recruitment coordinator. Update interviews as needed.
locale: en-US
release: australia
product: Interview Management
classification: interview-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Interview Management, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Manage interviews

Manage interviews as a recruiter or recruitment coordinator. Update interviews as needed.

## Before you begin

Role required: sn\_ta\_hiring\_core.recruiter or sn\_ta\_hiring\_core.recruitment\_coordinator

You must activate the Interview Management plugin to have access to this functionality.

## Procedure

1.  Navigate to **Workspaces** &gt; **Recruitment workspace**.

2.  Select the job requisition that you want to manage an interview for.

3.  In the **Overview** tab, under the Applications section, select the required applicant with whom the interview is scheduled.

4.  On the application record page, select the **Job interviews** tab.

5.  Select the required interview record.

6.  From the interview record page, perform any of the following actions.

<table id="choicetable_j1m_phc_bdc"><thead><tr><th align="left" id="d501100e104">

Option

</th><th align="left" id="d501100e107">

Action

</th></tr></thead><tbody><tr><td id="d501100e113">

**Update the state**

</td><td>

On the **Details** tab, update the **State** field.

</td></tr><tr><td id="d501100e128">

**View the attendee details**

</td><td>

On the **Attendees** tab, view the attendee details such as name, role, acceptance status, job title, and type.

</td></tr><tr><td id="d501100e140">

**View the interview feedback details**

</td><td>

On the **Feedback** tab, view the feedback details such as number, state, rating, review comments, interviewer, and interview type.

</td></tr><tr><td id="d501100e152">

**Add a feedback record manually, when an interview has happened off the system**

</td><td>

On the **Feedback** tab, select **Add feedback** and then select the **Interviewer**.**Note:**

-   If a feedback record in incomplete/complete state is already assigned to an interviewer, a new record can’t be created for the same interviewer.
-   The due date on the feedback record created is set as seven days from the interview start date by default. An admin can update the **sn\_ta\_hiring\_core.due\_date\_for\_interview\_feedback** property to change the default value.


</td></tr><tr><td id="d501100e185">

**Send reminder to interviewer to submit feedback**

</td><td>

From the **Feedback** tab, open the feedback record and select **Send reminder**.**Note:** Feedback reminders are also configured to be sent automatically for one week \(on alternate days\) from the feedback creation date, by default. This default value can be updated using the **sn\_ta\_hiring\_core.due\_date\_for\_interview\_feedback** property.

</td></tr><tr><td id="d501100e205">

**Provide interview feedback**

</td><td>

From the **Feedback** tab:-   To provide interview feedback, open the feedback record assigned to you and enter the details, and then select **Submit feedback**. For more information, see [Provide interview feedback](provide-interview-feedback-recruiter.md).
-   To edit a feedback submitted by you, open the feedback record and then select **Edit feedback**.
-   To indicate that an interview assigned to you didn't happen, open the feedback record and select **Interview incomplete** to enter the corresponding reason and comments.


</td></tr><tr><td id="d501100e244">

**Reschedule an interview**

</td><td>

1.  Select **Reschedule**.
2.  Select a **Reschedule reason** and enter corresponding **Notes**.

**Note:** The options available in the **Reschedule reason** field can be customized by an admin.

3.  Select **Proceed**.
4.  On the Reschedule interview form, fill in the fields.

For a description of the field values, see [Schedule interview form](../reference/schedule-interview-form.md).

 **Note:** The reschedule count of an interview, and the reason and notes entered during rescheduling are saved in the activity stream of the interview record.

</td></tr><tr><td id="d501100e297">

**Complete an interview**

</td><td>

Select **Mark as complete**.

</td></tr><tr><td id="d501100e309">

**Mark an interview as no show**

</td><td>

From the Mark as complete list, select **No show**.

</td></tr><tr><td id="d501100e321">

**Cancel an interview**

</td><td>

From the Mark as complete list, select **Cancel interview**.

</td></tr></tbody>
</table>
**Parent Topic:**[Using Interview Management](../concept/using-interview-mgmnt.md)

