---
title: Create a survey module
description: You can create a module that opens a survey.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Survey distribution, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
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


**Parent Topic:**[Survey distribution](../concept/c_SurveyDistribution.md)

**Related topics**  


[Email notifications for surveys](../concept/email-notification-for-surveys.md)

[Send survey invitations to users](t_SendSurveyInvitationsToUsers.md)

[Define a recipients list for surveys](define-recipient-list.md)

[Add a recipients list to a survey](add-recipient-list-survey.md)

[Embed a survey within the Outlook email client](embed-survey-in-outlook-email.md)

[Enable localization for a survey](enable-localization-survey.md)

[Survey URLs](../concept/c_SurveyURLs.md)

[Sharing surveys](../concept/c_SurveyInportAndExport.md)

[Configure a survey in the Connect chat support](take-survey-connect-chat.md)

