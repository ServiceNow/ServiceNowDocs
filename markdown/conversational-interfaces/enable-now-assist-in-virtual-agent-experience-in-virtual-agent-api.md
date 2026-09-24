---
title: Enable ServiceNow Otto in Virtual Agent API
description: Enable ServiceNow Otto in Virtual Agent API to support generative AI skills across multiple provider channels.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/enable-now-assist-in-virtual-agent-experience-in-virtual-agent-api.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Use, Virtual Agent API, Conversational Interfaces]
---

# Enable ServiceNow Otto in Virtual Agent API

Enable ServiceNow Otto in Virtual Agent API to support generative AI skills across multiple provider channels.

## Before you begin

Set up ServiceNow Otto for Virtual Agent. See [Assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/configure-now-assist-va.md) for more information.

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
|Active|Select the **Active** checkbox.|

5.  Select **Submit**.


