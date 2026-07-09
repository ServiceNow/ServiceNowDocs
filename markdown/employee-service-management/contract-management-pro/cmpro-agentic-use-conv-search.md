---
title: Conversational contract search and insights Workflow
description: Configure conversational contract search and insights workflow to enable searching information in contracts using natural language and dialogue-driven queries, making it easier to find relevant information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/contract-management-pro/cmpro-agentic-use-conv-search.html
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using Now Assist in Contract Management, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Conversational contract search and insights Workflow

Configure conversational contract search and insights workflow to enable searching information in contracts using natural language and dialogue-driven queries, making it easier to find relevant information.

## Configurations for Conversational contract search and insights

**Important:**

-   Verify you have set the data access permission for your role in the following:
    -   Conversational Contract Search agentic workflow.

        For more information, see [Configuring user access and data permissions for agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cmpro-conf-users-agentic-wf.md).

    -   Search contracts AI agent.

        For more information, [Configuring user access and data permissions for AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cmpro-conf-users-ai-agents.md).

    -   Contracts query enhancer and Search contract with contextual input Now Assist skills.

        For more information, see [Configure data permissions for Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cmpro-conf-roles-skills.md)

-   Verify you have run the scheduled job to copy signed contract documents into the contract repository. For more information, see [Copy contract documents to contract repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cmpro-na-conv-copy-docs-to-cntr.md).
-   Verify you have indexed the data for conversational search. For more information, see [Index contracts table for conversational search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cmpro-converse-search-indexing.md).

    Verify all the skills are activated and configurations complete. For more information, see [Verify skill activation and configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cmpro-converse-skills-activation.md).

-   Verify you have turned on the Now Assist panel to view the agentic workflow in it. For more information, see [Activate Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/activate-now-assist-panel.md).

## Conditions for the Agentic Workflow to trigger

The Conversational contract search and insights is triggered when a you enter queries in the Now Assist panel.

Contract fulfillers and assignment group managers with the now\_assist\_panel\_user role can view the agentic workflow conversation in the Now Assist panel.

**Note:** The agentic workflow isn’t supported in the Virtual Agent panel.

## Accessing the Agentic Workflow

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller

If your generative AI service provider isn’t Now LLM Service, verify that the API connections and credentials are configured. For more information, see [Configuring API credentials for generative AI capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configuring-api-credentials-for-generative-ai-capabilities.md).

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Search for **Search for Conversational Contract Search and Insights** and open it.

## AI agents used in Search for Conversational Contract Search and Insights Workflow

|Name|Description|
|----|-----------|
|Search contracts AI agent|This agent helps you find and understand legal contracts and documents by giving search results for questions asked in natural language. It works as a conversational search and Q&amp;A tool within the Contract Lifecycle Management system.|
|Document and visual insights AI agent|This agent helps with tasks related to processing of documents. For more information, see [Document and visual insights AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/document-and-visual-insights-ai-agent.md).|

-   **[Search in contracts using conversational search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cmpro-na-converse-ask-ques.md)**  
Ask question in the Now Assist panel to search for information on the contracts and its content.

**Parent Topic:**[Using Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-use-now-assist-land.md)

**Related topics**  


[Metadata extraction using Now Assist in Contract Management]()

[Contract analysis using Now Assist in Contract Management]()

