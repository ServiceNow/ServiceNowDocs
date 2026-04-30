---
title: Embed a survey within the Outlook email client
description: Embed an interactive survey in the email notification sent to a user. The user can answer the survey questions and submit the survey from the email client instead of opening the survey in a new browser tab.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Survey distribution, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Embed a survey within the Outlook email client

Embed an interactive survey in the email notification sent to a user. The user can answer the survey questions and submit the survey from the email client instead of opening the survey in a new browser tab.

## Before you begin

Role required: admin or survey\_admin

The Outlook Actionable Messages plugin \(sn\_ms\_oam\) should be activated.

**Note:**

-   The Outlook Actionable Messages \(OAM\) feature is not supported in all Microsoft mail products and versions. To verify whether your version of Outlook supports OAM, refer to the [Microsoft](https://docs.microsoft.com/en-us/outlook/actionable-messages/) website.
-   Actionable messages are supported only for emails sent from the @service-now.com email address. If you are sending an email from a customized email address, you should register as a new service in the [Microsoft](https://aka.ms/publishoam) website setting the scope as **Organization**. Specify the provider ID value in the **sn\_ms\_oam.outlookactionable.originator** property.
-   Actionable messages are based on the Sender Policy Framework \(SPF\)/DomainKeys Identified Mail \(DKIM\) validation for the email sender verification. If an email recipient receives email via an external provider, emails may not be rendered as adaptive cards.
-   You cannot customize the default actionable message templates.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  For the **Survey Invitation** notification, in the **What it will contain** tab, add the following script in the **Message** field in addition to the existing information.

    ```
    ${mail_script:include_survey_actionable} 
    ```

    This script includes the Outlook actionable message in the email notification sent to the user.

3.  Navigate to **Survey** &gt; **View Surveys**, and open a survey.

4.  To send an email notification to the survey user, select the **Send notifications** check box.

5.  Select the **Outlook Actionable Message** check box and save the survey.

    **Note:**

    -   The Image Scale type question is supported only if there is a single question in the survey.
    -   Template type question with image option is supported only if there is a single question in the survey.
    -   Date/Time type question is supported in web client of Outlook and not in desktop client as Microsoft doesn't support Date/Time for Outlook desktop client.
    -   Two duplicate choice display values should not be used as the internal value may not be submitted incorrectly.
    -   The answer for String type question can be validated based on the option selected in the Field Validation field. For example, if you select the option as email address, then the answer entered can only be in the email-id format. Answers in any other format will not be accepted.
    -   The version of Microsoft Outlook does not support the following question types to create an embedded survey:
        -   Attachment
        -   Reference
        -   Ranking
    -   Dependent questions are not supported.
    -   Signature is not supported.
    -   Mandatory questions are supported.
    In both the Platform UI and Survey Designer, a validation is run to ensure all survey questions are supported.

6.  Click **Assign Survey** and assign the survey to a user.

    An email notification with the embedded survey is sent to the user. The user can take the survey and submit it from the email client instead of opening the survey in a new browser tab.


**Parent Topic:**[Survey distribution](../concept/c_SurveyDistribution.md)

**Related topics**  


[Email notifications for surveys](../concept/email-notification-for-surveys.md)

[Send survey invitations to users](t_SendSurveyInvitationsToUsers.md)

[Define a recipients list for surveys](define-recipient-list.md)

[Add a recipients list to a survey](add-recipient-list-survey.md)

[Enable localization for a survey](enable-localization-survey.md)

[Survey URLs](../concept/c_SurveyURLs.md)

[Create a survey module](t_CreatingASurveyModule.md)

[Sharing surveys](../concept/c_SurveyInportAndExport.md)

[Configure a survey in the Connect chat support](take-survey-connect-chat.md)

