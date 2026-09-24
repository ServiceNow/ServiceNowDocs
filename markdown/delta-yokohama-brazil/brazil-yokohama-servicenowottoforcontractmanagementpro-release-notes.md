---
title: Combined ServiceNow Otto for Contract Management Pro release notes for upgrades from Yokohama to Brazil
description: Consolidated page of all release notes for ServiceNow Otto for Contract Management Pro from Yokohama to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-brazil/brazil-yokohama-servicenowottoforcontractmanagementpro-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 21
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto for Contract Management Pro release notes for upgrades from Yokohama to Brazil

Consolidated page of all release notes for ServiceNow Otto for Contract Management Pro from Yokohama to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto for Contract Management Pro release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto for Contract Management Pro to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for ServiceNow Otto for Contract Management Pro.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Automated obligation extraction](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&family=yokohama&ft:locale=en-US)**

Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Using contract playbook to review AI-extracted obligations](https://www.servicenow.com/docs/access?context=cmpro-na-review-obligations&family=yokohama&ft:locale=en-US)**

Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **[Contract obligation extraction skill in Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-conf-obligation-extraction&family=yokohama&ft:locale=en-US)**

Configure and map use cases for obligation extraction skill in the AI Admin Hub console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Conversational contract search and insights Workflow](https://www.servicenow.com/docs/access?context=cmpro-agentic-use-conv-search&family=yokohama&ft:locale=en-US)**

Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://www.servicenow.com/docs/access?context=now-llm-model-updates&family=yokohama&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


 -   **[Review AI results](https://www.servicenow.com/docs/access?context=cmpro-na-review-ai&family=yokohama&ft:locale=en-US)**

Use the playbook within a contract repository record to review the metadata extracted by the AI agents in the Manage contract repository agentic workflow. You can make necessary changes to the extracted information, and submit it to update the contract repository. If the contract end date is available, the **Review contract reminders** tab appears in the playbook, enabling you to review and update the AI-calculated contract reminder date and specify recipients for contract renewal or terminations.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=yokohama&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Select large language models for use cases in Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cmpro-na-manage-llm&family=yokohama&ft:locale=en-US)**

Select a large language models \(LLM\) provider at for a contract analysis or metadata extraction use case. The selected LLM is applicable only for the specific use case and overrides the LLM selected for Now Assist in Contract Management skills.


 -   **[Manage contract repository agentic workflow](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&family=yokohama&ft:locale=en-US)**

Use the Manage contract repository agentic workflow to improve productivity by autonomously creating milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.

    |Agentic workflows|Description|
    |-----------------|-----------|
    |Manage contract repository|Uses AI agents to retrieve contract details such as renewal notice period, termination notice period, or auto-renewal clause information, and determine the average lead time for similar contracts to create contract milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.|


</td></tr><tr><td>

Zurich

</td><td>

-   **[Export conversational search results](https://www.servicenow.com/docs/access?context=cmpro-agentic-use-conv-search&family=zurich&ft:locale=en-US)**

Export search results from conversational search in multiple file formats. The export includes all search results and uses the columns configured in your list view. Customize the exported columns using the Personalize fields option.


 -   **[Feedback for Now Assist contract analysis](https://www.servicenow.com/docs/access?context=cmpro-review-contract-document&family=zurich&ft:locale=en-US)**

Provide feedback on AI-identified non-standard and missing clauses to help improve AI accuracy over time. When reviewing contracts using Now Assist contract analysis, you can indicate whether the AI suggestions were helpful or not helpful by using the thumbs up or thumbs down feedback options. You can also provide optional qualitative feedback with comments. The feedback option is available in both the workspace and Microsoft Word add-in.

The feedback provided on each clause is captured in the **Contracts Gen AI Feedback** table.

-   **[Automatically navigate to non-standard clauses in Microsoft Word add-in](https://www.servicenow.com/docs/access?context=cmpro-review-contract-document&family=zurich&ft:locale=en-US)**

Locate non-standard clauses easily in Microsoft Word. The document scrolls to the relevant section using AI citations when you select a Now Assist suggestion in the Microsoft Word add-in.


 -   **[Automated obligation extraction](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&family=zurich&ft:locale=en-US)**

Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Using contract playbook to review AI-extracted obligations](https://www.servicenow.com/docs/access?context=cmpro-na-review-obligations&family=zurich&ft:locale=en-US)**

Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **[Contract obligation extraction skill in Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-conf-obligation-extraction&family=zurich&ft:locale=en-US)**

Configure and map use cases for obligation extraction skill in the AI Admin Hub console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Use conversational contract search and insights](https://www.servicenow.com/docs/access?context=cmpro-agentic-use-conv-search&family=zurich&ft:locale=en-US)**

Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some generative AI skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://www.servicenow.com/docs/access?context=now-llm-model-updates&family=zurich&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


 -   **[Using contract playbook to review AI-extracted metadata and contract reminder date](https://www.servicenow.com/docs/access?context=cmpro-na-review-ai&family=zurich&ft:locale=en-US)**

Use the playbook within a contract repository record to review the metadata extracted by the AI agents in the manage contract repository agentic workflow. You can make necessary changes to the extracted information, and submit it to update the contract repository. If the contract end date is available, the **Review contract reminders** tab appears in the playbook, enabling you to review and update the AI-calculated contract reminder date and specify recipients for contract renewal or terminations.

-   **[New third-party AI model provider options available for all AI applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.

-   **[New third-party AI model provider options available for all AI applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.

-   **[Select LLMs](https://www.servicenow.com/docs/access?context=cmpro-na-manage-llm&family=zurich&ft:locale=en-US)**

Select a large language model \(LLM\) provider for a contract analysis or metadata extraction use case. The selected LLM is applicable only for the specific use case and overrides the LLM selected for Now Assist in Contract Management skills.


</td></tr><tr><td>

Australia

</td><td>

-   **[Contract Management Pro MCP Server](https://www.servicenow.com/docs/access?context=cmpro-negotiation-mcp&family=australia&ft:locale=en-US)**

Review contract documents against organization's standards using an external AI tool connected to Contract Management Pro through the MCP Server. The MCP server retrieves the latest approved Contract Analysis Playbook containing organization's standard terms, approved clause language, and approved fallback language. The AI tool uses the playbook to suggest changes and redline the document.


 -   **[Export conversational search results](https://www.servicenow.com/docs/access?context=cmpro-agentic-workflows&family=australia&ft:locale=en-US)**

Export search results from conversational search in multiple file formats. The export includes all search results and uses the columns configured in your list view. Customize the exported columns using the Personalize fields option.


 -   **[Feedback for AI contract analysis](https://www.servicenow.com/docs/access?context=cmpro-review-contract-document&family=australia&ft:locale=en-US)**

Provide feedback on AI-identified non-standard and missing clauses to help improve AI accuracy over time. When reviewing contracts using contract analysis, you can indicate whether the AI suggestions were helpful or not helpful by using the thumbs up or thumbs down feedback options. You can also provide optional qualitative feedback with comments. The feedback option is available in both the workspace and Microsoft Word add-in.

The feedback provided on each clause is captured in the **Contracts Gen AI Feedback** table.

-   **[Automatically navigate to non-standard clauses in Microsoft Word add-in](https://www.servicenow.com/docs/access?context=cmpro-review-contract-document&family=australia&ft:locale=en-US)**

Locate non-standard clauses easily in Microsoft Word. The document scrolls to the relevant section using AI citations when you select a suggestion in the Microsoft Word add-in.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing ServiceNow Otto for Contract Management Pro features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Automated obligation extraction](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&family=yokohama&ft:locale=en-US)**

Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Using contract playbook to review AI-extracted obligations](https://www.servicenow.com/docs/access?context=cmpro-na-review-obligations&family=yokohama&ft:locale=en-US)**

Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **[Contract obligation extraction skill in Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-conf-obligation-extraction&family=yokohama&ft:locale=en-US)**

Configure and map use cases for obligation extraction skill in the AI Admin Hub console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Conversational contract search and insights Workflow](https://www.servicenow.com/docs/access?context=cmpro-agentic-use-conv-search&family=yokohama&ft:locale=en-US)**

Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://www.servicenow.com/docs/access?context=now-llm-model-updates&family=yokohama&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


 -   **[Extract metadata from signed contracts automatically](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&family=yokohama&ft:locale=en-US)**

Use the AI agents in the Manage contract repository agentic workflow to automatically extract metadata from signed contracts and calculate the contract reminder dates for contract renewal or termination. You can review the AI results in the contract playbook and update it if necessary before saving it.

-   **[Contract metadata extraction use cases](https://www.servicenow.com/docs/access?context=metadata-extraction-use-case&family=yokohama&ft:locale=en-US)**

Support for 14 additional metadata fields in the CM Pro - Contract Metadata Extraction use case available in the base system.


 -   **[Configuring contract metadata extraction](https://www.servicenow.com/docs/access?context=cncore-conf-metadata-extraction&family=yokohama&ft:locale=en-US)**

Create a use case and its associated fields for contract metadata extraction in the AI Admin Hub console to define the information that you want Now Assist to detect in a signed contract.Create a use case mapping in the AI Admin Hub console to map a use case to specific tables and define conditions to apply the use case for metadata extraction.

-   **[Configuring contract analysis](https://www.servicenow.com/docs/access?context=cmpro-conf-contract-analysis&family=yokohama&ft:locale=en-US)**

Create a use case and its associated question groups for contract analysis in the AI Admin Hub console to identify the non-standard and missing clauses in a contract.Create a clause mapping AI Admin Hub console to map question groups of a use case to active clauses in the clause library to display suggestions for non-standard clauses in a contract.Create an expected response mapping in the AI Admin Hub console to map questions of a use case to an expected response to identify the non-standard clause in a contract.Create a use case mapping in the AI Admin Hub console to map a use case to specific tables and define conditions to apply the use case for contract analysis.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Default large language model provider](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

The default model provider for contract metadata extraction, contract analysis, and contract obligation extraction is Azure OpenAI.


 -   **[Improved missing clause detection](https://www.servicenow.com/docs/access?context=cncore-NA-review-land&family=zurich&ft:locale=en-US)**

Missing clause detection in contract revision using the contract analysis skill has been enhanced for accuracy. The setup, configuration, and review experience remains unchanged across all supported workspaces.


 -   **[Configure use case mappings for metadata and obligation extraction](https://www.servicenow.com/docs/access?context=cmpro-na-usecase-mappings-me&family=zurich&ft:locale=en-US)**

Clear the **Contracts created from contract request** check box on the use case mapping forms for the contract metadata extraction and contract obligation extraction skills to extract metadata and obligations form signed contracts that are uploaded directly on a contract record.

-   **[Use conversational contract search and insights](https://www.servicenow.com/docs/access?context=cmpro-agentic-use-conv-search&family=zurich&ft:locale=en-US)**

The Now Assist powered conversational search feature's improved experience enables you to:

    -   View results in a listing view, making it easier to scan, compare, and navigate contract information.
    -   Open contract documents directly from the search results and perform an in‐document search.
The conversational search feature does not support searching within contract documents that are scanned PDFs.


 -   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


 -   **[Some generative AI skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Enhanced Manage contract repository agentic workflow](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&family=zurich&ft:locale=en-US)**

The manage contract repository agentic workflow has been optimized for enhanced performance. It now utilizes a single agent, the Contract Repository AI agent to extract both contract metadata and obligations from signed contracts, and retrieve required information to calculate the contract reminder date.

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&family=zurich&ft:locale=en-US)**

Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


 -   **[Extract metadata from signed contracts automatically](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&family=zurich&ft:locale=en-US)**

Use the AI agents in the manage contract repository agentic workflow to automatically extract metadata from signed contracts and calculate the contract reminder dates for contract renewal or termination. You can review the AI results in the contract playbook and update it if necessary before saving it.

-   **[Contract metadata extraction use cases](https://www.servicenow.com/docs/access?context=metadata-extraction-use-case&family=zurich&ft:locale=en-US)**

Support for 14 additional metadata fields in the CM Pro - Contract Metadata Extraction use case is available in the base system.


 -   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


</td></tr><tr><td>

Australia

</td><td>

-   **[Search in contracts document](https://www.servicenow.com/docs/access?context=cmpro-na-converse-ask-ques-new&family=australia&ft:locale=en-US)**

Contract document-based conversational search queries now return all matching results instead of 10 results. Use show more option to load the remaining results.

-   **[Search in contract metadata](https://www.servicenow.com/docs/access?context=cmpro-na-search-metadata&family=australia&ft:locale=en-US)**

In conversational search, introduced an option to preform in-document search after the contract metadata search results are available.


 -   **[ServiceNow AI implementation](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


 -   **[Default large language model provider](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

The default model provider for contract metadata extraction, contract analysis, and contract obligation extraction is Azure OpenAI.

-   **[Improved missing clause detection](https://www.servicenow.com/docs/access?context=cncore-NA-review-land&family=australia&ft:locale=en-US)**

Missing clause detection in contract revision using the contract analysis skill has been enhanced for accuracy. The setup, configuration, and review experience remains unchanged across all supported workspaces.


 -   **[Configure use case mappings for metadata and obligation extraction](https://www.servicenow.com/docs/access?context=cmpro-na-usecase-mappings-me&family=australia&ft:locale=en-US)**

Clear the **Contracts created from contract request** check box on the use case mapping forms for the contract metadata extraction and contract obligation extraction skills to extract metadata and obligations from signed contracts that are uploaded directly on a contract record.

-   **[Conversational contract search and insights](https://www.servicenow.com/docs/access?context=cmpro-agentic-workflows&family=australia&ft:locale=en-US)**

The conversational search feature's improved experience enables you to:

    -   View results in a listing view, making it easier to scan, compare, and navigate contract information.
    -   Open contract documents directly from the search results and perform an in‐document search.
The conversational search feature does not support searching within contract documents that are scanned PDFs.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Search in contracts document](https://www.servicenow.com/docs/access?context=cmpro-na-converse-ask-ques-new&family=brazil&ft:locale=en-US)**

Contract document-based conversational search queries now return all matching results instead of 10 results. Use Show more option to load the remaining results.

-   **[Search in contract metadata](https://www.servicenow.com/docs/access?context=cmpro-na-search-metadata&family=brazil&ft:locale=en-US)**

In conversational search, introduced an option to preform in-document search after the contract metadata search results are available.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some ServiceNow Otto for Contract Management Pro features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some ServiceNow Otto for Contract Management Pro features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Brazil

</td><td>

-   **Now LLM Service**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow Otto for Contract Management Pro.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Contract Management Pro - Prime by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Contract Management Pro - Prime is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Contract Management Pro - Prime by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto for Contract Management Pro we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow Otto for Contract Management Pro we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ServiceNow Otto for Contract Management Pro, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow Otto for Contract Management Pro we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow Otto for Contract Management Pro we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

[\[Placeholder link text to key australia-patch-6\]](https://www.servicenow.com/docs/access?context=australia-patch-6&family=australia&ft:locale=en-US)

-   Contract Management Pro MCP Server to retrieve the approved contract analysis playbook for external AI tools, enabling the use of organization's standard terms and approved clause language when reviewing contracts.
-   Contract document-based conversational search queries now return all matching results instead of 10 results. Use Show more option to load the remaining results.
-   In conversational search, introduced an option to preform in-document search after the contract metadata search results are available.

 [Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Contract Management Pro. Check your entitlements to determine your access to specific features.
-   Export conversational search results in multiple file formats.

 [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Identify missing clauses in contract revisions with improved accuracy.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Provide feedback on AI contract analysis results to help improve the AI accuracy.
-   Navigate directly to non-standard clause locations in a document when reviewing AI suggestions in the Microsoft Word add-in.
-   Configure use case mappings to extract metadata and obligations from a signed contract that is uploaded directly on a contract record.
-   Use AI powered conversational search to query contract documents using natural language and dialogue-driven queries, making it easier to find relevant information.

 See [\[Placeholder link text to key bundle-emplsm.cncore-now-assit-landing\]](https://www.servicenow.com/docs/access?context=cncore-now-assit-landing&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Minimize the deviations and reduce the turnaround time by identifying non-standard and missing clauses from the contract document.
-   Automatically extract the key metadata from signed contracts and update the contract repository, which improves accuracy and efficiency.
-   Locate contract information and insights using natural language queries across both contract metadata and signed documents. This enables quick summarization and retrieval of contract information.
-   Extract metadata and obligations from signed contracts, calculate reminder dates based on contract terms, and enable users to review and approve extracted information through a playbook interface before updating the contract repository.
-   Review contract documents in external AI tools using organizational playbook guidance from . AI-proposed redlines follow approved playbooks rather than general guidance.

 See [AI capabilities in Contract Management Pro](https://www.servicenow.com/docs/access?context=cncore-exp-now-assist-land&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-yokohama-brazil/rn-combined-intro.md)

