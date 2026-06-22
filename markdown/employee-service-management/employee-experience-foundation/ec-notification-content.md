---
title: Notification content
description: Create email, push, and SMS notifications to send messages directly to your employees. Messages can also be sent as part of a campaign.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/ec-notification-content.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating employee communications, Manage, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Notification content

Create email, push, and SMS notifications to send messages directly to your employees. Messages can also be sent as part of a campaign.

## Getting started

To send email, push, or SMS notifications, perform the following tasks:

-   Activate the Notify \[com.snc.notify\] plugin: [Activate Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/notify/t_ActivateNotify.md)
-   Ensure that the following system properties are configured:

<table id="table_xvj_bmb_h1c"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_ca.sms\_notification.max\_events

</td><td>

Determines the maximum number of campaign events to queue per job run for SMS. The default value is 50.

</td></tr><tr><td>

sn\_ca.sms\_notification.max\_users\_per\_event

</td><td>

Determines the maximum number of users to add per a campaign event for SMS. The default is 1,000.

</td></tr><tr><td>

sn\_cd.sms\_notification.max\_recipients

</td><td>

Determines the maximum number of users to add per Content Delivery notification for SMS. The default value is 50,000.

</td></tr><tr><td>

sn\_cd.sms\_notification.max\_users\_per\_event

</td><td>

Determines the maximum number of users to add for a Content Delivery event for SMS. The default value is 1,000.

</td></tr><tr><td>

glide.notify.sms.max\_concatenation

</td><td>

Notify supports the concept of SMS concatenation. The maximum length of a single SMS is 160 characters for plaintext or 70 characters for Unicode SMS messages. Up to 10 SMS messages are linked together when the maximum length is reached. This property configures the maximum number of SMS messages that are linked into one large SMS message. If the body length is exceeded the body truncates and a message logs. **Note:** The charges are per SMS, which means that 1600 character SMS is 10 times as expensive as a 160 character SMS. Also, not all providers support SMS concatenation.

</td></tr></tbody>
</table>-   Configure notifications to work with an SMS service provider or configure a Twilio account. See [Configure Notify with Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/notify/t_ConfigureNotifyWithTwilio.md).
-   Create notification content. See [Create email, SMS, or push notification content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/ecpro-manage-notification-content.md).
-   Map SMS content to a campaign \(Content Experiences\). See [Create a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/ecpro-manage-campaigns.md).
-   Schedule content \(Content Experiences\). See [Create a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/ecpro-manage-campaigns.md), [Create content for a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/ecpro-manage-content.md), or [Create campaign bundles/stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/ecpro-manage-campaign-bundles.md), or [Scheduling the delivery of content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/ecpro-schedule-content.md).
-   Run scheduled jobs:
    -   Content Experiences: Send SMS Notifications: Responsible for sending SMS notifications for campaigns. Default value is to run every hour.
    -   Content Experiences: Update Campaign Audience: Reevaluates the audience for a campaign and removes employees that no longer satisfy the criteria.

        Adds users that match your defined criteria to the campaign. Users show up in the Campaign Targets related list for a campaign.

    -   Content Experiences: Add Non-Portal Campaign Content: Creates sn\_ca\_campaign\_item\_user\_records for sent emails. It does not send the email.
    -   Content Publishing: Send SMS notifications: Responsible for sending SMS notifications for Content Delivery. Default value is to run every hour.

For more information, see: [Email and SMS notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/c_EmailNotifications.md), [Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/notify/notify-landing-page.md), and [Numbers and number groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/notify/c_NumberGroups.md).

