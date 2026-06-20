---
title: Enable basic email
description: Enable basic email to use ServiceNow - provided email servers and accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/t\_ConfiguringStandardEmail.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Basic email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable basic email

Enable basic email to use ServiceNow - provided email servers and accounts.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Email Properties**.

2.  Configure these email properties and select **Save**.

    \[Omitted image "email-properties.png"\] Alt text: Email properties

    |Property section|Label|System property|Setting required|
    |----------------|-----|---------------|----------------|
    |Outbound Email Configuration|Email sending enabled|glide.email.smtp.active|Yes|
    |Inbound Email Configuration|Email receiving enabled|glide.email.read.active|Yes|


**Parent Topic:**[Basic email setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/c_StandardEmailConfiguration.md)

