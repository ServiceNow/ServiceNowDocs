---
title: Schedule an interview
description: Schedule interview with applicants on a job requisition to get started with the interview journey.
locale: en-US
release: australia
product: Interview Management
classification: interview-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Interview Management, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Schedule an interview

Schedule interview with applicants on a job requisition to get started with the interview journey.

## Before you begin

Role required: sn\_ta\_hiring\_core.recruiter or sn\_ta\_hiring\_core.recruitment\_coordinator

You must activate the Interview Management plugin to have access to this functionality.

## About this task

As a recruiter, you can schedule interviews with applicants throughout their application journey states. These meetings can be screening rounds, interviews, or discussions to evaluate the applicant profile for the job.

## Procedure

1.  Navigate to **Workspaces** &gt; **Recruitment workspace**.

2.  Select the job requisition that you want to schedule an interview for.

3.  In the **Overview** tab, under the Applications section, select the applicant that you want to schedule an interview with.

4.  On the application record page, select **Schedule interview**.

    **Note:** If upgrading from an earlier version, make sure to edit and populate the **Hiring role**, **Visibility to applicant**, and **Type** fields of the hiring team members in the job requisition. For details, see [Edit hiring team members](../concept/manage-hiring-team.md#).

5.  On the Schedule interview form, fill in the fields.

    For a description of the field values, see [Schedule interview form](../reference/schedule-interview-form.md).

6.  Preview the draft invite and select **Send**.

    -   If you have selected multiple slots, an email invite is sent to the applicant to select a time slot to schedule the interview.
    -   If you have selected a single time slot, the interview is scheduled directly and the applicant receives an interview invite to reduce response time.
    -   If Microsoft Outlook integration is enabled, after an applicant picks a slot, an interview email invite is automatically sent to the hiring team and applicant. If not enabled, you must manually send an invite to the hiring team and applicant and move the state to Scheduled.
    -   If Zoom integration is enabled, and is selected as the interview channel, a Zoom meeting link will be included in the interview invite.
    -   If the interview is scheduled to happen within an hour, an interview feedback record per interviewer is created immediately. If scheduled later, feedback records are created an hour before the interview start time by default.

        **Note:** You can update the **sn\_ta\_hiring\_core.interviewFeedbackScheduleJobLength** property to change the default scheduled time to create feedback records.

7.  On the application record page, review the scheduled interview in the **Job interviews** tab.


## What to do next

You can also track your interviews from the List view. For more information, see [List view in Recruitment workspace](../concept/list-view-recruit-workspace.md).

**Parent Topic:**[Using Interview Management](../concept/using-interview-mgmnt.md)

