---
title: ServiceNow Otto for Contract Management Pro release notes
description: The ServiceNow Otto for Contract Management Pro uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. You can integrate external AI-powered negotiation tools with ServiceNow Otto for Contract Management Pro through Model Context Protocol to access contract context during negotiation. ServiceNow Otto for Contract Management Pro was enhanced and updated in the Brazil release. See the following sections for release notes by version.Conversational search now returns all matching results from contract document-based queries with a Show more option to load the rest. You can also run an in-document search once the contract metadata results are available.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/cmpro-otto-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [parallel signing order, parallel signature, signing order, sequential order, Wet/Offline signature, Signatories tab, Contract Workspace, DocuSign, AdobeSign]
breadcrumb: [Contract Management Pro release notes, Employee Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ServiceNow Otto for Contract Management Pro release notes

The ServiceNow Otto for Contract Management Pro uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. You can integrate external AI-powered negotiation tools with ServiceNow Otto for Contract Management Pro through Model Context Protocol to access contract context during negotiation. ServiceNow Otto for Contract Management Pro was enhanced and updated in the Brazil release. See the following sections for release notes by version.

## About ServiceNow Otto for Contract Management Pro

-   Minimize the deviations and reduce the turnaround time by identifying non-standard and missing clauses from the contract document.
-   Automatically extract the key metadata from signed contracts and update the contract repository, which improves accuracy and efficiency.
-   Locate contract information and insights using natural language queries across both contract metadata and signed documents. This enables quick summarization and retrieval of contract information.
-   Extract metadata and obligations from signed contracts, calculate reminder dates based on contract terms, and enable users to review and approve extracted information through a playbook interface before updating the contract repository.
-   Review contract documents in external AI tools using organizational playbook guidance from . AI-proposed redlines follow approved playbooks rather than general guidance.

See [AI capabilities in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-exp-now-assist-land.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Contract Management Pro - Prime by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Contract Management Pro release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/cmpro-landing-page.md)

## Version 2.5.2

Conversational search now returns all matching results from contract document-based queries with a Show more option to load the rest. You can also run an in-document search once the contract metadata results are available.

### What's changed

-   **[Search in contracts document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cmpro-na-converse-ask-ques-new.md)**

    Contract document-based conversational search queries now return all matching results instead of 10 results. Use Show more option to load the remaining results.

-   **[Search in contract metadata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cmpro-na-search-metadata.md)**

    In conversational search, introduced an option to preform in-document search after the contract metadata search results are available.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


