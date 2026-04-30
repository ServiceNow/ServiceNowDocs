---
title: Configure a survey in the Connect chat support
description: Enable a user to take a survey after chatting with a support agent.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Survey distribution, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a survey in the Connect chat support

Enable a user to take a survey after chatting with a support agent.

## Before you begin

Role required: admin or survey\_admin

**Note:** The Connect Support plugin \(com.glide.connect.support\) should be activated.

## Procedure

1.  Navigate to **All** &gt; **Connect Support** &gt; **Support Administration** &gt; **Chat Survey**.

2.  Click **New**.

3.  In the Chat Survey form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Survey|Survey whose instance should be available in Connect Support.|
    |Type|Type of chat where the survey is available. Connect: Survey is available in Connect Support.|
    |Chat queue|Chat queue where the survey is available.|
    |Active|Specifies if the chat survey configuration is active.|
    |Description|Description of the chat survey configuration.|

4.  Click **Submit**.

    When a support agent of the assignment group associated with the chat queue ends a chat with a user, the survey instance is available in the chat window for the users.

    **Note:** The survey URL displayed after a connect chat is not a clickable link in the Virtual Agent chat widget. Copy and paste the URL to access the survey.


**Parent Topic:**[Survey distribution](../concept/c_SurveyDistribution.md)

**Related topics**  


[Email notifications for surveys](../concept/email-notification-for-surveys.md)

[Send survey invitations to users](t_SendSurveyInvitationsToUsers.md)

[Define a recipients list for surveys](define-recipient-list.md)

[Add a recipients list to a survey](add-recipient-list-survey.md)

[Embed a survey within the Outlook email client](embed-survey-in-outlook-email.md)

[Enable localization for a survey](enable-localization-survey.md)

[Survey URLs](../concept/c_SurveyURLs.md)

[Create a survey module](t_CreatingASurveyModule.md)

[Sharing surveys](../concept/c_SurveyInportAndExport.md)

[Monitor incoming Connect Support conversations](../../../use/collaboration/task/t_MonitorIncomingConnectSupport.md)

