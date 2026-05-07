---
title: Enable additional chat features
description: Add chat features to your chat assistant.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 3
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Enable additional chat features

Add chat features to your chat assistant.

## Before you begin

See [Brand an assistant](brand-assistant.md).

Role required: virtual\_agent\_admin or admin

## About this task

By default, all chat features, except web search mode, are turned on.

**Note:** For Now Assist panel - Developer assistant, only response streaming is available.

## Procedure

1.  **Allow web search** to let users switch to search the web directly from chat, enhancing access to external info.

    **Note:** For premium chat, web search mode and web search fallback are dependent on one another. If web search mode is turned off, web search fallback is unavailable \(grayed out\). If web search mode is turned on, web search fallback is available, and can be turned on or off.

    ![Turn different chat features for your assistant on or off.](../image/NAinVA-chat-features-0426.png "Additional chat features")

    Web search mode enables users to search the internet by selecting a globe icon within the chat window. The default web search provider, at the instance level, is Google Gemini.

    **Warning:**

    Certain API features that process data via third-party providers may route traffic to a data center outside of your region or location for these API features. See [KB2596322](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2596322) for a list of third-party APIs. Please consider your organization's data policies before using this feature.

    If the instance is self-hosted or regulated, the warning message won't be shown.

    To change the web search provider, select **Configure the API** to bring you to the Now Assist Admin LLM model-selection page.

    -   If you want to use AWS Anthropic as the web search provider, switch the instance-level LLM to Claude.
    -   If the instance LLM is selected as Now LLM Service, Azure OpenAI, or Google Gemini, Gemini will still be the web search provider.
    -   If you want to use Perplexity AI or Azure OpenAI as the web search provider, you’ll need to perform a custom manual configuration. For more information, see [Manage model providers](https://www.servicenow.com/docs/access?context=edit-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
    To change the LLM provider for Now Assist in Virtual Agent, select the AI agents skill group in Now Assist Admin console. Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings** &gt; **Manage AI models** &gt; **Manage model providers** &gt; **Edit model provider** &gt; **Customize**.

2.  **Allow response streaming** for LLM messages to stream as they are generated instead of appearing all at once.

    Response streaming is not supported on every display experience or when using Dynamic Translation. Streaming at the assistant level can be turned on regardless of whether Dynamic Translation is turned on or off. However, response streaming won't work when Dynamic Translation is turned on at the instance level.

    **Note:** Dynamic Translation can be turned off in the Now Assist Admin console. Turning off Dynamic Translation impacts the entire instance.

    For more information, see [Chat streaming responses](../../virtual-agent/concept/streaming-responses-requestor.md).

3.  **Allow document uploads** so that users can ask questions about content or get a document summary.

    For more information on file formats for uploading files to an assistant, see [Upload documents in a chat](upload-documents-na-va.md).

4.  **Show closed chats** to allow users to view past chat history.

    Closed chat is only supported in the enhanced chat experience.

5.  **Allow voice input** so that users can speak to their assistant instead of typing.

    Voice input is only available for Now Assist panel - Platform \(default\) assistant. For more information about voice input, see [Standard chat](https://www.servicenow.com/docs/access?context=now-assist-panel-standard&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US), [Enhanced chat](https://www.servicenow.com/docs/access?context=now-assist-panel-enhanced&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).


## What to do next

See [Manage an assistant chat experience](manage-assistant-chat-experience.md).

