---
title: Publish a survey
description: You must publish a survey to enable people to receive and complete survey instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/t\_PublishASurvey.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Publish a survey

You must publish a survey to enable people to receive and complete survey instances.

## Before you begin

Role required: admin or survey\_admin, survey\_creator

**Note:** Users with the survey\_creator role can publish a survey only if they own the survey. If they do not own the survey, they cannot publish it.

## About this task

The **State** field on the Survey Definition form indicates whether the survey is in the **Draft** or **Published** state.

**Note:** You cannot return a survey to the **Draft** state after it has been published. You do have the option to deactivate a survey by clearing the **Active** check box.

## Procedure

1.  Navigate to **Survey** **View Surveys** and select a survey to publish.

2.  Click **Publish**.

    When you publish a survey, the system generates survey instances for any associated survey users. You can [assign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_SendSurveyInvitationsToUsers.md) the survey to other users manually.


-   **[Publish a survey in the Survey Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_PublishASurveyInSurveyDesigner.md)**  
You must save changes to a survey before you can publish it to the specified recipients or groups.

**Parent Topic:**[Survey administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_SurveyAdminTasks.md)

**Related topics**  


[View survey reports]()

[Survey designer]()

[View a survey instance]()

[Survey users and groups]()

[Copy a survey]()

[Customize the appearance of a survey]()

[Survey definitions]()

[Create a survey designer template question]()

[Survey questions]()

[Survey trigger conditions]()

[Survey distribution]()

[Outlook Actionable Messages]()

[Sentiment analysis for surveys]()

[Surveys in Service Portal and the Now Mobile app]()

[Surveys in ITSM Virtual Agent]()

[Legacy survey migration]()

