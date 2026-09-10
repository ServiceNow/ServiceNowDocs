---
title: Now Assist in Contract Management release notes
description: The ServiceNow Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.The ServiceNow Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.The ServiceNow Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.The ServiceNow Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.The ServiceNow Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligations from signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-03-13"
reading_time_minutes: 10
---

# Now Assist in Contract Management release notes

The ServiceNow® Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligationsfrom signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.

## About Now Assist in Contract Management

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills are now turned on by default.
-   Use AI-powered obligation extraction to automatically identify and capture key obligations from signed contracts, and then review, edit, approve, or reject them within the contract playbook to create obligation records automatically.
-   Activate the Contract obligation extraction skill in the AI Admin Hub console to enable automatic obligation extraction.
-   Use Now Assist powered conversational search to query contract documents using natural language and dialogue-driven queries, making it easier to find relevant information.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use the contract playbook to review and update the AI extracted metadata and reminder date for contract renewal or termination.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

Yokohama Patch 3

-   Activate and configure the contract metadata extraction skill for Contract Management Pro in the AI Admin Hub console.
-   Activate and configure the contract analysis skill for Contract Management Pro in the AI Admin Hub console.
-   Use the Manage contract repository agentic workflow to autonomously set milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.

See  for more information.

## Activation and other requirements

**Important:** Now Assist in Contract Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Now Assist in Contract Management is a ServiceNow AI Platform feature that is available with activation of the Now Assist in Contract Management \(sn\_cm\_gen\_ai\). For details, see .

-   **Upgrade information**

    If you’re upgrading to Now Assist in Contract Management starting with Yokohama Patch 3 from a previous version and you have customized use cases, run a fix script to migrate the existing data to the AI Admin Hub console.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.
    2.  In the **Name** field, search for `Upsert DI skill config`.
    3.  In the script, add the use case ids that you want to migrate to the AI Admin Hub console.
    4.  Select **Run Fix Script**.
    For more information, see .

-   **Browser requirements**

    Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.


**Parent Topic:**[Contract Management Pro release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/cmpro-rn.md)

## December 2025

The ServiceNow® Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligationsfrom signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.

### What's new

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **Automated obligation extraction**

    Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **Using contract playbook to review AI-extracted obligations**

    Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **Contract obligation extraction skill in Now Assist in Contract Management**

    Configure and map use cases for obligation extraction skill in the AI Admin Hub console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   ****

    Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

    The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-llm-model-updates.md)**

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


### What's changed

-   **Automated obligation extraction**

    Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **Using contract playbook to review AI-extracted obligations**

    Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **Contract obligation extraction skill in Now Assist in Contract Management**

    Configure and map use cases for obligation extraction skill in the AI Admin Hub console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   ****

    Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

    The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-llm-model-updates.md)**

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


## September 2025

The ServiceNow® Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligationsfrom signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.

### What's new

-   ****

    Use the playbook within a contract repository record to review the metadata extracted by the AI agents in the Manage contract repository agentic workflow. You can make necessary changes to the extracted information, and submit it to update the contract repository. If the contract end date is available, the **Review contract reminders** tab appears in the playbook, enabling you to review and update the AI-calculated contract reminder date and specify recipients for contract renewal or terminations.

-   **[New third-party AI model provider options available for all Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   ****

    Select a large language models \(LLM\) provider at for a contract analysis or metadata extraction use case. The selected LLM is applicable only for the specific use case and overrides the LLM selected for Now Assist in Contract Management skills.


## August 2025

The ServiceNow® Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligationsfrom signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.

### What's changed

-   **Extract metadata from signed contracts automatically**

    Use the AI agents in the Manage contract repository agentic workflow to automatically extract metadata from signed contracts and calculate the contract reminder dates for contract renewal or termination. You can review the AI results in the contract playbook and update it if necessary before saving it.

-   ****

    Support for 14 additional metadata fields in the CM Pro - Contract Metadata Extraction use case available in the base system.


## May 2025

The ServiceNow® Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligationsfrom signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.

### What's new

-   ****

    Use the Manage contract repository agentic workflow to improve productivity by autonomously creating milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.

    |Agentic workflows|Description|
    |-----------------|-----------|
    |Manage contract repository|Uses AI agents to retrieve contract details such as renewal notice period, termination notice period, or auto-renewal clause information, and determine the average lead time for similar contracts to create contract milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.|


### What's changed

-   ****

    Create a use case and its associated fields for contract metadata extraction in the AI Admin Hub console to define the information that you want Now Assist to detect in a signed contract.Create a use case mapping in the AI Admin Hub console to map a use case to specific tables and define conditions to apply the use case for metadata extraction.

-   ****

    Create a use case and its associated question groups for contract analysis in the AI Admin Hub console to identify the non-standard and missing clauses in a contract.Create a clause mapping AI Admin Hub console to map question groups of a use case to active clauses in the clause library to display suggestions for non-standard clauses in a contract.Create an expected response mapping in the AI Admin Hub console to map questions of a use case to an expected response to identify the non-standard clause in a contract.Create a use case mapping in the AI Admin Hub console to map a use case to specific tables and define conditions to apply the use case for contract analysis.


