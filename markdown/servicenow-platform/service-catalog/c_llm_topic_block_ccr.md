---
title: LLM topic block for Conversational Catalog Requests
description: The LLM topic block is a Virtual Agent topic component that connects a conversational catalog request to ServiceNow Otto. It enables generative AI to interpret requester input during the conversation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/c\_llm\_topic\_block\_ccr.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 1
keywords: [LLM topic block, Virtual Agent, Conversational Catalog Requests, generative AI]
breadcrumb: [Conversational catalog item requests, Conversational Catalog Requests, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# LLM topic block for Conversational Catalog Requests

The LLM topic block is a Virtual Agent topic component that connects a conversational catalog request to ServiceNow Otto. It enables generative AI to interpret requester input during the conversation.

Virtual Agent topics for Conversational Catalog Requests use the LLM topic block to hand off requester input to ServiceNow Otto.

When a requester describes what they need in the chat interface, the LLM topic block sends that natural language input to ServiceNow Otto, which processes it and returns the most relevant catalog item for the conversation to continue with.

The LLM topic block sits within the Virtual Agent topic flow and acts as the integration point between the conversation and the ServiceNow Otto generative AI service. Without it, the Virtual Agent topic can't route requester input to ServiceNow Otto for catalog item resolution.

## Key benefits

The LLM topic block offers the following benefits in Conversational Catalog Request topics:

-   Eliminates rigid keyword-matching logic in Virtual Agent topic design by delegating catalog item resolution to ServiceNow Otto.
-   Enables a single conversational topic to resolve requests across multiple catalog categories, reducing the number of Virtual Agent topics a designer must maintain.
-   Transfers conversation context from the Virtual Agent session to ServiceNow Otto, so the AI response reflects what the requester has already described rather than starting from an empty prompt.

**Parent Topic:**[Conversational catalog item requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/explore.md)

