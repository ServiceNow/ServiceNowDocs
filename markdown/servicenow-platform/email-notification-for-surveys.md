---
title: Email notifications for surveys
description: When an administrator creates a survey and assigns it to a user, an email notification is sent to the user. Selecting the survey link in the email notification redirects the user to the survey page, where the user can take the survey. This type of survey is called a non-triggered survey.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/email-notification-for-surveys.html
release: australia
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Survey distribution, Survey administration, Use surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Email notifications for surveys

When an administrator creates a survey and assigns it to a user, an email notification is sent to the user. Selecting the survey link in the email notification redirects the user to the survey page, where the user can take the survey. This type of survey is called a non-triggered survey.

To configure the teams that must receive the notification, or modify the notification content, navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications** and open the **Survey Invitation** notification. For more information, see .

**Note:** You can include an embedded survey in the survey email notification by using the **Outlook Actionable Message** check box. After you select this check box and save the survey, a validation is run to verify that all survey questions are supported. This field is available only when the Outlook Actionable Messages \(sn\_ms\_oam\) plugin is installed. For more information, see [Outlook Actionable Messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/outlook-actionable-messages.md).

## Base system Survey Invitation notification

ServiceNow includes a pre-configured **Survey Invitation** notification for surveys. When a survey is assigned to a user and a non-triggered or triggered condition fires, this notification sends an email to the designated user. You don't need to create event or notification.

**Parent Topic:**[Survey distribution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_SurveyDistribution.md)

**Related topics**  


[Send survey invitations to users]()

[Define a recipients list for surveys]()

[Add a recipients list to a survey]()

[Embed a survey within the Outlook email client]()

[Enable localization for a survey]()

[Survey URLs]()

[Create a survey module]()

[Sharing surveys]()

[Configure a survey in the Connect chat support]()

