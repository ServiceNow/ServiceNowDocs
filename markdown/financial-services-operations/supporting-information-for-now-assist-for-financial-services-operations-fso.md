---
title: Supporting information for ServiceNow Otto for Financial Services Operations \(FSO\)
description: Get a quick overview of the important information that is related to the ServiceNow Otto for Financial Services Operations \(FSO\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/supporting-information-for-now-assist-for-financial-services-operations-fso.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [generative AI for financial services operations versions, generative AI for financial services operations licensing, generative AI for financial services operations dependencies, generative AI for financial services operations activation]
breadcrumb: [AI in FSO, Explore, Financial Services Operations \(FSO\)]
---

# Supporting information for ServiceNow Otto for Financial Services Operations \(FSO\)

Get a quick overview of the important information that is related to the ServiceNow Otto for Financial Services Operations \(FSO\) application.

## Supported user interfaces

AI skills in FSO are supported in the following user interfaces.

<table id="table_n13_4fj_mbc"><thead><tr><th>

Interface

</th><th>

Skill

</th></tr></thead><tbody><tr><td>

Financial Services Workspace

</td><td>

-   Case summarization
-   Disputes intake via Virtual Agent

</td></tr><tr><td>

Core UI

</td><td>

Case summarization

</td></tr><tr><td>

Customer 360 page and Interaction page in Agentic Contact Center for Banking

</td><td>

-   Customer profile summarization
-   Customer interaction context summary

</td></tr><tr><td>

Customer 360 and Interaction page in Agentic Contact Center for Insurance

</td><td>

-   Insurance customer profile summarization
-   Insurance interaction context summary

</td></tr><tr><td>

Portal

</td><td>

Disputes intake via Virtual Agent

</td></tr></tbody>
</table>## Financial Services Operations AI agent collection

The FSO AI agent collection \(`sn_fso_ai_agents`\) provides a shared library of AI agents for Financial Services Operations. The agents understand user-defined goals, formulate strategic plans, help human agents resolve cases, and autonomously execute tasks.

For a list of AI agents included in the collection, see [AI capabilities in Financial Services Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/ai-capabilities-in-fso.md).

## Query Orchestrator

Query Orchestrator \(`sn_qry_orchstr`\) provides a shared, reusable orchestration layer for AI agents across Financial Services Operations business domains. The Query Orchestrator breaks down complex questions into smaller, targeted sub-queries; routes each sub-query to the most appropriate data source; and aggregates the results into a single structured response for the AI agent to use.

Query Orchestrator provides the following capabilities:

-   **Query decomposition**

    Analyzes complex questions and breaks it into sub-queries that can each be answered independently.

-   **Intent classification**

    Identifies each sub-query intent to determine how it should be handled and which data source is most appropriate.

-   **Source routing**

    Maps each sub-query to the most appropriate data source based on the classified intent. Examples include Knowledge Base search for article lookups, or Knowledge Graph for entity and relationship data.

-   **Parallel execution**

    Dispatches sub-queries to their assigned sources concurrently to minimize overall response latency.

-   **Response aggregation**

    Collects results from all sources and merges them into a single structured payload for the AI agent.

-   **Structured output**

    Returns results in a consistent, schema-defined format that the AI agent uses to generate a comprehensive answer in the ServiceNow Otto panel.


**Related topics**  


[AI capabilities in Financial Services Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/ai-capabilities-in-fso.md)

[Enable AI capabilities in Financial Services Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/enable-ai-capabilities-in-fso.md)

