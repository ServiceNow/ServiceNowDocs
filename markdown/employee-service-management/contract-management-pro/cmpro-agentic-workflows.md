---
title: Agentic workflows Contract Management Pro
description: Use agentic workflows in Contract Management Pro to extract metadata and obligations from signed contracts, and set reminders for contract renewals or termination.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-agentic-workflows.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [AI agents in CM Pro, AI agents in contracts, AI agents in contract management pro, agentic workflows in contract management pro, agentic workflows in contracts, agentic workflows in CM Pro]
breadcrumb: [AI capabilities in Contract Management Pro, Explore, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Agentic workflows Contract Management Pro

Use agentic workflows in Contract Management Pro to extract metadata and obligations from signed contracts, and set reminders for contract renewals or termination.

The following agentic workflows are available for contract management:

-   **Manage contract repository**

    Extracts metadata and obligations from signed contracts, calculates reminder dates based on contract terms, and enables users to review and approve extracted information through a playbook interface before updating the contract repository.

    For more information on activating the skill, see [Configure AI capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/confg-na-in-cmpro.md). For more information on how to use the skill, see [Extract contract metadata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-metadata-extract-land.md) and [Create obligations using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-create-obligations-landing.md).

-   **Conversational contract search and insights**

    Queries contract documents with conversational search using natural language and dialogue-driven queries, making it easier to find relevant information.

    Conversational search enables queries based on:

    -   Contract metadata
    -   Content available in the contract document
    -   Combined search across metadata and contract document
    -   Summarization and Q&amp;A on contract documents
    Limitations:

    -   No support for search within scanned PDF documents
    -   Search functionality is limited to contracts stored in internal storage only
    For more information on activating the skill, see [Configure AI capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/confg-na-in-cmpro.md).


<table id="table_dxr_mb1_v2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Manage contract repository

</td><td>

Uses an AI agent to extract key metadata and obligations from a signed contract, and calculate the contract reminder date by analyzing the contract end date, auto-renewal clause, and notice period for contract renewal or termination. The playbook in the contract record enables users to review AI extracted metadata and obligations to update the contract repository with extracted metadata, and create obligation records, respectively. Users can also set reminders for contract renewal or termination.**Note:** The agentic workflow is triggered in the ServiceNow Otto panel. It is not supported in the Virtual Agent panel.

</td><td>

Contract repository AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read only.

To modify an agentic workflow, you must first duplicate it, and then update it. For more information, see:

-   [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md)
-   [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md)
-   [Modify an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aia-use-case.md)

**Note:** When you modify an agentic workflow, AI agents, or tools, make sure that you update all instructions accordingly.

If you have customized the manage contract repository agentic workflow, [update the script include to run it autonomously.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-script-includ-agenticAI.md)

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md).

