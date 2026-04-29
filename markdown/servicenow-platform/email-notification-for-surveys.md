---
title: Email notifications for surveys
description: When an administrator creates a survey and assigns it to a user, an email notification is sent to the user. Selecting the survey link in the email notification redirects the user to the survey page, where the user can take the survey. This type of survey is called a non-triggered survey.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Survey distribution, Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Email notifications for surveys

When an administrator creates a survey and assigns it to a user, an email notification is sent to the user. Selecting the survey link in the email notification redirects the user to the survey page, where the user can take the survey. This type of survey is called a non-triggered survey.

Triggered surveys are the surveys that users get when the trigger condition is met. For a triggered survey, an event is inserted in the event queue. The event can be configured for specific teams to determine whether an [email notification](../task/t_ModifySurveyDefinitions.md) should be sent to users. If the event is configured to send an email notification, an automated email is sent when the trigger condition is met. For more information about configuring the trigger condition, see [Configure a trigger condition for a survey](../task/t_CreateATriggerCondition.md).

**Note:** You can include an embedded survey in the survey email notification by using the **Outlook Actionable Message** check box. After you select this check box and save the survey, a validation is run to verify that all survey questions are supported. This field is available only when the Outlook Actionable Messages \(sn\_ms\_oam\) plugin is installed. For more information, see [Outlook Actionable Messages](../../outlook-actionable-messages/concept/outlook-actionable-messages.md).

**Parent Topic:**[Survey distribution](c_SurveyDistribution.md)

**Related topics**  


[Send survey invitations to users](../task/t_SendSurveyInvitationsToUsers.md)

[Define a recipients list for surveys](../task/define-recipient-list.md)

[Add a recipients list to a survey](../task/add-recipient-list-survey.md)

[Embed a survey within the Outlook email client](../task/embed-survey-in-outlook-email.md)

[Enable localization for a survey](../task/enable-localization-survey.md)

[Survey URLs](c_SurveyURLs.md)

[Create a survey module](../task/t_CreatingASurveyModule.md)

[Sharing surveys](c_SurveyInportAndExport.md)

[Configure a survey in the Connect chat support](../task/take-survey-connect-chat.md)

