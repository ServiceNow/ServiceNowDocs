---
title: Activate the Care Team Operations AI Chat Assistant and agents
description: Activate the Care Team Operations AI Chat Assistant, its AI agents, and the Request care team assistance agentic workflow so that care team members can create cases conversationally.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-operations-core/hco-now-assist-activate-cto-assistant.html
release: brazil
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 1
breadcrumb: [Configure agentic workflows, Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Activate the Care Team Operations AI Chat Assistant and agents

Activate the Care Team Operations AI Chat Assistant, its AI agents, and the Request care team assistance agentic workflow so that care team members can create cases conversationally.

## Before you begin

Role required: admin

Complete [Install ServiceNow Otto for Care Team Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hco-now-assist-install.md) and [Enable ServiceNow Otto for AI Search for case intake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/hco-now-assist-enable-ai-search.md).

## About this task

The assistant, its AI agents, and the agentic workflow are installed inactive. Activate each one before care team members can use them.

## Procedure

1.  Navigate to **Assistant Designer** &gt; **Assistants** and open **Care Team Operations AI Chat Assistant**.

2.  Select **Edit** &gt; **Settings**, and then select **Activate**.

3.  Select **Display experiences** and ensure that **Care Team Portal** is in the **Portals** list.

4.  Navigate to **AI Agent Studio** &gt; **AI Agents** and open **Care team operations case intake AI agent**.

5.  In **Select channels and status** on the **Engage via Otto** tab, select **Care Team Operations AI Chat Assistant** as the assistant, and then select **Activate** to activate the agent.

6.  Repeat the previous two steps for **Care team operations case creation AI agent**.

7.  In **Care Team Operations AI Chat Assistant**, go to **Promoted Assets** and add **Request care team assistance** as a promoted asset.

8.  Select **Save**.


## Result

Care team members can use the Request care team assistance workflow in the Care Team Operations AI Chat Assistant to create care team cases.

**Note:** If Care Team Mobile is installed, the assistant is automatically added to Care Team Mobile. No additional mobile configuration is required.

## What to do next

[Activate the Care Team Operations Case Creation AI voice agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hco-now-assist-activate-voice-agent.md)

