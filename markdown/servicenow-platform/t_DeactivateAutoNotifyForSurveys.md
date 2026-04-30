---
title: Deactivate auto-notification for surveys
description: Deactivate an auto-notification to avoid a problem that causes a second system-generated email notification being sent to a user.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Survey URLs, Survey distribution, Survey administration, Use, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Deactivate auto-notification for surveys

Deactivate an auto-notification to avoid a problem that causes a second system-generated email notification being sent to a user.

## Before you begin

Role required: admin or survey\_admin

## About this task

When a survey is assigned to a user, an email notification containing a general survey URL is sent to the user. But sometimes, the user might receive a second system-generated notification.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Open the **Survey Invitation** notification.

3.  Configure the form to add the **Send to event creator** option to the Who will receive section.

    The **Send to event creator** option is selected by default.

4.  Clear the **Send to event creator** check box.

    The system no longer sends auto-notification messages to survey users.


**Parent Topic:**[Survey URLs](../concept/c_SurveyURLs.md)

**Related topics**  


[Obtain and distribute a general survey URL](t_ObtainAGeneralSurveyURL.md)

[Obtain a survey instance URL](t_ObtainASurveyInstanceURL.md)

[Test a survey URL](t_TestTheSurveyURL.md)

