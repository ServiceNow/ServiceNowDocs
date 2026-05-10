---
title: Install Now Assist AI voice agents
description: Install Now Assist AI voice agents on your ServiceNow instance to enable voice-based support through agentic AI experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-12-05"
reading_time_minutes: 1
breadcrumb: [Deploy AI voice agents, Now Assist AI agents, Enable AI experiences]
---

# Install Now Assist AI voice agents

Install Now Assist AI voice agents on your ServiceNow instance to enable voice-based support through agentic AI experience.

## Before you begin

Role required: sn\_aia\_admin

## About this task

AI voice agents aren’t standalone applications that you can install directly. To enable AI voice agents on your instance, you must install and activate Now Assist for Platform \(sn\_genai\_platform\), which is the base application for platform AI voice agents. Now Assist for Platform is auto-installed with any of your Now Assist products, for example, Now Assist for IT Service Management \(ITSM\) and Now Assist for HR Service Delivery \(HRSD\).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for the following plugins.

    -   Now Assist for Platform \(sn\_genai\_platform\) for enabling default platform AI voice agents
    -   IT Service Management AI voice agent collection \(sn\_itsm\_voice\_aia\) for enabling default ITSM AI voice agents. See [Agentic AI in the Voice application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-voice.md) for more information.
    -   HR Voice AI Agents \(sn\_hr\_voice\_aia\) for enabling default HRSD AI voice agents. See [HR AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-voice-ai-agents.md) for more information.
3.  Select **Install** to install each of the required plugins.


## Result

AI voice agents associated with the applications are installed on your instance.

