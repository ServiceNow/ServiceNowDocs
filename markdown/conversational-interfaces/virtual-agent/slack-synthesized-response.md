---
title: Chat responses in Slack conversations
description: Enhance your users experience in Slack conversations with smarter chat responses powered by the Large Language Models \(LLM\) based capabilities, such as synthesized response, streaming synthesized response, agentic response, and people cards.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Use Now Assist in VA conversations with Slack, Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Chat responses in Slack conversations

Enhance your users experience in Slack conversations with smarter chat responses powered by the Large Language Models \(LLM\) based capabilities, such as synthesized response, streaming synthesized response, agentic response, and people cards.

## Synthesized response

With synthesized responses implemented in Slack conversations, the user experience is increased in several ways for the response to contain the most relevant items and information, such as:

-   Returning multiple Genius Results and topics in carousel format.
-   Providing unified search across topics and catalog items.
-   Providing a multi-Knowledge Base Q&amp;A pipeline that enables multiple snippets from multiple Knowledge Base articles to be passed to the LLM as the context for answer generation.

The overall synthesized response helps users experience a conversational flow that understands query intent, searches across records of various types, and summarizes results in a unified, easy-to-consume response.

When you start a conversation in Slack and ask a question, with Now Assist enabled on it, you receive a summary of the response with catalog items and topics followed by the citation links. For example, if you enter a command `laptop` in your conversations, you see the responses in a synthesized format.

![Slack synthesized response in a Now Assist enabled conversation.](../images/na-slck-synthesized-rspns.png)

When you select the **View other options** button they get the list of available Knowledge Base articles and catalogs, which you can select and go through the details.

## Streaming synthesized response

Streaming synthesized response in Slack conversations provides a faster interaction and more engaged user experience with real-time updates while the messages are processed. To learn more about response streaming, see [Chat streaming responses](streaming-responses-requestor.md) and [Manage an assistant chat experience](../../now-assist-in-va/task/manage-assistant-chat-experience.md).

To enable response streaming in Slack conversations, see [Enable Now Assist in Virtual Agent for Slack](../task/enable-na-llm-slack.md). With response streaming enabled in Slack conversations, you can experience the following enhancements:

-   Reduced latency in conversations
-   Increased engagement
-   Ability to handle longer or more complex queries effectively

## People card in synthesized response

When your users inquire about a person in Slack conversations, they can view the synthesized response with a people card having the person's details, such as email id, contact number, and link to the ServiceNow profile.

## Agentic response

With agentic response implemented in Slack conversations, your users can view the real-time details of different steps performed by an AI agent while generating the response to your query. If required, users can also take actions while the conversation is ongoing.

To learn more about enabling agentic response, see [Use agentic support for a chat assistant](../../now-assist-in-va/task/use-agentic-support.md).

## Example of triggering AI agents through REST API

Example of using the sn\_aia REST API endpoints to trigger agents through REST API calls.

```
{
"jsonrpc": "2.0",
"id": "{{$guid}}",
"method": "message/send",
"params": {
"message": {
"kind": "message",
"role": "user",
"parts": [
{
"kind": "text",
"text": "Help me plan a calculator app"
}
],
"messageId": "{{$guid}}"
}
}
}
```

**Parent Topic:**[Using Now Assist in Virtual Agent conversations with Slack](na-va-llm-slack.md)

