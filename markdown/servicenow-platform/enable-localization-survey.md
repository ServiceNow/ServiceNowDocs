---
title: Enable localization for a survey
description: Enable a survey user to take a survey in multiple languages.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Survey distribution, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable localization for a survey

Enable a survey user to take a survey in multiple languages.

## Before you begin

Role required: admin or survey\_admin

The plugin for the language that you want the survey to be available in should be installed.

**Note:** Localization is applicable only for public surveys.

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **Administration** &gt; **Properties**.

2.  Enable the **Enable/Disable whether to show language picker when a public survey is taken** \(**show\_lang\_picker\_for\_publicsurveys**\) property.

3.  In the System Settings window, from the **Language** list, select the language that you want the survey to be available in.

    **Note:** The **Language** list is available only when a language plugin is installed.

4.  Navigate to **Survey** &gt; **View Surveys** and open a public survey.

5.  Enter the translated text for the survey title, questions, and answers.

6.  Save and publish the survey.

    **Note:** The localization is also applicable in Service Portal if the **Assessment Properties Allow survey link from email to open in service portal view \(applies only for surveys\)** \(**sn\_portal\_surveys.sp\_survey.email\_redirection**\) property is enabled.

    -   The survey is available for survey users in the translated language.
    -   Users can change the language of the survey using the language picker.

**Parent Topic:**[Survey distribution](../concept/c_SurveyDistribution.md)

**Related topics**  


[Email notifications for surveys](../concept/email-notification-for-surveys.md)

[Send survey invitations to users](t_SendSurveyInvitationsToUsers.md)

[Define a recipients list for surveys](define-recipient-list.md)

[Add a recipients list to a survey](add-recipient-list-survey.md)

[Embed a survey within the Outlook email client](embed-survey-in-outlook-email.md)

[Survey URLs](../concept/c_SurveyURLs.md)

[Create a survey module](t_CreatingASurveyModule.md)

[Sharing surveys](../concept/c_SurveyInportAndExport.md)

[Configure a survey in the Connect chat support](take-survey-connect-chat.md)

