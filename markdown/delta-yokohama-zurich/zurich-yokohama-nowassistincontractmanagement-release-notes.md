---
title: Combined Now Assist in Contract Management release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Now Assist in Contract Management from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-nowassistincontractmanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 13
breadcrumb: [Products combined by family]
---

# Combined Now Assist in Contract Management release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Now Assist in Contract Management from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist in Contract Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist in Contract Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

If you’re upgrading to Now Assist in Contract Management starting with Yokohama Patch 3 from a previous version and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.
2.  In the **Name** field, search for `Upsert DI skill config`.
3.  In the script, add the use case ids that you want to migrate to the Now Assist Admin console.
4.  Select **Run Fix Script**.

For more information, see [Post-upgrade steps for Now Assist in Contract Management](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-upgrade-steps&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

If you’re upgrading to Now Assist in Contract Management from Yokohama \(Patch 2 and lower\) or Xanadu \(Patch 8 and lower\), and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.
2.  In the **Name** field, search for `Upsert DI skill config`.
3.  In the script, add the use case IDs that you want to migrate to the Now Assist Admin console.
4.  Select **Run Fix Script**.

For more information, see [Post upgrade steps](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-upgrade-steps&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Now Assist in Contract Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Automated obligation extraction](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-reminder-agentic-wf&family=yokohama&ft:locale=en-US)**

Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Using contract playbook to review AI-extracted obligations](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-review-obligations&family=yokohama&ft:locale=en-US)**

Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **[Contract obligation extraction skill in Now Assist in Contract Management](https://servicenow-staging.fluidtopics.net/access?context=cncore-conf-obligation-extraction&family=yokohama&ft:locale=en-US)**

Configure and map use cases for obligation extraction skill in the Now Assist Admin console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Conversational contract search and insights Workflow](https://servicenow-staging.fluidtopics.net/access?context=cmpro-agentic-use-conv-search&family=yokohama&ft:locale=en-US)**

Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some Now Assist skills are turned on by default](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://servicenow-staging.fluidtopics.net/access?context=now-llm-model-updates&family=yokohama&ft:locale=en-US)**

-   **[Review AI results](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-review-ai&family=yokohama&ft:locale=en-US)**

Use the playbook within a contract repository record to review the metadata extracted by the AI agents in the Manage contract repository agentic workflow. You can make necessary changes to the extracted information, and submit it to update the contract repository. If the contract end date is available, the **Review contract reminders** tab appears in the playbook, enabling you to review and update the AI-calculated contract reminder date and specify recipients for contract renewal or terminations.

-   ****
-   **[Select large language models for use cases in Now Assist in Contract Management](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-manage-llm&family=yokohama&ft:locale=en-US)**

Select a large language models \(LLM\) provider at for a contract analysis or metadata extraction use case. The selected LLM is applicable only for the specific use case and overrides the LLM selected for Now Assist in Contract Management skills.


-   **[Manage contract repository agentic workflow](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-reminder-agentic-wf&family=yokohama&ft:locale=en-US)**

Use the Manage contract repository agentic workflow to improve productivity by autonomously creating milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.

    |Agentic workflows|Description|
    |-----------------|-----------|
    |Manage contract repository|Uses AI agents to retrieve contract details such as renewal notice period, termination notice period, or auto-renewal clause information, and determine the average lead time for similar contracts to create contract milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.|


</td></tr><tr><td>

Zurich

</td><td>

-   **[Automated obligation extraction](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-reminder-agentic-wf&family=zurich&ft:locale=en-US)**

Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Using contract playbook to review AI-extracted obligations](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-review-obligations&family=zurich&ft:locale=en-US)**

Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **[Contract obligation extraction skill in Now Assist in Contract Management](https://servicenow-staging.fluidtopics.net/access?context=cncore-conf-obligation-extraction&family=zurich&ft:locale=en-US)**

Configure and map use cases for obligation extraction skill in the Now Assist Admin console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Conversational contract search and insights Workflow](https://servicenow-staging.fluidtopics.net/access?context=cmpro-agentic-use-conv-search&family=zurich&ft:locale=en-US)**

Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some Now Assist skills are turned on by default](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://servicenow-staging.fluidtopics.net/access?context=now-llm-model-updates&family=zurich&ft:locale=en-US)**

-   **[Using contract playbook to review AI-extracted metadata and contract reminder date](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-review-ai&family=zurich&ft:locale=en-US)**

Use the playbook within a contract repository record to review the metadata extracted by the AI agents in the manage contract repository agentic workflow. You can make necessary changes to the extracted information, and submit it to update the contract repository. If the contract end date is available, the **Review contract reminders** tab appears in the playbook, enabling you to review and update the AI-calculated contract reminder date and specify recipients for contract renewal or terminations.

-   ****
-   **[Select LLMs](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-manage-llm&family=zurich&ft:locale=en-US)**

Select a large language model \(LLM\) provider for a contract analysis or metadata extraction use case. The selected LLM is applicable only for the specific use case and overrides the LLM selected for Now Assist in Contract Management skills.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Now Assist in Contract Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Automated obligation extraction](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-reminder-agentic-wf&family=yokohama&ft:locale=en-US)**

Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Using contract playbook to review AI-extracted obligations](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-review-obligations&family=yokohama&ft:locale=en-US)**

Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **[Contract obligation extraction skill in Now Assist in Contract Management](https://servicenow-staging.fluidtopics.net/access?context=cncore-conf-obligation-extraction&family=yokohama&ft:locale=en-US)**

Configure and map use cases for obligation extraction skill in the Now Assist Admin console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Conversational contract search and insights Workflow](https://servicenow-staging.fluidtopics.net/access?context=cmpro-agentic-use-conv-search&family=yokohama&ft:locale=en-US)**

Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   ****
-   **[Now LLM LTS support for Contract Management Pro](https://servicenow-staging.fluidtopics.net/access?context=now-llm-model-updates&family=yokohama&ft:locale=en-US)**

-   **[Extract metadata from signed contracts automatically](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-reminder-agentic-wf&family=yokohama&ft:locale=en-US)**

Use the AI agents in the Manage contract repository agentic workflow to automatically extract metadata from signed contracts and calculate the contract reminder dates for contract renewal or termination. You can review the AI results in the contract playbook and update it if necessary before saving it.

-   **[Contract metadata extraction use cases](https://servicenow-staging.fluidtopics.net/access?context=metadata-extraction-use-case&family=yokohama&ft:locale=en-US)**

Support for 14 additional metadata fields in the CM Pro - Contract Metadata Extraction use case available in the base system.


-   **[Configuring contract metadata extraction](https://servicenow-staging.fluidtopics.net/access?context=cncore-conf-metadata-extraction&family=yokohama&ft:locale=en-US)**

Create a use case and its associated fields for contract metadata extraction in the Now Assist Admin console to define the information that you want Now Assist to detect in a signed contract.

Create a use case mapping in the Now Assist Admin console to map a use case to specific tables and define conditions to apply the use case for metadata extraction.

-   **[Configuring contract analysis](https://servicenow-staging.fluidtopics.net/access?context=cmpro-conf-contract-analysis&family=yokohama&ft:locale=en-US)**

Create a use case and its associated question groups for contract analysis in the Now Assist Admin console to identify the non-standard and missing clauses in a contract.

Create a clause mapping Now Assist Admin console to map question groups of a use case to active clauses in the clause library to display suggestions for non-standard clauses in a contract.

Create an expected response mapping in the Now Assist Admin console to map questions of a use case to an expected response to identify the non-standard clause in a contract.

Create a use case mapping in the Now Assist Admin console to map a use case to specific tables and define conditions to apply the use case for contract analysis.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**




-   ****
-   **[Enhanced Manage contract repository agentic workflow](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-reminder-agentic-wf&family=zurich&ft:locale=en-US)**

The manage contract repository agentic workflow has been optimized for enhanced performance. It now utilizes a single agent, the Contract Repository AI agent to extract both contract metadata and obligations from signed contracts, and retrieve required information to calculate the contract reminder date.

-   ****

-   **[Extract metadata from signed contracts automatically](https://servicenow-staging.fluidtopics.net/access?context=cmpro-na-reminder-agentic-wf&family=zurich&ft:locale=en-US)**

Use the AI agents in the manage contract repository agentic workflow to automatically extract metadata from signed contracts and calculate the contract reminder dates for contract renewal or termination. You can review the AI results in the contract playbook and update it if necessary before saving it.

-   **[Contract metadata extraction use cases](https://servicenow-staging.fluidtopics.net/access?context=metadata-extraction-use-case&family=zurich&ft:locale=en-US)**

Support for 14 additional metadata fields in the CM Pro - Contract Metadata Extraction use case is available in the base system.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Now Assist in Contract Management features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Now Assist in Contract Management features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Now Assist in Contract Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Now Assist in Contract Management is a ServiceNow AI Platform feature that is available with activation of the Now Assist in Contract Management \(sn\_cm\_gen\_ai\). For details, see [Configure](https://servicenow-staging.fluidtopics.net/access?context=confg-na-in-cmpro&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Now Assist in Contract Management by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist in Contract Management we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Now Assist in Contract Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

</td></tr><tr><td>

Zurich

</td><td>

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Now Assist in Contract Management, such as specific requirements or compliance levels.

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

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Now Assist in Contract Management we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Now Assist in Contract Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills are now turned on by default.
-   Use AI-powered obligation extraction to automatically identify and capture key obligations from signed contracts, and then review, edit, approve, or reject them within the contract playbook to create obligation records automatically.
-   Activate the Contract obligation extraction skill in the Now Assist Admin console to enable automatic obligation extraction.
-   Use Now Assist powered conversational search to query contract documents using natural language and dialogue-driven queries, making it easier to find relevant information.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use the contract playbook to review and update the AI extracted metadata and reminder date for contract renewal or termination.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

 Yokohama Patch 3

-   Activate and configure the contract metadata extraction skill for Contract Management Pro in the Now Assist Admin console.
-   Activate and configure the contract analysis skill for Contract Management Pro in the Now Assist Admin console.
-   Use the Manage contract repository agentic workflow to autonomously set milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.

 See [Now Assist in CM Pro](https://servicenow-staging.fluidtopics.net/access?context=cncore-now-assit-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 5](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.

 [Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Some Now Assist skills are now turned on by default.
-   Use AI-powered obligation extraction to automatically identify and capture key obligations from signed contracts, and then review, edit, approve, or reject them within the contract playbook to create obligation records automatically.
-   Activate the Contract obligation extraction skill in the Now Assist Admin console to enable automatic obligation extraction.
-   Use Now Assist powered conversational search to query contract documents using natural language and dialogue-driven queries, making it easier to find relevant information.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

 [Zurich Patch 1](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Use the contract playbook to review and update the AI extracted metadata and reminder date for contract renewal or termination.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

 See [Now Assist in CM Pro](https://servicenow-staging.fluidtopics.net/access?context=cncore-now-assit-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

