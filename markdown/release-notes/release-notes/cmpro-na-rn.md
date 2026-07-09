---
title: Now Assist in Contract Management release notes
description: The ServiceNow Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-07-07"
reading_time_minutes: 11
---

# Now Assist in Contract Management release notes

The ServiceNow® Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligationsfrom signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Zurich release.

## Now Assist in Contract Management highlights for the Zurich release

[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

-   Identify missing clauses in contract revisions with improved accuracy.

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Provide feedback on Now Assist contract analysis results to help improve the AI accuracy.
-   Navigate directly to non-standard clause locations in a document when reviewing Now Assist suggestions in the Microsoft Word add-in.
-   Configure use case mappings to extract metadata and obligations from a signed contract that is uploaded directly on a contract record.
-   Use Now Assist powered conversational search to query contract documents using natural language and dialogue-driven queries, making it easier to find relevant information.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Use AI-powered obligation extraction to automatically identify and capture key obligations from signed contracts, and then review, edit, approve, or reject them within the contract playbook to create obligation records automatically.
-   Activate the Contract obligation extraction skill in the Now Assist Admin console to enable automatic obligation extraction.
-   Use Now Assist powered conversational search to query contract documents using natural language and dialogue-driven queries, making it easier to find relevant information.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Use the contract playbook to review and update the AI extracted metadata and reminder date for contract renewal or termination.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.

See [Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-now-assit-landing.md) for more information.

**Important:** Now Assist in Contract Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist in Contract Management to Zurich

If you're upgrading to Now Assist in Contract Management from Yokohama \(Patch 2 and lower\) or Xanadu \(Patch 8 and lower\), and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.
2.  In the **Name** field, search for `Upsert DI skill config`.
3.  In the script, add the use case IDs that you want to migrate to the Now Assist Admin console.
4.  Select **Run Fix Script**.

For more information, see [Post-upgrade steps for Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-na-upgrade-steps.md).

## New in the Zurich release

-   **[Feedback for Now Assist contract analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-review-contract-document.md)**

    Provide feedback on AI-identified non-standard and missing clauses to help improve AI accuracy over time. When reviewing contracts using Now Assist contract analysis, you can indicate whether the AI suggestions were helpful or not helpful by using the thumbs up or thumbs down feedback options. You can also provide optional qualitative feedback with comments. The feedback option is available in both the workspace and Microsoft Word add-in.

    The feedback provided on each clause is captured in the **Contracts Gen AI Feedback** table.

-   **[Automatically navigate to non-standard clauses in Microsoft Word add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-review-contract-document.md)**

    Locate non-standard clauses easily in Microsoft Word. The document scrolls to the relevant section using AI citations when you select a Now Assist suggestion in the Microsoft Word add-in.


-   **[Automated obligation extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-na-reminder-agentic-wf.md#section_tgm_mt3_dhc)**

    Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Using contract playbook to review AI-extracted obligations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-na-review-obligations.md)**

    Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **[Contract obligation extraction skill in Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-conf-obligation-extraction.md)**

    Configure and map use cases for obligation extraction skill in the Now Assist Admin console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Conversational contract search and insights Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-agentic-use-conv-search.md)**

    Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

    The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-llm-model-updates.md)**

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[Using contract playbook to review AI-extracted metadata and contract reminder date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-na-review-ai.md)**

    Use the playbook within a contract repository record to review the metadata extracted by the AI agents in the manage contract repository agentic workflow. You can make necessary changes to the extracted information, and submit it to update the contract repository. If the contract end date is available, the **Review contract reminders** tab appears in the playbook, enabling you to review and update the AI-calculated contract reminder date and specify recipients for contract renewal or terminations.

-   **[New third-party AI model provider options available for all AI applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.

-   **[New third-party AI model provider options available for all AI applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.

-   **[Select large language models for use cases in Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-na-manage-llm.md)**

    Select a large language model \(LLM\) provider for a contract analysis or metadata extraction use case. The selected LLM is applicable only for the specific use case and overrides the LLM selected for Now Assist in Contract Management skills.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Default large language model provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

    The default model provider for contract metadata extraction, contract analysis, and contract obligation extraction is Azure OpenAI.


-   **[Improved missing clause detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-NA-review-land.md)**

    Missing clause detection in contract revision using the contract analysis skill has been enhanced for accuracy. The setup, configuration, and review experience remains unchanged across all supported workspaces.


-   **[Configure use case mappings for metadata and obligation extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-na-usecase-mappings-me.md)**

    Clear the **Contracts created from contract request** check box on the use case mapping forms for the contract metadata extraction and contract obligation extraction skills to extract metadata and obligations form signed contracts that are uploaded directly on a contract record.

-   **[Conversational contract search and insights Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-agentic-use-conv-search.md)**

    The Now Assist powered conversational search feature's improved experience enables you to:

    -   View results in a listing view, making it easier to scan, compare, and navigate contract information.
    -   Open contract documents directly from the search results and perform an in‐document search.
    The conversational search feature does not support searching within contract documents that are scanned PDFs.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Enhanced Manage contract repository agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-na-reminder-agentic-wf.md)**

    The manage contract repository agentic workflow has been optimized for enhanced performance. It now utilizes a single agent, the Contract Repository AI agent to extract both contract metadata and obligations from signed contracts, and retrieve required information to calculate the contract reminder date.

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


-   **[Extract metadata from signed contracts automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cmpro-na-reminder-agentic-wf.md)**

    Use the AI agents in the manage contract repository agentic workflow to automatically extract metadata from signed contracts and calculate the contract reminder dates for contract renewal or termination. You can review the AI results in the contract playbook and update it if necessary before saving it.

-   **[Contract metadata extraction use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/metadata-extraction-use-case.md)**

    Support for 14 additional metadata fields in the CM Pro - Contract Metadata Extraction use case is available in the base system.


## Activation information

Install Now Assist in Contract Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn't supported in Microsoft Internet Explorer.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/cncore-cmpro-landing-page.md)**

    Use Contract Management Pro to set up contract document templates, clauses, clause variations, and to initiate contract requests. It also supports Now Assist - driven contract analysis and metadata extraction, e-signatures, wet signatures, and external storage systems.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    The Now Assist Admin console provides you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Contract Management Pro release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/cmpro-rn.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

