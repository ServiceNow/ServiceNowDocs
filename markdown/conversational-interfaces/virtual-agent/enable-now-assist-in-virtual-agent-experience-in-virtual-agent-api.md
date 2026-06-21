---
title: Enable Now Assist experience in Virtual Agent API
description: Enable Now Assist experience in Virtual Agent API to support generative AI skills across multiple provider channels.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/conversational-interfaces/virtual-agent/enable-now-assist-in-virtual-agent-experience-in-virtual-agent-api.html
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Virtual Agent API, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Enable Now Assist experience in Virtual Agent API

Enable Now Assist experience in Virtual Agent API to support generative AI skills across multiple provider channels.

## Before you begin

Set up Now Assist in Virtual Agent. See [Configuring Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md) for more information.

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_now_assist_deployment_channel.list` in the navigation filter.

2.  Click **New**.

3.  On the form, fill in the fields.

4.  |Field|Value|
|-----|-----|
|Document Table|Select Provider Channel Identity from the dropdown.|
|Document Id|Select the Provider Channel Identity \[sys\_cs\_provider\_application\] record corresponding to Virtual Agent API.|
|Now Assist Deployment|Select Now Assist for Virtual Agent.|
|Active|Select the **Active** checkbox.|

5.  Click **Submit**.


**Parent Topic:**[Using Virtual Agent API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/conversational-interfaces/virtual-agent/virtual-agent-api.md)

