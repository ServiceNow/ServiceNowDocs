---
title: AI Service Graph connector for LangGraph
description: Use the  AI Service Graph Connector for LangGraph to discover AI assets such as AI systems, agents, models, tools, and prompts and well as usage data for these AI agents. This usage information is consumed by the AI Control Tower value dashboard.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-03"
reading_time_minutes: 1
breadcrumb: [Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# AI Service Graph connector for LangGraph

Use the  AI Service Graph Connector for LangGraph to discover AI assets such as AI systems, agents, models, tools, and prompts and well as usage data for these AI agents. This usage information is consumed by the AI Control Tower value dashboard.

## Download apps from the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home)  website to download the AI Service Graph Connector for LangGraph app.

## Supported ServiceNow versions

-   Australia
-   Zurich patch 7
-   Yokohama patch 11

## User roles

Roles required in the ServiceNow environment:

-   sn\_ai\_disc.discovery\_admin
-   sn\_cmdb\_int\_util.sgc\_admin

## Prerequisites from LangGraph

Steps to be performed in LangGraph environment:

Enter the connection details and API Key credentials and update the credential record.

1.  **Connection Name**: Choose a unique name for this connection.
2.  **Connection URL for LangSmith API**: The URL to use when connecting to the LangSmith API, e.g. ‘’https://my-langsmith.example/com/api’’ if not self-hosting, it is recommended to leave this value as it is.
3.  **Connection URL for LangSmith host API**: The URL to use when connecting to the LangSmith “host” API, e.g. ‘’https://my-langsmith.example/com/api-host. If it is not self-hosting, it is recommended to leave the value as it is.
4.  **API Key**: The API key from LangSmith to use for authorization. The API Key should provide access to at least one workspace.

