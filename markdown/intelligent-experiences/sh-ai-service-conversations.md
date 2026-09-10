---
title: Detected AI service conversations
description: Judge the sensitivity of what's being shared a detected AI service by reading the actual prompt text sent to the service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sh-ai-service-conversations.html
release: australia
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Investigate a detected AI service, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Detected AI service conversations

Judge the sensitivity of what's being shared a detected AI service by reading the actual prompt text sent to the service.

## Reviewing conversations and prompts

The **Conversations** tab groups individual prompts that belong to the same session, showing you the exchange between a user and a service. Read through the prompts in a conversation to learn how the service is being used. A code assistant receiving routine syntax questions is a different exposure than the same service receiving customer records or credentials.

-   View the user and LLM model used by the service that received the prompt.
-   View the size of the request in the **Request size \(bytes\)** column.
-   Learn when the request was sent and through which channel by viewing the **Sources** column.
-   Drill further into usage details by selecting a prompt in the list.

The **Conversations** tab appears on services that Agent Client Collector \(ACC\) detected, because it displays request content read on the device before encryption. See [How Shadow AI detects unsanctioned AI use](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-how-detection-works.md) for which signals each detection method reports.

**Parent Topic:**[Investigating a detected AI service in Shadow AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-investigating-detected-services.md)

