---
title: Substitute yourself as an interviewer
description: Assign a substitute interviewer yourself, instead of relying on a recruiter or coordinator to assign one for you.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/interview-management/substitute-interviewer-self.html
release: australia
product: Interview Management
classification: interview-management
topic_type: task
last_updated: "2026-05-04"
reading_time_minutes: 2
keywords: [substitute interviewer, interview substitution, replace interviewer, interview invitation, recruiting coordinator]
breadcrumb: [Managing interviews as an interviewer, Use, Interview Management, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Substitute yourself as an interviewer

Assign a substitute interviewer yourself, instead of relying on a recruiter or coordinator to assign one for you.

## Before you begin

**Note:** You can substitute yourself until 5 minutes before the interview start time by default. An admin can update the **sn\_ta\_int\_mgmt.substitute\_cutoff\_minutes** property to change the default value.

Role required: sn\_ta\_hiring\_core.interviewer

## Procedure

1.  Open the interview invitation email you received from the recruitment team.

    If you're a hiring manager or recruiter, you can substitute yourself as an interviewer from the Employee Center portal or Recruitment workspace respectively.

2.  Select **Substitute myself**.

    You can also select this option from:

    -   The **Upcoming activities** section in the **Overview** tab on the application page.
    -   The **Interviews** tab on the application page.
    -   The interview record page.
3.  In the Substitute interviewer dialog box, select a substitute interviewer from one of the following tabs.

    -   **Roster**: The interviewers available from **Additional interviewer roster** defined during the interview phase setup.
    -   **Hiring team**: Interviewers who are part of the hiring team for this requisition.
    -   **Search**: A search field that lets you find any other eligible interviewer by name or title \(snc\_internal role\).
    If a tab has no interviewers to display, that tab is hidden.

4.  From the **Substitution reason** list, select the reason for requesting a substitute.

5.  In the **Message** field, enter a note to the substitute interviewer.

    Use this field to share context, handover details, or other relevant information the substitute should know before the interview.

6.  Select the **Stay informed about this interview** check box to continue receiving updates about this interview after the substitution is complete.

7.  Select **Confirm**.


## Result

After the substitution request is submitted:

-   A confirmation message is displayed and the interviewer is substituted.
-   An interview invite email is sent to the substitute interviewer. The original interviewer is copied on the email if they opted to stay informed.
-   The calendar of the original and substitute interviewer are updated accordingly.
-   A notification email about the interviewer substitution is sent to the recruiter, recruitment coordinator, hiring manager, and the interviewers associated with the interview. An admin can turn off this notification by setting the **sn\_ta\_int\_mgmt.notify\_hiring\_team\_on\_substitution** property to false.
-   The substitution details are recorded in the activity log of the interview record.
-   The substitute interviewer is added to the hiring team, if not already part of it.
-   The associated interview feedback task is reassigned to the substitute interviewer.

**Parent Topic:**[Managing interviews as an interviewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/interview-management/manage-interviews-interviewer.md)

