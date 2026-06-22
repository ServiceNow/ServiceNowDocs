---
title: Synthesized response in Slack conversations
description: Synthesized responses in Slack conversations provide a smarter experience with Large Language Models \(LLM\) based results summarized in a single response for users to see information in a conversational way, and avoid browsing through carousels.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/slack-synthesized-response.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-06-22"
reading_time_minutes: 2
breadcrumb: [Use Now Assist in VA conversations with Slack, Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Synthesized response in Slack conversations

Synthesized responses in Slack conversations provide a smarter experience with Large Language Models \(LLM\) based results summarized in a single response for users to see information in a conversational way, and avoid browsing through carousels.

With synthesized responses implemented in Slack conversations, the user experience is increased in several ways for the response to contain the most relevant items and information, such as:

-   Returning multiple Genius Results and topics in carousel format.
-   Providing unified search across topics and catalog items.
-   Providing a multi-Knowledge Base Q&amp;A pipeline that enables multiple snippets from multiple Knowledge Base articles to be passed to the LLM as the context for answer generation.

The overall synthesized response helps users experience a conversational flow that understands query intent, searches across records of various types, and summarizes results in a unified, easy-to-consume response.

When you start a conversation in Slack and ask a question, with Now Assist enabled on it, you receive a summary of the response with catalog items and topics followed by the citation links. For example, if you enter a command `laptop` in your conversations, you see the responses in a synthesized format.

\[Omitted image "na-slck-synthesized-rspns.png"\] Alt text: Slack synthesized response in a Now Assist enabled conversation.

When you select the **View other options** button they get the list of available Knowledge Base articles and catalogs, which you can select and go through the details.

## Streaming synthesized response

Streaming synthesized responses in Slack conversations provides a faster interaction and more engaged user experience with real-time updates while the messages are processed. To learn more about response streaming, see [Chat streaming responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/streaming-responses-requestor.md) and [Manage an assistant chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/manage-assistant-chat-experience.md).

To enable response streaming in Slack conversations, see [Enable Now Assist in Virtual Agent for Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/enable-na-llm-slack.md). With response streaming enabled in Slack conversations, you can experience the following enhancements:

-   Reduced latency in conversations
-   Increased engagement
-   Ability to handle longer or more complex queries effectively

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

**Parent Topic:**[Using Now Assist in Virtual Agent conversations with Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/na-va-llm-slack.md)

