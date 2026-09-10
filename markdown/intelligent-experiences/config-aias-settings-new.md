---
title: Configure AI Agent Studio settings
description: Configure general settings for AI Agent Studio and agentic AI assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/config-aias-settings-new.html
release: australia
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 2
keywords: [old ai agent studio, legacy ai agent studio, old aias, legacy aias]
breadcrumb: [Configure AI Agent Studio, AI Agent Studio, Enable AI experiences]
---

# Configure AI Agent Studio settings

Configure general settings for AI Agent Studio and agentic AI assets.

## Before you begin

Role required: sn\_aia.admin

## About this task

AI Agent Studio has multiple settings for your agentic AI assets and how they function within the ServiceNow AI ecosystem.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Settings**.

2.  [Enable AI Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-guardian-new.md).

    AI Guardian enables you to help protect against offensive content and prompt injection. You can choose whether to check for offensive content, or you can configure prompt injection detection in AI Admin Hub.

3.  [Set up long-term memory for agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/long-term-memory-aia-new.md).

    Long-term memory allows agentic AI assets to remember user preferences or facts from previous interactions and use these memories for more focused conversations.

4.  [Configure external AI agent discoverability and contextual data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/integrate-external-aia.md).

    You can use third-party integrations to connect ServiceNow to other agentic AI systems. From the **Settings** page, you can choose whether you want to discover external agents or have your ServiceNow AI agents discoverable by others. You can also configure memory and data access for external AI agents.

5.  [Manage Model Contextual Protocol \(MCP\) servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-mcp-client-on-ai-agent-studio.md).

    MCP servers can connect ServiceNow AI agents with external tools to perform additional tasks.

6.  [Select your large language model \(LLM\) provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/select-aia-llm-new.md).

    Choose which LLM model provider to use for all agentic AI assets on your instance.

    **Note:** Options for available LLM providers are configured with [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-landing.md).

7.  Select **View legacy AI Agent Studio** to access the previous iteration of the AI Agent Studio UI.


