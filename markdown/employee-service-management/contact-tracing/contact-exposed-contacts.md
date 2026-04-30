---
title: Follow up with potentially exposed contacts
description: As a case task owner, contact potentially exposed users to follow up on their health status using the predefined instructions and survey questions.
locale: en-US
release: xanadu
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing cases to follow up with potentially exposed contacts, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Follow up with potentially exposed contacts

As a case task owner, contact potentially exposed users to follow up on their health status using the predefined instructions and survey questions.

## Before you begin

Role required: sn\_imt\_tracing.contact\_tracer

## About this task

The case manager defines instructions for contact tracers to use when following up with potentially exposed users, such as the follow-up frequency. Contact tracers should follow these instructions to work on the assigned tasks.

The Exposure Case Task Survey is available for contact tracers to use to assess the health status of the exposed contact. The administrator can review and modify the survey. For more information, see [Survey designer](https://www.servicenow.com/docs/access?context=c_SurveyDesignerElements&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Case Management** &gt; **Case Tasks**.

2.  Open a task from the list.

3.  To start work on a newly assigned task, click **Start Work**.

    The state of the case task updates to Work in Progress.

4.  Follow up with the potentially exposed contact specified in the **User** field in one of the following ways:

    -   Contact the user by calling or sending an email with the questions specified in the survey by clicking **Take Survey**.
    -   Send the survey via SMS for the user to respond via SMS by clicking **Send SMS Survey** if available.

        **Note:** You must have Virtual Agent installed and set up for use with SMS and Twilio to complete SMS outreach delivery. For more information on this feature, see [Virtual Agent conversations for Contact Tracing](../concept/contact-tracing-va-sms.md#).

    Each follow-up result is added to the Survey results related list.

    **Note:** These follow-up results can be viewed only by the contact tracer to whom the case task is assigned, the case manager, and the contact tracing admin.

5.  Update the final health status of the potentially exposed contact in the **Outcome** field when you complete the required number of follow-ups.

    -   If the potentially exposed contact reports positive symptoms of the disease, select **Infected**.
    -   If the potentially exposed contact reports normal, select **Cleared**.
    **Note:** An exposed contact’s health status and the **Outcome** field are updated when changes are made to either item. If there are multiple open case tasks for an exposed contact, the health status in all tasks will be updated to match the outcome of the most recently modified case task.

6.  Click **Close Task**.


## Result

The case task is closed. If notifications are enabled, the case manager is notified via an email.

## What to do next

The case manager can review the closed task and update the health status of the exposed user's as per the outcome value.

**Note:** The case manager can update the health status of an exposed contact only if there is no active case for the user.

If Employee Readiness Core is installed and the potentially exposed contacts requirement activated, the user's health and safety requirement status is also updated.

After all the case tasks in the case have been closed, the case manager can close the case.

**Parent Topic:**[Managing cases to follow up with potentially exposed contacts](../concept/exposure-case-management.md)

