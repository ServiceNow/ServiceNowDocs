---
title: Configure Conversational contract search and insights
description: Configure Conversational contract search and insights skill to enable searching information in contracts using natural language and dialogue-driven queries, making it easier to find relevant information.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-10-25"
reading_time_minutes: 2
keywords: [Obligation extraction, Configure obligation extraction]
breadcrumb: [Configure agentic workflows, Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure Conversational contract search and insights

Configure Conversational contract search and insights skill to enable searching information in contracts using natural language and dialogue-driven queries, making it easier to find relevant information.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

Complete the following steps to configure Conversational contract search and insights.

-   **[Copy contract documents to contract repository](cmpro-na-conv-copy-docs-to-cntr.md)**

    Copy signed contract documents into the contract repository for conversational search.

-   **[Index contracts table for conversational search](cmpro-converse-search-indexing.md)**

    Index the data for conversational search.

-   **[Configure conversational search tables](cmpro-na-kg-table.md)**

    Configure Knowledge graph tags to identify which tables should be used for answering natural language questions in conversational search.

-   **[Configuring user access and data permissions for agentic workflows](../concept/cmpro-conf-users-agentic-wf.md)**

    Set the data access permissions for the agentic workflow- Conversational Contract Search.

-   **[Configuring user access and data permissions for AI agents](../concept/cmpro-conf-users-ai-agents.md)**

    Set the data access permissions for the Agent- Search contracts AI.

-   **[Configure data permissions for Now Assist skills](cmpro-conf-roles-skills.md)**

    Set the data access permissions for the Now Assist skills- Contracts query enhancer, Contracts query classifier and Search contract with contextual input.


## Accessing the Agentic Workflow

If your generative AI service provider isn’t Now LLM Service, verify that the API connections and credentials are configured. For more information, see [Configuring API credentials for generative AI capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller/configuring-api-credentials-for-generative-ai-capabilities.md).

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Search for **Conversational Contract Search and Insights** and open it.

## AI agents used in Search for Conversational Contract Search and Insights Workflow

|Name|Description|
|----|-----------|
|Search contracts AI agent|This agent helps you find and understand legal contracts and documents by giving search results for questions asked in natural language. It works as a conversational search and Q&amp;A tool within the Contract Lifecycle Management system.|
|Document and visual insights AI agent|This agent helps with tasks related to processing of documents. For more information, see [Document and visual insights AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/document-and-visual-insights-ai-agent.md).|

