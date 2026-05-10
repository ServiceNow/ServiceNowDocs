---
title: Set up Alibaba Cloud service accounts
description: Create Alibaba Cloud infrastructure service accounts on the ServiceNow AI Platform to access your Alibaba Cloud account during Alibaba Cloud discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Discovery for Alibaba Cloud, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Set up Alibaba Cloud service accounts

Create Alibaba Cloud infrastructure service accounts on the ServiceNow AI Platform to access your Alibaba Cloud account during Alibaba Cloud discovery.

## Before you begin

Verify that Alibaba Cloud API credentials have been created. For more information, see [Create Alibaba Cloud API Credentials](create-alibaba-cloud-api-credentials.md).

Retrieve the **Account ID**, which can be found under **Root Account** or **RAM User** in the Alibaba Cloud Console. For more information, see the [Alibaba Cloud documentation](https://www.alibabacloud.com/help/en).

Role required: discovery\_admin

## Procedure

1.  In the navigation filter, enter `cmdb_ci_cloud_service_account.list`.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|A unique name for the Alibaba Cloud service account.|
    |Account Id|Compartment ID, which is the Alibaba Cloud Account Identifier of the compartment associated with this service account.|
    |Discovery Credentials|Name of credentials created for an Alibaba Cloud.|
    |Datacenter URL|URL of the datacenter.|
    |Datacenter Type|The Alibaba Cloud datacenter \[cmdb\_ci\_Alibaba\_datacenter\].|
    |Accessor account|Account name associated to the discovery credentials.|

4.  Select **Submit**.


## What to do next

Create a schedule for Alibaba Cloud in [Discovery](create-alibaba-cloud-discovery-schedule.md) or [Discovery Admin Workspace](create-alibaba-schedule-DAW.md).

**Parent Topic:**[Discovery for Alibaba Cloud](../concept/alibaba-cloud-discovery.md)

