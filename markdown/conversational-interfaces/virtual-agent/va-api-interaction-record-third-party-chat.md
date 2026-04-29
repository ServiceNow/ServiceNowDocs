---
title: Configure interaction record to store clientSessionId in Virtual Agent API
description: You can configure to store clientSessionId to support third-party chat applications.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Configure interaction record to store clientSessionId in Virtual Agent API

You can configure to store **clientSessionId** to support third-party chat applications.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_provider_application.list` in the filter.

2.  Select the **VA Bot to Bot Provider Application** record to open it.

3.  In the Provider Channel Identity form, select the **Provider Identity Properties** related list and click **New**.

4.  On the Custom Adapter Property form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the customer adapter property, such as `third_party_chat`.|
    |Value|Enter `true`.|
    |Description|Enter an explanation for this property: `The custom adapter property to contain the client sessions by the supported third-party application in the Interaction record.`|

5.  Click **Submit**.


**Parent Topic:**[Using Virtual Agent API](../concept/use-virtual-agent-api.md)

