---
title: Enable SMS delivery with the email client
description: Give users the option to send an email client message as an SMS text message.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/r\_EnableTheSMSDeliveryOption.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Email client, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable SMS delivery with the email client

Give users the option to send an email client message as an SMS text message.

## Before you begin

Role required: admin

## Procedure

1.  In the application navigator, enter `sys_properties.list`.

2.  From the list, find and open the record for the **glide.email\_client.show\_sms\_option** property.

3.  On the form, change **Value** to **true**.

4.  Click **Update**.


## Result

In the email client, user can select to send the message as an SMS text message.

\[Omitted image "sms-delivery.png"\] Alt text: Email client SMS delivery

If the recipient doesn't have a registered SMS device, the email client sends the message to the primary email device.

**Parent Topic:**[Configure email client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configuring-email-client.md)

**Related topics**  


[Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md)

