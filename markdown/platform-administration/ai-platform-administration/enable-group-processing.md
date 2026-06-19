---
title: Enable email account group processing
description: Enable the email reader job to start processing your email account groups so that you can reduce the time it takes to process inbound email accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/enable-group-processing.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Multiple email readers, Email accounts, Create, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable email account group processing

Enable the email reader job to start processing your email account groups so that you can reduce the time it takes to process inbound email accounts.

## Before you begin

[Create email account groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/create-email-account-group.md).

Role required: admin

## Procedure

1.  [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md) with the following settings:

    -   Name: **glide.email.inbound.account\_group\_processing**
    -   Type: true \| false
    -   Value: **true**

## What to do next

Check the status of your email account groups to see if processing time has been reduced. For more information, see [Monitor email account groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/monitor-email-account-groups.md).

To further reduce processing time, consider creating another email reader job to process inbound email accounts. For more information, see [Create an email reader job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/create-email-reader-job.md).

