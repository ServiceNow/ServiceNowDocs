---
title: View a survey instance
description: A survey instance represents one questionnaire assigned to one user. You view an instance to verify that survey instances were created, to check the state of a survey instance, or to reassign a survey instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View a survey instance

A survey instance represents one questionnaire assigned to one user. You view an instance to verify that survey instances were created, to check the state of a survey instance, or to reassign a survey instance.

## Before you begin

Role required: admin or survey\_admin

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **Survey Instances**.

    The following sub-modules are available based on the state of the instances:

    -   **Ready to take**: Displays survey instances that are ready to be taken by the user. By default, these instances are sorted in ascending order by the **Number** field.
    -   **In progress**: Displays survey instances that are in progress. By default, these instances are sorted in ascending order by the **Number** field.
    -   **Completed**: Displays survey instances that are complete. By default, these instances are sorted in descending order by the **Taken on** field.
    -   **Cancelled**: Displays survey instances that are cancelled. By default, these instances are sorted in ascending order by the **Number** field.
    -   **All**: Displays survey instances in all states. By default, these instances are sorted in ascending order by the **Number** field.
2.  Open a survey instance from the required sub-module.

    By default, you can view the following fields in the [Survey Instance form](../reference/survey-instance-form.md) for all sub-modules other than **Completed**.

    -   **Number**
    -   **Metric type**
    -   **Due date**
    -   **State**
    -   **Assigned to**
    -   **Domain**
    -   **Expiration date**
    -   **View User's Response**
    -   **Retry Sentiment Analysis**
    -   **Assessment Instance Questions**
    **Note:**

    -   When you open an instance in the **Completed** sub-module, you are redirected to the User's Response page.
    -   Each survey instance is stored as a record on the Assessment Instance \[asmt\_assessment\_instance\] table with a modified view for survey use.

**Parent Topic:**[Survey administration](../reference/r_SurveyAdminTasks.md)

**Related topics**  


[View survey reports](view-survey-overview.md)

[Survey designer](../concept/c_SurveyDesigner.md)

[Survey users and groups](../concept/c_SurveyUsersAndGroups.md)

[Copy a survey](copy-survey.md)

[Publish a survey](t_PublishASurvey.md)

[Customize the appearance of a survey](t_CustomizingAppearance.md)

[Survey definitions](../concept/c_SurveyDefinitions.md)

[Create a survey designer template question](t_CreateASurveyDesignerTemplateQ.md)

[Survey questions](../concept/c_SurveyQuestion.md)

[Survey trigger conditions](../concept/c_TriggerConditions.md)

[Survey distribution](../concept/c_SurveyDistribution.md)

[Outlook Actionable Messages](../../outlook-actionable-messages/concept/outlook-actionable-messages.md)

[Sentiment analysis for surveys](../concept/sentiment-analysis.md)

[Surveys in Service Portal and the Now Mobile app](../concept/c_SurveyServicePortal.md)

[Surveys in ITSM Virtual Agent](../concept/survey-virtual-agent.md)

[Legacy survey migration](../concept/c_MigrateSurveys.md)

[Schedule periods](../concept/c_SchedulePeriods.md)

[Event scheduling](https://www.servicenow.com/docs/access?context=c_ScheduleEvents&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

