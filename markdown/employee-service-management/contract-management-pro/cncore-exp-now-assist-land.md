---
title: Explore Now Assist in Contract Management
description: Use AI capabilities to identify non-standard and missing clauses in a contract and locate contract insights from contract metadata and documents using natural language. With metadata extraction, automatically extract metadata from signed contracts and add it to the contract repository. Use obligation extraction to capture obligations from signed contracts and create obligation records to track and fulfill compliance requirements.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
keywords: [Now Assist in contract management pro, Now Assist for contract management pro, AI for contract management pro, AI in contract management pro]
breadcrumb: [Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Explore Now Assist in Contract Management

Use AI capabilities to identify non-standard and missing clauses in a contractand locate contract insights from contract metadata and documents using natural language. With metadata extraction, automatically extract metadata from signed contracts and add it to the contract repository. Use obligation extraction to capture obligations from signed contracts and create obligation records to track and fulfill compliance requirements.

## Overview of Now Assist in Contract Management

The following AI capabilities are available to a contract fulfiller:

-   Extract the metadata from a signed contract to review and add the information to the mapped fields in the contract repository.
-   Analyze the contract documents for non-standard and missing clauses by using AI-generated suggestions to minimize deviations and reduce turnaround time.
-   Automatically extract obligations from a signed contract and review those obligations in the contract playbook to create obligation records in a contract record.
-   Use conversational search to query the contract repository based on contract metadata and to perform semantic search in the signed contract documents from the Now Assist panel.

## Skills

-   **Contract metadata extraction**

    Extracts metadata from a signed contract in contract repository record and displays the information on the Document Intelligence interface.

    For more information on activating the skill, see [Configure Now Assist in Contract Management](../task/confg-na-in-cmpro.md). For more information on extracting the metadata from a contract, see [Metadata extraction using Now Assist in Contract Management](cncore-metadata-extract-land.md).

-   **Contract analysis**

    Reviews the contract document for non-standard and missing clauses.

    For more information on activating the skill, see [Configure Now Assist in Contract Management](../task/confg-na-in-cmpro.md). For more information on contract analysis, see [Contract analysis using Now Assist in Contract Management](cncore-NA-review-land.md).

-   **Contract obligation extraction**

    Extracts obligations from a signed contract in a contract repository record and displays the extracted information in the contract playbook.

    **Note:** Obligation extraction is available only with the manage contract repository agentic workflow.

    For more information on activating the skill, see [Configure Now Assist in Contract Management](../task/confg-na-in-cmpro.md).

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
    -   A maximum of 20 search results are displayed for a query
    -   Queries involving related tables, such as Obligations, aren't supported
    For more information on activating the skill, see [Configure Now Assist in Contract Management](../task/confg-na-in-cmpro.md).


You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Now Assist in Contract Management users

<table id="table_ns3_1vj_qcc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Administrator\[sn\_cm\_gen\_ai.ai\_contract\_admin\]

</td><td>

Provides administrative access to Now Assist in Contract Management.Installs Now Assist in Contract Management plugin, and activates the required skills.

</td></tr><tr><td>

Configurator\[sn\_cm\_gen\_ai.ai\_contract\_config\]

</td><td>

Configures the use case mappings for the Now Assist in Contract Management application.

</td></tr><tr><td>

AI contract fulfiller\[sn\_cm\_gen\_ai.ai\_contract\_fulfiller\]

</td><td>

Uses the Now Assist in Contract Management capabilities to analyze the contract documents for deviations and to extract the metadata from signed contracts.Uses the manage contract repository agentic workflow to extract metadata and obligations automatically from signed contracts and review the extracted information in a contract playbook.

Uses conversational search to query the contract repository based on contract metadata and to perform semantic search inside the signed contract documents from the Now Assist panel.

</td></tr></tbody>
</table>## Metadata extraction workflow

The following workflow shows how different users work together to configure and extract the metadata from the contract by using the Now Assist in Contract Management application.

1.  The contract AI administrator installs the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\).
2.  The contract AI administrator assigns users to the roles of contract AI fulfiller and contract AI configurator.
3.  The contract AI configurator configures and activates the Contract metadata extraction skill in the Now Assist Admin console.
4.  In the system properties, the administrator specifies whether the metadata extraction should be automatically or manually initiated.
5.  When a contract repository record is created with a signed contract, a contract manager with the sn\_cm\_gen\_ai.ai\_contract\_fulfiller role initiates the metadata extraction process.

    The system properties can also be configured to initiate the metadata extraction process automatically when the contract repository record is created. For more information, see [Configure system properties for contract metadata extraction](../task/cncore-conf-sys-prop-na.md).

6.  The contract manager receives a notification when the metadata extraction is successfully completed.

    **Note:** The **Metadata extraction-Completed** notification isn’t active by default.

7.  The contract manager selects the **Review extracted metadata** button to view the extracted information in the DocIntel viewer.
8.  The contract manager submits the verified information to update it in the contract repository.
9.  When the extraction process is completed, the **Extraction results** tab opens on the contract repository record and displays the status of the processed information.

## Contract analysis workflow

The following sample end-to-end workflow shows how different users work together to configure and review the contract by using Now Assist in Contract Management.

1.  The contract AI administrator installs the Now Assist in Contract Management application.
2.  The contract AI administrator assigns users to the roles of contract AI fulfiller and contract AI configurator.
3.  The contract AI configurator configures and activates the contract analysis skill in the Now Assist Admin console.
4.  The contract AI configurator maps the question groups to the active clauses in the clause library, maps the questions to the expected responses, and then maps the use case to specific tables.
5.  The contract AI fulfiller initiates the contract analysis by using Now Assist in Contract Management.
6.  The Now Assist in Contract Management application analyzes the contract and identifies the non-standard and missing clauses.
7.  The contract AI fulfiller reviews the analysis and accepts or ignores the suggested clauses.
8.  The contract AI fulfiller can also add the missing clauses from the clause library.
9.  The contract AI fulfiller completes the review task.

## Now Assist in Contract Management benefits

|Benefit|Key feature|Role|
|-------|-----------|----|
|Automatically extract the key metadata from signed contracts and update the contract repository, which improves accuracy and efficiency.|Metadata extraction|Contract AI fulfiller|
|Minimize the deviations and reduce the turnaround time by identifying non-standard and missing clauses from the contract document.|Contract analysis|Contract AI fulfiller|
|Automatically extract obligation from signed contracts and create obligation records in contract repository to track and fulfill the responsibilities specified in a contract.|Obligation extraction|Contract AI fulfiller|
|Locate contract information and insights using natural language queries across both contract metadata and signed documents. This enables quick summarization and retrieval of contract information.|Conversational search|Contract AI fulfiller|

## What to explore next

To learn more about configuring and using Now Assist in Contract Management, see the following topics:

-   [Configure Now Assist in Contract Management](../task/confg-na-in-cmpro.md)
-   [Using Now Assist in Contract Management](cncore-use-now-assist-land.md)

