---
title: Obtain and distribute a general survey URL
description: You can distribute a general survey URL to allow any eligible user to open a survey questionnaire.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Survey URLs, Survey distribution, Survey administration, Use, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Obtain and distribute a general survey URL

You can distribute a general survey URL to allow any eligible user to open a survey questionnaire.

## Before you begin

Role required: admin or survey\_admin

## About this task

The general URL is available on the Survey Definition form and on the survey creator. You can also email the URL for a public survey that is published.

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **View Surveys**.

2.  Open a survey definition from the Assessment Metric Types list.

3.  To view or copy the URL, click the **View Survey URL** related link.

    This related link is visible only if the survey definition is **Active**.

4.  To distribute the URL to users, paste the copied URL as desired, or click the **Email** button to send via email.

    The **Email** button is visible only for a public survey that is published.


## What to do next

When a survey user clicks the general survey URL, the system creates a survey instance for the survey user as long as the user does not have an instance in the **Ready to take** state. The system is configured by default to send an email notification when a survey instance is generated.

As a result, the survey user receives a second notification in addition to the notification that you sent with the general survey URL. This may confuse the survey user. To avoid this issue, you can deactivate auto-notification.

**Parent Topic:**[Survey URLs](../concept/c_SurveyURLs.md)

**Related topics**  


[Deactivate auto-notification for surveys](t_DeactivateAutoNotifyForSurveys.md)

[Obtain a survey instance URL](t_ObtainASurveyInstanceURL.md)

[Test a survey URL](t_TestTheSurveyURL.md)

