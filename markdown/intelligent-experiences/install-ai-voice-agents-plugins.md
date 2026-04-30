---
title: Install Now Assist AI voice agents
description: Install Now Assist AI voice agents on your ServiceNow instance to enable voice-based support through agentic AI experience.
locale: en-US
release: yokohama
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

AI voice agents aren’t standalone applications that you can install directly. To enable AI voice agents on your instance, you must install and activate Now Assist for Voice, which is the base application for platform AI voice agents. To enable ITSM and HR AI voice agents, you must install and activate Now Assist for IT Service Management \(ITSM\) and Now Assist for HR Service Delivery \(HRSD\) applications along with the corresponding voice plugins.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for the following plugins.

    -   Now Assist for Voice \(sn\_voice\_aia\) for enabling default Platform AI voice agents
    -   IT Service Management AI voice agent collection \(sn\_itsm\_voice\_aia\) for enabling default ITSM AI voice agents. See [Using the IT Service Management Now Assist Voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.
    -   HR Voice AI Agents \(sn\_hr\_voice\_aia\) for enabling default HRSD AI voice agents.
3.  Select **Install** to install each of the required plugins.


## Result

AI voice agents associated with the applications are installed on your instance.

