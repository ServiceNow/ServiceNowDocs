---
title: Chat streaming responses
description: Synthesized responses stream in real time for Now Assist LLM chat conversations instead of waiting for the entire message to render. Streaming enables responses from the LLM to be sent immediately to help improve performance when replying to requests.
locale: en-US
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Using, Now Assist, Virtual Agent, AI Search, Streaming, genius results, generative AI]
breadcrumb: [Using Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Chat streaming responses

Synthesized responses stream in real time for Now Assist LLM chat conversations instead of waiting for the entire message to render. Streaming enables responses from the LLM to be sent immediately to help improve performance when replying to requests.

LLM response messages stream for synthesized responses as they’re generated instead of appearing all at once to end users. Responses stream in either one letter or one word at a time. After end users enter a question or request into the chat, synthesized responses begin to stream in and stop streaming after the full message has been delivered. While the response is generating, various loading messages \(such as `Generating an answer`\) appear. For more information and examples of loading messages, see [Latency feedback in Virtual Agent](../reference/latency-feedback.md). An animated sparkle ![Animated AI sparkle icon.](../../../common/image/icon-ai-sparkle.png) icon appears while the response is generating. The animated sparkle ![Animated AI sparkle icon.](../../../common/image/icon-ai-sparkle.png) icon changes to the static branded Virtual Agent icon after the response has fully loaded.

**Tip:** If you want to turn off the animated sparkle icon during streaming, set **sn\_nowassist\_va.nass\_animated\_avatar\_enabled** to `false` in the System Property \[sys\_properties\] table. When the animated sparkle icon is off, the loading messages are followed by an animated ellipsis ![Animated ellipsis icon.](../../../reuse/icons/product-icons/ellipsis-horizontal-fill-24.svg) icon. For more information about this system property, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

For standard chat, the **Show more** link appears after six lines of text is streamed. Selecting **Show more** streams the remainder of the message until the full message is delivered.

![Fully streamed response example showing six lines of text before the Show more link and Sources section.](../../now-assist-in-va/image/nava-streamed-full-message.png "Example of a standard chat streamed synthesize response fully loaded")

For enhanced chat, streaming is applicable to the synthesized response wherever it applies. When streaming completes, the entire synthesized response displays, rather than a truncated response, in the chat window or enhanced chat. The synthesized response can stream in the chat window or on the portal's search results page, as well as the enhanced chat's **Now Assist** tab.

To enable streaming, configure your AI assistants to stream responses during the Now Assist in Virtual Agent guided setup. For more information, see [Configuring assistants overview](../../now-assist-in-va/task/configure-now-assist-va.md).

**Important:** The streaming feature isn’t available when dynamic translation is turned on. To enable streaming, dynamic translation must be turned off.

