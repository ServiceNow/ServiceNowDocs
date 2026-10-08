---
title: Enable additional chat features
description: Add chat features to your chat assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/additional-chat-features.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Create a chat assistant, View assistants, Assistants overview, Create assistants, Virtual Agent, Conversational Interfaces]
---

# Enable additional chat features

Add chat features to your chat assistant.

## Before you begin

See [Brand and personalize an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/brand-assistant.md).

Role required: virtual\_agent\_admin or admin

## About this task

By default, all chat features, except web search mode, are turned on.

**Note:** For ServiceNow Otto panel - Developer assistant, only response streaming is available.

## Procedure

1.  **Allow web search** to let users switch to search the web directly from chat, enhancing access to external info.

    **Note:** For premium chat, web search mode and web search fallback are dependent on one another. If web search mode is turned off, web search fallback is unavailable \(grayed out\). If web search mode is turned on, web search fallback is available, and can be turned on or off.

    \[Omitted image "sno-additional-chat.png"\] Alt text: Turn different chat features for your assistant on or off.

    Web search mode enables users to search the internet by selecting a globe icon within the chat window. The default web search provider, at the instance level, is Google Gemini.

    **Warning:**

    Certain API features that process data via third-party providers may route traffic to a data center outside of your region or location for these API features. See [KB2596322](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2596322) for a list of third-party APIs. Please consider your organization's data policies before using this feature.

    If the instance is self-hosted or regulated, the warning message won't be shown.

    To change the web search provider, select **Configure the API** to bring you to the Admin LLM model-selection page.

    -   If you want to use AWS Anthropic as the web search provider, switch the instance-level LLM to Claude.
    -   If the instance LLM is selected as Now LLM Service, Azure OpenAI, or Google Gemini, Gemini will still be the web search provider.
    -   If you want to use Perplexity AI or Azure OpenAI as the web search provider, you’ll need to perform a custom manual configuration. For more information, see [Manage model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/edit-model-providers.md).
    To change the LLM provider for ServiceNow Otto for Virtual Agent, select the AI agents skill group in AI Admin Hub. Navigate to **All** &gt; **AI Admin Hub** &gt; **Settings** &gt; **Manage AI models** &gt; **Manage model providers** &gt; **Edit model provider** &gt; **Customize**.

2.  **Allow response streaming** for LLM messages to stream as they are generated instead of appearing all at once.

    Response streaming is not supported on every display experience or when using Dynamic Translation. Streaming at the assistant level can be turned on regardless of whether Dynamic Translation is turned on or off. However, response streaming won't work when Dynamic Translation is turned on at the instance level.

    **Note:** Dynamic Translation can be turned off in the AI Admin Hub. Turning off Dynamic Translation impacts the entire instance.

    For more information, see [Chat streaming responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/streaming-responses-requestor.md).

3.  **Allow document uploads** so that users can ask questions about content or get a document summary.

    For more information on file formats for uploading files to an assistant, see [Upload documents in a chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/upload-documents-na-va.md).

    **Note:** If AI Guardian is turned on for the instance, **Allow document uploads** can't be turned on. When you create a new assistant, this option is turned on by default if AI Guardian is off, and turned off by default if AI Guardian is on.

4.  **Show closed chats** to allow users to view past chat history.

    Closed chat is only supported in the enhanced chat experience.

5.  **Prioritize AI agents during skills discovery** so that AI agents take priority over other assets, such as knowledge bases and Q&amp;A modules, when the assistant discovers skills.

    All assistants use agentic orchestration by default, so AI agent skills are always available for skills discovery. Selecting the **Prioritize AI agents during skills discovery** option gives AI agents priority over other assets for the assistant.

    For more information about agentic AI, see [Explore AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-ai-agents.md).

    **Note:** If you upgraded from an earlier release, this setting may already be enabled on your assistant. Upgrading the Now Assist in Virtual Agent plugin to version 23.0.6 or later automatically creates a configuration record that enables agentic orchestration. Verify your current assistant mode before proceeding. For guidance on what changes after an upgrade, see [Configuring agentic conversations in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/agentic-conversations-vad.md).


## What to do next

See [Manage an assistant chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/manage-assistant-chat-experience.md).

