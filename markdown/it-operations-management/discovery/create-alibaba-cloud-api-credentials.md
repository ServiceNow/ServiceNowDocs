---
title: Create Alibaba Cloud API Credentials
description: Create Alibaba Cloud API credentials on the ServiceNow AI Platform to enable access to your Alibaba Cloud resources during Alibaba Cloud discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Discovery for Alibaba Cloud, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Create Alibaba Cloud API Credentials

Create Alibaba Cloud API credentials on the ServiceNow AI Platform to enable access to your Alibaba Cloud resources during Alibaba Cloud discovery.

## Before you begin

Verify that your Alibaba Cloud user has at least read-only access to all Alibaba Cloud services. For information on access permissions, consult your system administrator.

Retrieve the following properties from the Alibaba Cloud Console:

-   **AccessKey ID**
-   **AccessKey secret**

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Credentials**.

2.  Select **New**.

3.  Select **Alibaba Cloud API Credentials**.

4.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|Unique and descriptive name for the Alibaba Cloud credentials.|
    |Active|Option that makes the credential active.|
    |AccessKey ID|The AccessKey ID for your Alibaba Cloud account.|
    |AccessKey secret|The AccessKey secret used to authenticate and securely sign API requests for your Alibaba Cloud account.|

5.  Select **Submit**.


## What to do next

[Set up Alibaba Cloud service accounts](set-up-alibaba-cloud-service-account.md)

**Parent Topic:**[Discovery for Alibaba Cloud](../concept/alibaba-cloud-discovery.md)

