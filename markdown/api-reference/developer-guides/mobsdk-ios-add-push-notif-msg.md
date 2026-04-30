---
title: Add a push notification message
description: Configure the message displayed to users when they receive their push notification.
locale: en-US
release: yokohama
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up push notifications on your ServiceNow instance, Configure push notifications, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Add a push notification message

Configure the message displayed to users when they receive their push notification.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System Notification** &gt; **Push** &gt; **Push Messages**.

2.  Select **New**.

3.  In the Push Message form, fill in the following fields:

<table id="table_rhp_1wj_prb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the push notification message record. **Note:** This name is not visible in the notification, it is only a reference for use during configuration.

</td></tr><tr><td>

Push app

</td><td>

Mobile application to which you want to send the notification. This is the application that you added in "Add a push application record".

</td></tr><tr><td>

Push message

</td><td>

Push notification message content record created in "Add a push notification message content record".

</td></tr><tr><td>

Table

</td><td>

Table the message originates from. Select `Push Notification [sys_cs_message_notification]`.

</td></tr></tbody>
</table>4.  Select **Submit** to create the record.


