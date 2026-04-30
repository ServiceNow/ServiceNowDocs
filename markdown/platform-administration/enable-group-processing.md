---
title: Enable email account group processing
description: Enable the email reader job to start processing your email account groups so that you can reduce the time it takes to process inbound email accounts.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Multiple email readers, Email accounts, Create, Email Administration, Notifications, Configure core features, Administer]
---

# Enable email account group processing

Enable the email reader job to start processing your email account groups so that you can reduce the time it takes to process inbound email accounts.

## Before you begin

[Create email account groups](create-email-account-group.md).

Role required: admin

## Procedure

1.  [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#) with the following settings:

    -   Name: **glide.email.inbound.account\_group\_processing**
    -   Type: true \| false
    -   Value: **true**

## What to do next

Check the status of your email account groups to see if processing time has been reduced. For more information, see [Monitor email account groups](monitor-email-account-groups.md).

To further reduce processing time, consider creating another email reader job to process inbound email accounts. For more information, see [Create an email reader job](create-email-reader-job.md).

