---
title: ServiceNow Otto for Contract Management Pro release notes
description: The ServiceNow Otto for Contract Management Pro uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. ServiceNow Otto for Contract Management Pro was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# ServiceNow Otto for Contract Management Pro release notes

The ServiceNow Otto for Contract Management Pro uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. ServiceNow Otto for Contract Management Pro was enhanced and updated in the Australia release.

## ServiceNow Otto for Contract Management Pro highlights for the Australia release

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Contract Management Pro. Check your entitlements to determine your access to specific features.
-   Export conversational search results in multiple file formats.

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   Identify missing clauses in contract revisions with improved accuracy.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Provide feedback on AI contract analysis results to help improve the AI accuracy.
-   Navigate directly to non-standard clause locations in a document when reviewing AI suggestions in the Microsoft Word add-in.
-   Configure use case mappings to extract metadata and obligations from a signed contract that is uploaded directly on a contract record.
-   Use AI powered conversational search to query contract documents using natural language and dialogue-driven queries, making it easier to find relevant information.

See [ServiceNow Otto for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-now-assit-landing.md) for more information.

**Important:** Contract Management Pro - Prime is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Export conversational search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-agentic-use-conv-search.md)**

    Export search results from conversational search in multiple file formats. The export includes all search results and uses the columns configured in your list view. Customize the exported columns using the Personalize fields option.


-   **[Feedback for AI contract analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-review-contract-document.md)**

    Provide feedback on AI-identified non-standard and missing clauses to help improve AI accuracy over time. When reviewing contracts using contract analysis, you can indicate whether the AI suggestions were helpful or not helpful by using the thumbs up or thumbs down feedback options. You can also provide optional qualitative feedback with comments. The feedback option is available in both the workspace and Microsoft Word add-in.

    The feedback provided on each clause is captured in the **Contracts Gen AI Feedback** table.

-   **[Automatically navigate to non-standard clauses in Microsoft Word add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-review-contract-document.md)**

    Locate non-standard clauses easily in Microsoft Word. The document scrolls to the relevant section using AI citations when you select a suggestion in the Microsoft Word add-in.


## Changed in this release

-   **[ServiceNow® AI implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sn-ai-implementation-landing.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


-   **[Default large language model provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

    The default model provider for contract metadata extraction, contract analysis, and contract obligation extraction is Azure OpenAI.

-   **[Improved missing clause detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-NA-review-land.md)**

    Missing clause detection in contract revision using the contract analysis skill has been enhanced for accuracy. The setup, configuration, and review experience remains unchanged across all supported workspaces.


-   **[Configure use case mappings for metadata and obligation extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-na-usecase-mappings-me.md)**

    Clear the **Contracts created from contract request** check box on the use case mapping forms for the contract metadata extraction and contract obligation extraction skills to extract metadata and obligations form signed contracts that are uploaded directly on a contract record.

-   **[Conversational contract search and insights Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-agentic-use-conv-search.md)**

    The conversational search feature's improved experience enables you to:

    -   View results in a listing view, making it easier to scan, compare, and navigate contract information.
    -   Open contract documents directly from the search results and perform an in‐document search.
    The conversational search feature does not support searching within contract documents that are scanned PDFs.


## Activation information

Install Contract Management Pro - Prime by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-cmpro-landing-page.md)**

    Contract Management Pro solution enables you to set up contract document templates, clauses, and clause variations, and to initiate contract and amendmentrequests. The solution uses AI to analyze contracts and extract metadata. It also supports e-signatures, wet signatures, and external storage systems.

-   **[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)**

    The AI Admin Hub console provides you with quick and effortless access to the important information that you need to set up, configure, and monitor AI applications and features.


**Parent Topic:**[Contract Management Pro release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/cmpro-rn.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn-landing.md)

