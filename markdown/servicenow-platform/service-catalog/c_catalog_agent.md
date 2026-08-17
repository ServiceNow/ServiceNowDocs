---
title: Catalog Agent for Premium chat
description: The Catalog Agent for Premium chat uses AI Agent conversation through ServiceNow Otto to guide requesters through a conversational catalog request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/c\_catalog\_agent.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 1
keywords: [catalog agent, agentic AI, Catalog Builder, conversational catalog request]
breadcrumb: [Conversational catalog item requests, Conversational Catalog Requests, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Catalog Agent for Premium chat

The Catalog Agent for Premium chat uses AI Agent conversation through ServiceNow Otto to guide requesters through a conversational catalog request.

The Catalog Agent interprets the catalog item requester's intent, asks targeted follow-up questions in a conversational flow, and determines what information to collect next based on previous responses.

Requesters interact with the Catalog Agent through natural language, responding to prompts as they would in a chat. The Catalog Agent maps those responses to the correct catalog item variables and compiles them into a completed request when the conversation concludes.

## Key benefits

The Catalog Agent offers the following benefits:

-   Displays one question or a small set of related questions at a time, rather than a full page of fields by surfacing one question or a small set of related questions at a time, rather than a full page of fields.
-   Seeks clarification when a response is ambiguous or incomplete before moving on.
-   Handles field branching automatically, so requesters see only the questions relevant to their specific situation.
-   Enables requesters to express needs in plain language without requiring familiarity with catalog item structure or field naming conventions.
-   Supports more variable types in Premium chat sessions, providing broader AI Agent coverage for catalog item requests.
-   Provides a consistent conversational experience across portals and the ServiceNow Otto panel without requiring users to switch interfaces.

## Considerations

Consider the following when using the Catalog Agent:

-   The Catalog Agent requires catalog items to be configured to support the conversational request flow. Not all catalog items support agent-based intake by default.
-   ServiceNow Otto must be active on the instance for the Catalog Agent to function.
-   AI-generated responses during the conversation reflect the information provided by the requester. Catalog managers must review variable mappings to verify the Catalog Agent collects the correct data for each item.

**Parent Topic:**[Conversational catalog item requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/explore.md)

