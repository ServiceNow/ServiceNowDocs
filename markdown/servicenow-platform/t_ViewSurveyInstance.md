---
title: View a survey instance
description: A survey instance represents one questionnaire assigned to one user. You view an instance to verify that survey instances were created, to check the state of a survey instance, or to reassign a survey instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/t\_ViewSurveyInstance.html
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

    By default, you can view the following fields in the [Survey Instance form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/survey-instance-form.md) for all sub-modules other than **Completed**.

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

**Parent Topic:**[Survey administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_SurveyAdminTasks.md)

**Related topics**  


[View survey reports]()

[Survey designer]()

[Survey users and groups]()

[Copy a survey]()

[Publish a survey]()

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

[Schedule periods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_SchedulePeriods.md)

[Event scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ScheduleEvents.md)

