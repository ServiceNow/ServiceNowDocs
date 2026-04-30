---
title: Enable Now Assist experience in Virtual Agent API
description: Enable Now Assist experience in Virtual Agent API to support generative AI skills across multiple provider channels.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Enable Now Assist experience in Virtual Agent API

Enable Now Assist experience in Virtual Agent API to support generative AI skills across multiple provider channels.

## Before you begin

Set up Now Assist in Virtual Agent. See [Configuring assistants overview](../../now-assist-in-va/task/configure-now-assist-va.md) for more information.

**Note:** Now Assist capabilities are supported only in asynchronous mode.

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_now_assist_deployment_channel.list` in the navigation filter.

2.  Select **New**.

3.  On the form, fill in the fields.

4.  |Field|Value|
|-----|-----|
|Document Table|Select Provider Channel Identity from the dropdown.|
|Document Id|Select the Provider Channel Identity \[sys\_cs\_provider\_application\] record corresponding to Virtual Agent API.|
|Now Assist Deployment|Select Now Assist for Virtual Agent.|
|Active|Select the **Active** check box.|

5.  Select **Submit**.


**Parent Topic:**[Using Virtual Agent API](../concept/use-virtual-agent-api.md)

