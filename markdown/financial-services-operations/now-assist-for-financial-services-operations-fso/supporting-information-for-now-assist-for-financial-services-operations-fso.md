---
title: Supporting information for Now Assist for Financial Services Operations \(FSO\)
description: Get a quick overview of the important information that is related to the Now Assist for Financial Services Operations \(FSO\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/now-assist-for-financial-services-operations-fso/supporting-information-for-now-assist-for-financial-services-operations-fso.html
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [generative AI for financial services operations versions, generative AI for financial services operations licensing, generative AI for financial services operations dependencies, generative AI for financial services operations activation]
breadcrumb: [Reference, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Supporting information for Now Assist for Financial Services Operations \(FSO\)

Get a quick overview of the important information that is related to the Now Assist for Financial Services Operations \(FSO\) application.

## Supported versions

Now Assist for FSO is supported starting with the Xanadu release.

## Supported user interfaces

The Now Assist for FSO application includes the skills that are listed in the following table.

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
</table>## Application information

Activate the Now Assist for FSO store app \(sn\_fso\_gen\_ai\) to use the capabilities included in the application.

This store app has the following dependencies:

-   Financial Services Operations Core \(sn\_bom\)
-   Now Assist for Platform \(sn\_genai\_platform\)
-   Now Assist for Customer Service Management \(CSM\) \(sn\_csm\_gen\_ai\)
-   Form Data Collector \(sn\_con\_frm\_dt\_coll\)
-   Financial Services Operations AI Agent Collection \(sn\_fso\_ai\_agents\)
-   Query Orchestrator \(sn\_qry\_orchstr\)

Activate the applications in the following order:

1.  Financial Services Card Operations \(sn\_bom\_credit\_card\)
2.  Now Assist for FSO \(sn\_fso\_gen\_ai\)

## Financial Services Operations AI agent collection

The FSO AI agent collection \(`sn_fso_ai_agents`\) is a ServiceNow Store application included with Now Assist for FSO. It provides a shared library of AI agents for Financial Services Operations. The agents understand user-defined goals, formulate strategic plans, help human agents resolve cases, and autonomously execute tasks.

For a list of AI agents included in the collection, see the following:

-   [Standalone AI agents in Financial Services Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/ai-agents-fso.md)
-   [Using agentic workflows in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/using-ai-agent-use-cases-in-now-assist-for-fso.md)

## Query Orchestrator

Query Orchestrator \(`sn_qry_orchstr`\) is a ServiceNow Store application included with Now Assist for FSO. It provides a shared, reusable orchestration layer for AI agents across Financial Services Operations business domains. The Query Orchestrator breaks down complex questions into smaller, targeted sub-queries; routes each sub-query to the most appropriate data source; and aggregates the results into a single structured response for the AI agent to use.

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

    Returns results in a consistent, schema-defined format that the AI agent uses to generate a comprehensive answer in the Now Assist panel.


-   **[Form Data Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/learn-about-the-form-data-collector.md)**  
Learn about the Form Data Collector. This application is used to assist with populating case form fields during a customer's interaction with a Virtual Agent chatbot.

**Parent Topic:**[Now Assist for Financial Services Operations \(FSO\) reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-fso-reference.md)

**Related topics**  


[Configure case summarization in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-now-assist-for-fso.md)

[Configure Disputes intake via Virtual Agent in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configuring-disputes-intake-via-virtual-agent.md)

