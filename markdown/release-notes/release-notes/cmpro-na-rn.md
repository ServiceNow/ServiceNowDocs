---
title: Now Assist in Contract Management release notes
description: The ServiceNow Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-03-13"
reading_time_minutes: 10
---

# Now Assist in Contract Management release notes

The ServiceNow® Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligationsfrom signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.

## Now Assist in Contract Management highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

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

See [Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-now-assit-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

**Important:** Now Assist in Contract Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist in Contract Management to Yokohama

If you’re upgrading to Now Assist in Contract Management starting with Yokohama Patch 3 from a previous version and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.
2.  In the **Name** field, search for `Upsert DI skill config`.
3.  In the script, add the use case ids that you want to migrate to the Now Assist Admin console.
4.  Select **Run Fix Script**.

For more information, see [Post-upgrade steps for Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cmpro-na-upgrade-steps&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

## New in the Yokohama release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Automated obligation extraction](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US#section_tgm_mt3_dhc)**

    Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Using contract playbook to review AI-extracted obligations](https://www.servicenow.com/docs/access?context=cmpro-na-review-obligations&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **[Contract obligation extraction skill in Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-conf-obligation-extraction&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Configure and map use cases for obligation extraction skill in the Now Assist Admin console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Conversational contract search and insights Workflow](https://www.servicenow.com/docs/access?context=cmpro-agentic-use-conv-search&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

    The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://www.servicenow.com/docs/access?context=now-llm-model-updates&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[Reviewing AI-extracted results in the playbook](https://www.servicenow.com/docs/access?context=cmpro-na-review-ai&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Use the playbook within a contract repository record to review the metadata extracted by the AI agents in the Manage contract repository agentic workflow. You can make necessary changes to the extracted information, and submit it to update the contract repository. If the contract end date is available, the **Review contract reminders** tab appears in the playbook, enabling you to review and update the AI-calculated contract reminder date and specify recipients for contract renewal or terminations.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Select large language models for use cases in Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cmpro-na-manage-llm&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Select a large language models \(LLM\) provider at for a contract analysis or metadata extraction use case. The selected LLM is applicable only for the specific use case and overrides the LLM selected for Now Assist in Contract Management skills.


-   **[Manage contract repository agentic workflow](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Use the Manage contract repository agentic workflow to improve productivity by autonomously creating milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.

    |Agentic workflows|Description|
    |-----------------|-----------|
    |Manage contract repository|Uses AI agents to retrieve contract details such as renewal notice period, termination notice period, or auto-renewal clause information, and determine the average lead time for similar contracts to create contract milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.|


## Changed in this release

-   **[Automated obligation extraction](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US#section_tgm_mt3_dhc)**

    Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Using contract playbook to review AI-extracted obligations](https://www.servicenow.com/docs/access?context=cmpro-na-review-obligations&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **[Contract obligation extraction skill in Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-conf-obligation-extraction&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Configure and map use cases for obligation extraction skill in the Now Assist Admin console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Conversational contract search and insights Workflow](https://www.servicenow.com/docs/access?context=cmpro-agentic-use-conv-search&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

    The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://www.servicenow.com/docs/access?context=now-llm-model-updates&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[Extract metadata from signed contracts automatically](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Use the AI agents in the Manage contract repository agentic workflow to automatically extract metadata from signed contracts and calculate the contract reminder dates for contract renewal or termination. You can review the AI results in the contract playbook and update it if necessary before saving it.

-   **[Contract metadata extraction use cases](https://www.servicenow.com/docs/access?context=metadata-extraction-use-case&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Support for 14 additional metadata fields in the CM Pro - Contract Metadata Extraction use case available in the base system.


-   **[Configuring contract metadata extraction](https://www.servicenow.com/docs/access?context=cncore-conf-metadata-extraction&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Create a use case and its associated fields for contract metadata extraction in the Now Assist Admin console to define the information that you want Now Assist to detect in a signed contract.

    Create a use case mapping in the Now Assist Admin console to map a use case to specific tables and define conditions to apply the use case for metadata extraction.

-   **[Configuring contract analysis](https://www.servicenow.com/docs/access?context=cmpro-conf-contract-analysis&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Create a use case and its associated question groups for contract analysis in the Now Assist Admin console to identify the non-standard and missing clauses in a contract.

    Create a clause mapping Now Assist Admin console to map question groups of a use case to active clauses in the clause library to display suggestions for non-standard clauses in a contract.

    Create an expected response mapping in the Now Assist Admin console to map questions of a use case to an expected response to identify the non-standard clause in a contract.

    Create a use case mapping in the Now Assist Admin console to map a use case to specific tables and define conditions to apply the use case for contract analysis.


## Activation information

Now Assist in Contract Management is a ServiceNow AI Platform feature that is available with activation of the Now Assist in Contract Management \(sn\_cm\_gen\_ai\). For details, see [Configure Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=confg-na-in-cmpro&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

## Related ServiceNow applications and features

-   **[Contract Management Pro](https://www.servicenow.com/docs/access?context=cncore-cmpro-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Use Contract Management Pro to set up contract document templates, clauses, clause variations, and to initiate contract requests. It also supports Now Assist - driven contract analysis and metadata extraction, e-signatures, wet signatures, and external storage systems.

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Contract Management Pro release notes](cmpro-rn.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

