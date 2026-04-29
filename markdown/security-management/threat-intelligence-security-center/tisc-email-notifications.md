---
title: Email Notifications
description: Use email notifications to send selected users email notifications about specific tasks within the application, such as updates to observables/indicators/various other objects.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage email Notifications, Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Email Notifications

Use email notifications to send selected users email notifications about specific tasks within the application, such as updates to observables/indicators/various other objects.

Role required: admin

**Note:** As a System Administrator you can view, create or edit the email notification rule details in the classic view of the application.

Threat Intelligence Security Center provides rules driven email notifications which are sent to individual email addresses or a list of email addresses. Usually, Dissemination of Threat Intel information to internal users are sent typically in the form of an email. The process involves in delivering the threat intelligence data to users according to their specified format and time lines.

Email notifications allow administrators to specify:

-   When to send the notification
-   Who receives the notification
-   What content is in the notification

**Note:** If you want to make changes, then you need to configure whom the email should be sent by modifying the base system rules based on your requirements.

For more information, see [Create an email notification](https://servicenow.com/docs/bundle/washingtondc-platform-administration/page/administer/notification/task/t_CreateANotification.html) section on ServiceNow AI Platform administration documentation.

The following table details the email notification rules that are provisioned in the base system.

|Name|Table|
|----|-----|
|RSS Feeds with Zero Day mention|sn\_sec\_tisc\_rss\_feed|
|High Risk Malicious URL Observable|sn\_sec\_tisc\_url|
|High Risk Malicious IPV6 Observable|sn\_sec\_tisc\_ipv6\_address|
|Threat Reports with Zero Day mention|sn\_sec\_tisc\_threat\_report|
|High Risk Malicious IPV4 Observable|sn\_sec\_tisc\_ipv4\_address|
|High Risk Malicious SHA512 Observable|sn\_sec\_tisc\_sha512\_hash|
|High Risk Malicious Domain Observable|sn\_sec\_tisc\_domain\_name|
|Notifying on case updation|sn\_sec\_tisc\_case|

![email notifications](../image/tisc-email-notifications.png "Email Notifications")

**Note:** Clicking on each email notification will take you to the classic UI, so that you can take necessary actions such as viewing or editing or creating the notifications.

**Parent Topic:**[Manage email Notifications](tisc-notifications.md)

**Related topics**  


[Email logs](tisc-email-logs.md)

