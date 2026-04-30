---
title: Enable basic email
description: Enable basic email to use ServiceNow - provided email servers and accounts.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Basic email setup, Configure, Email Administration, Notifications, Configure core features, Administer]
---

# Enable basic email

Enable basic email to use ServiceNow - provided email servers and accounts.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Email Properties**.

2.  Configure these email properties and select **Save**.

    ![Email properties](../image/email-properties.png)

    |Property section|Label|System property|Setting required|
    |----------------|-----|---------------|----------------|
    |Outbound Email Configuration|Email sending enabled|glide.email.smtp.active|Yes|
    |Inbound Email Configuration|Email receiving enabled|glide.email.read.active|Yes|


**Parent Topic:**[Basic email setup](../concept/c_StandardEmailConfiguration.md)

