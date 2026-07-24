---
title: Create a survey module
description: You can create a module that opens a survey.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/t\_CreatingASurveyModule.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Survey distribution, Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a survey module

You can create a module that opens a survey.

## Before you begin

Role required: admin or survey\_admin

## About this task

When a user clicks a survey module, the system performs one of the following actions, depending on the configuration options for the survey and other factors.

-   Creates a new survey instance
-   Opens an existing survey instance
-   Displays an error message.

## Procedure

1.  Perform the appropriate action for your version of the UI:

    -   **Core UI**: Point to the application menu that contains the module to which you want to add the survey module and click the edit application \(pencil\) icon.
    -   **UI15**: Right-click the application menu you want to add the module to and select **Edit Application Menu**
2.  In the **Modules** related list, click **New**.

3.  Complete the following fields.

    -   **Link type**: Assessment

        Do not select **Survey**, which is used for legacy surveys only.

    -   **Assessment**: Select the survey you want the module to open.
4.  Complete and save the form.


**Parent Topic:**[Survey distribution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_SurveyDistribution.md)

**Related topics**  


[Email notifications for surveys]()

[Send survey invitations to users]()

[Define a recipients list for surveys]()

[Add a recipients list to a survey]()

[Embed a survey within the Outlook email client]()

[Enable localization for a survey]()

[Survey URLs]()

[Sharing surveys]()

[Configure a survey in the Connect chat support]()

