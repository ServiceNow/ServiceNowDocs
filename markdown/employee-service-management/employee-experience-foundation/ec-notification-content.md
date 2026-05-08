---
title: Notification content
description: Create email, push, and SMS notifications to send messages directly to your employees. Messages can also be sent as part of a campaign.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating employee communications, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Notification content

Create email, push, and SMS notifications to send messages directly to your employees. Messages can also be sent as part of a campaign.

## Getting started

To send email, push, or SMS notifications, perform the following tasks:

-   Activate the Notify \[com.snc.notify\] plugin: Activate Notify
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
</table>-   Configure notifications to work with an SMS service provider or configure a Twilio account. See Configure Notify with Twilio.
-   Create notification content. See [Create email, SMS, or push notification content](../task/ecpro-manage-notification-content.md).
-   Map SMS content to a campaign \(Content Experiences\). See [Create a campaign](../task/ecpro-manage-campaigns.md).
-   Schedule content \(Content Experiences\). See [Create a campaign](../task/ecpro-manage-campaigns.md), [Create content for a campaign](../task/ecpro-manage-content.md), or [Create campaign bundles/stages](../task/ecpro-manage-campaign-bundles.md), or [Scheduling the delivery of content](../task/ecpro-schedule-content.md).
-   Run scheduled jobs:
    -   Content Experiences: Send SMS Notifications: Responsible for sending SMS notifications for campaigns. Default value is to run every hour.
    -   Content Experiences: Update Campaign Audience: Reevaluates the audience for a campaign and removes employees that no longer satisfy the criteria.

        Adds users that match your defined criteria to the campaign. Users show up in the Campaign Targets related list for a campaign.

    -   Content Experiences: Add Non-Portal Campaign Content: Creates sn\_ca\_campaign\_item\_user\_records for sent emails. It does not send the email.
    -   Content Publishing: Send SMS notifications: Responsible for sending SMS notifications for Content Delivery. Default value is to run every hour.

For more information, see: Email and SMS notifications, Notify, and Numbers and number groups.

