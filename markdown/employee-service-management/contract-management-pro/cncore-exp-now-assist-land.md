---
title: AI capabilities in Contract Management Pro
description: Use AI capabilities to identify non-standard and missing clauses in contracts, extract metadata and obligations from signed contracts, and search contract metadata and documents using natural language.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-exp-now-assist-land.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist in contract management pro, Now Assist for contract management pro, AI for contract management pro, AI in contract management pro, ServiceNow Otto use cases, ServiceNow Otto for contract management pro]
breadcrumb: [Explore, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# AI capabilities in Contract Management Pro

Use AI capabilities to identify non-standard and missing clauses in contracts, extract metadata and obligations from signed contracts, and search contract metadata and documents using natural language.

## ServiceNow Otto for Contract Management Pro overview

ServiceNow Otto for Contract Management Pro provides the following AI capabilities for contract management:

-   **AI skills**

    AI skills enable users to extract metadata from signed contracts and analyze contracts for clause compliance.

    For more information, see [AI skills in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-ai-skills.md).

-   **Agentic workflows**

    The manage contract repository agentic workflow supports metadata and obligation extraction from signed contracts, calculates reminder dates based on contract end dates and renewal clauses, and enables users to review and update contract information through a playbook interface. Conversational search enables users to query contract metadata and documents using natural language.

    For more information, see [Agentic workflows Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-agentic-workflows.md).

-   **Contract Management Pro MCP Server**

    The Contract Management Pro MCP Server connects external AI tools to Contract Management Pro so that contract fulfillers or contract reviewers can review and redline the contract documents in their preferred AI tool using contract analysis playbooks from the system. The MCP server retrieves the latest approved Contract Analysis Playbook, which defines your organization's standard terms, approved clause language, and approved fallback language. The AI tool proposes redlines based on organizational playbook guidance.

    For more information, see [Contract Management Pro MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-negotiation-mcp.md).


## ServiceNow Otto for Contract Management Pro benefits

|Benefit|Key feature|Role|
|-------|-----------|----|
|Minimize the deviations and reduce the turnaround time by identifying non-standard and missing clauses from the contract document.|Contract analysis|Contract AI fulfiller|
|Automatically extract the key metadata from signed contracts and update the contract repository, which improves accuracy and efficiency.|Metadata extraction|Contract AI fulfiller|
|Locate contract information and insights using natural language queries across both contract metadata and signed documents. This enables quick summarization and retrieval of contract information.|Conversational search|Contract AI fulfiller|
|Extract metadata and obligations from signed contracts, calculate reminder dates based on contract terms, and enable users to review and approve extracted information through a playbook interface before updating the contract repository.|Manage contract repository|Contract AI fulfiller|
|Review contract documents in external AI tools using organizational playbook guidance from Contract Management Pro. AI-proposed redlines follow approved playbooks rather than general guidance.|Contract analysis using external AI tools|Contract AI fulfiller|

## ServiceNow Otto for Contract Management Pro users

<table id="table_ns3_1vj_qcc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Administrator\[sn\_cm\_gen\_ai.ai\_contract\_admin\]

</td><td>

Provides administrative access to ServiceNow Otto for Contract Management Pro.Installs ServiceNow Otto for Contract Management Pro plugin, and activates the required skills.

</td></tr><tr><td>

Configurator\[sn\_cm\_gen\_ai.ai\_contract\_config\]

</td><td>

Configures the use case mappings for the ServiceNow Otto for Contract Management Pro application.

</td></tr><tr><td>

AI contract fulfiller\[sn\_cm\_gen\_ai.ai\_contract\_fulfiller\]

</td><td>

Uses the ServiceNow Otto for Contract Management Pro capabilities to analyze the contract documents for deviations and to extract the metadata from signed contracts.Uses the manage contract repository agentic workflow to extract metadata and obligations automatically from signed contracts and review the extracted information in a contract playbook.

Uses conversational search to query the contract repository based on contract metadata and to perform semantic search inside the signed contract documents from the ServiceNow Otto panel.

Reviews contract documents in external AI tools that retrieve negotiation playbooks from Contract Management Pro through the Contract Management Pro MCP Server.

</td></tr></tbody>
</table>You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md).

## What to explore next

To learn more about configuring and using ServiceNow Otto for Contract Management Pro, see the following topics:

-   [Configure AI capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/confg-na-in-cmpro.md)
-   [AI capabilities in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-exp-now-assist-land.md)

