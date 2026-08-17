---
title: Install AI voice agents
description: Install the required plugins to enable AI voice agents on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/install-ai-voice-agents-plugins.html
release: zurich
topic_type: task
last_updated: "2025-12-05"
reading_time_minutes: 1
breadcrumb: [Deploy AI voice agents, AI Agent Studio, Enable AI experiences]
---

# Install AI voice agents

Install the required plugins to enable AI voice agents on your ServiceNow instance.

## Before you begin

Role required: sn\_aia\_admin

## About this task

ServiceNow Otto for Voice Agents is the application that enables AI voice agents on your instance. It is included with ServiceNow Otto for Platform \(sn\_genai\_platform\), which is automatically installed with any of your ServiceNow Otto products, for example, ServiceNow Otto for IT Service Management \(ITSM\) and ServiceNow Otto for HR Service Delivery \(HRSD\).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for the following plugins.

    -   ServiceNow Otto for Platform \(sn\_genai\_platform\) for enabling default platform AI voice agents
    -   IT Service Management AI voice agent collection \(sn\_itsm\_voice\_aia\) for enabling default ITSM AI voice agents. See [Agentic AI in the Voice application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm-aiagents-voice.md) for more information.
    -   HR Voice AI Agents \(sn\_hr\_voice\_aia\) for enabling default HRSD AI voice agents. See [HR AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-hrsd-voice-ai-agents.md) for more information.
3.  Select **Install** to install each of the required plugins.


## Result

AI voice agents associated with the applications are installed on your instance.

