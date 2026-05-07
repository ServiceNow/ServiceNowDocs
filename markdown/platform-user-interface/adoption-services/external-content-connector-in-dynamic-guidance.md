---
title: External content connector in Dynamic Guidance
description: Dynamic Guidance leverages XCC \(External Content Connector\) to provide intelligent, context-aware assistance by accessing ServiceNow product documentation.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2026-04-06"
reading_time_minutes: 1
breadcrumb: [Configure, Dynamic Guidance, Adoption services, Configure user experiences]
---

# External content connector in Dynamic Guidance

Dynamic Guidance leverages XCC \(External Content Connector\) to provide intelligent, context-aware assistance by accessing ServiceNow® product documentation.

Dynamic Guidance uses XCC specifically for to power its knowledge base search capabilities. This integration enables the system to search and retrieve relevant documentation to answer user queries effectively.

## Architecture of XCC integration

The architecture consists of three main components working together:

-   Dynamic Guidance- The user interacts with Dynamic Guidance through a voice interface. When the Generative AI application determines that it needs to search the knowledge base, it uses the search\_knowledge\_base tool.
-   RAG API handler- This middleware component receives the search query from Gemini and processes it to retrieve relevant documentation from XCC.

    **Note:** XCC uses AI search which, is enabled by default on all customer instances. See [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

-   XCC Search \(External Content Connectors ServiceNow® Docs\)- The XCC system searches the crawled ServiceNow® documentation and returns relevant content to the RAG API handler, which then provides it to Gemini for generating accurate responses.

