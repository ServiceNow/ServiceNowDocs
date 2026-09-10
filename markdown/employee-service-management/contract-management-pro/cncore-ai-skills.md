---
title: AI skills in Contract Management Pro
description: AI skills automate contract metadata extraction, analyze contracts for clause compliance, extract obligations, and enable conversational search across contract repositories.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-ai-skills.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-01-13"
reading_time_minutes: 4
keywords: [AI skills, contract metadata extraction, contract analysis, obligation extraction, conversational search]
breadcrumb: [AI capabilities in Contract Management Pro, Explore, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# AI skills in Contract Management Pro

AI skills automate contract metadata extraction, analyze contracts for clause compliance, extract obligations, and enable conversational search across contract repositories.

The following AI skills are available for contract management:

-   **Contract analysis**

    Reviews the contract document for non-standard and missing clauses.

    For more information on activating the skill, see [Configure AI capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/confg-na-in-cmpro.md). For more information on contract analysis, see [Contract review using ServiceNow Otto for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-NA-review-land.md).

-   **Contract metadata extraction**

    Extracts metadata from a signed contract in contract repository record and displays the information on the Document Intelligence interface.

    For more information on activating the skill, see [Configure AI capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/confg-na-in-cmpro.md). For more information on extracting the metadata from a contract, see [Extract contract metadata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-metadata-extract-land.md).

-   **Contract obligation extraction**

    Extracts obligations from a signed contract in a contract repository record and displays the extracted information in the contract playbook.

    **Note:** Obligation extraction is available only with the manage contract repository agentic workflow.

    For more information on activating the skill, see [Configure AI capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/confg-na-in-cmpro.md).

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


## Contract analysis workflow

The following sample end-to-end workflow shows how different users work together to configure and review the contract by using ServiceNow Otto for Contract Management Pro.

1.  The contract AI administrator installs the ServiceNow Otto for Contract Management Pro.
2.  The contract AI administrator assigns users to the roles of contract AI fulfiller and contract AI configurator.
3.  The contract AI configurator configures and activates the contract analysis skill in the AI Admin Hub console.
4.  The contract AI configurator maps question groups to active clauses in the clause library, questions to expected responses, and use cases to specific tables.
5.  The contract AI fulfiller initiates the contract analysis by using ServiceNow Otto for Contract Management Pro.
6.  The ServiceNow Otto for Contract Management Pro application analyzes the contract and identifies the non-standard and missing clauses.
7.  The contract AI fulfiller reviews the analysis and accepts or ignores the suggested clauses.
8.  The contract AI fulfiller can also add the missing clauses from the clause library.
9.  The contract AI fulfiller completes the review task.

## Metadata extraction workflow

The following workflow shows how different users work together to configure and extract the metadata from the contract by using the ServiceNow Otto for Contract Management Pro application.

1.  The contract AI administrator installs the ServiceNow Otto for Contract Management Pro plugin \(sn\_cm\_gen\_ai\).
2.  The contract AI administrator assigns users to the roles of contract AI fulfiller and contract AI configurator.
3.  The contract AI configurator configures and activates the contract metadata extraction skill in the AI Admin Hub console.
4.  In the system properties, the administrator specifies whether the metadata extraction should be automatically or manually initiated.
5.  When a contract repository record is created with a signed contract, a contract manager with the sn\_cm\_gen\_ai.ai\_contract\_fulfiller role initiates the metadata extraction process.

    The system properties can also be configured to initiate the metadata extraction process automatically when the contract repository record is created. For more information, see [Configure system properties for contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-conf-sys-prop-na.md).

6.  The contract manager receives a notification when the metadata extraction is successfully completed.

    **Note:** The **Metadata extraction-Completed** notification isn’t active by default.

7.  The contract manager selects the **Review extracted metadata** button to view the extracted information in the DocIntel viewer.
8.  The contract manager submits the verified information to update it in the contract repository.
9.  When the extraction process is completed, the **Extraction results** tab opens on the contract repository record and displays the status of the processed information.

