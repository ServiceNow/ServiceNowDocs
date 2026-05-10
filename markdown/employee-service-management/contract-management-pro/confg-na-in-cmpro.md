---
title: Configure Now Assist in Contract Management
description: As an AI administrator for contracts, you can configure Now Assist in Contract Management so that contract fulfillers can use the Now Assist capabilities while working on contract documents or search the contracts for information from the Now Assist panel.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [activate now assist in contract management, activate now assist in contract management pro, now assist in contract management pro, now assist for contract management pro, Now Assist in contract management pro, Now Assist for contract management pro, AI for contract management pro, AI in contract management pro]
breadcrumb: [Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure Now Assist in Contract Management

As an AI administrator for contracts, you can configure Now Assist in Contract Management so that contract fulfillers can use the Now Assist capabilities while working on contract documents or search the contracts for information from the Now Assist panel.

## Before you begin

Ensure that the application is in Global or Now Assist in Contract Management scope.

Role required: sn\_cm\_gen\_ai.ai\_contract\_admin

## About this task

Use the Now Assist Admin console to configure Now Assist in Contract Management. The console contains everything that you need to configure the Now Assist skills. For more information, see [Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

The following skills are available for Contract Management Pro in the Now Assist Admin console:

-   Contract metadata extraction
-   Contract obligation extraction
-   Contract analysis

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

## Procedure

1.  Install the Contract Management Pro - Prime plugin \(sn\_cm\_ai\_prime\).

    For information about the plugin installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

3.  Navigate to **Employee** &gt; **CM Pro**.

4.  Select **Activate skill** on the skill you want to activate.

    ![Now Assist skills available for Contract Management Pro.](../image/cmpro-NA-skills.png "Now Assist skills for Contract Management Pro")

5.  In the skill guided setup, configure the use cases and other mappings for the skill.

    For more information on configuring contract metadata extraction, see [Configuring contract metadata extraction](cncore-conf-metadata-extraction.md).

    For more information on configuring contract obligation extraction, see [Configuring contract obligation extraction](cncore-conf-obligation-extraction.md).

    For more information on configuring contract analysis, see [Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md).

6.  In the Define access page, select the roles to specify who can access the skills.

    -   If custom roles were added before upgrading to Now Assist in Contract Management Australia patch 1, they are updated automatically by a script and appear in the Define access page.
    -   If custom roles were not added, the default role sn\_cm\_gen\_ai.ai\_contract\_fulfiller, sn\_cm\_gen\_ai.ai\_contract\_admin, and sn\_cm\_gen\_ai.ai\_contract\_config automatically appear in the Define access page.
    -   If new roles are created after the upgrade, add them manually in the Define access page.
7.  In the Review and activate page, select **Activate**.


## Result

The Now Assist skill is activated for Contract Management Pro.

You can update or deactivate the skill by selecting **Edit** and **Deactivate** the options menu icon \(![Options menu icon.](../image/cmpro-na-three-dot-icon.png)\) of the active skill. For more information, see [Deactivate skills for Now Assist in Contract Management](cmpro-deactivate-na-skills.md).

## What to do next

[Configure data permissions for Now Assist skills](cmpro-conf-roles-skills.md)

-   **[Configure data permissions for Now Assist skills](cmpro-conf-roles-skills.md)**  
Add the user roles for a Now Assist skill to specify the roles that Now Assist uses to access data while performing a task. The user roles control the information that Now Assist can read, update, or share, based on the permissions of the selected roles.
-   **[Select large language models for use cases in Now Assist in Contract Management](cmpro-na-manage-llm.md)**  
Select a large language model \(LLM\) provider for a contract analysis or metadata extraction use case.
-   **[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)**  
Configure system properties and use cases for metadata extraction so that a contract manager can use Now Assist to extract metadata from a contract and add the extracted information to the contract repository.
-   **[Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md)**  
Configure use cases with associated field groups and fields, and map them to clauses and expected responses. Now Assist uses the applicable use case to analyze a contract document and identify non-standard and missing clauses.
-   **[Configuring contract obligation extraction](cncore-conf-obligation-extraction.md)**  
Configure and map use cases for the contract obligation extraction skill in the Now Assist Admin console to automatically extract key contractual obligations from signed contracts.
-   **[Configuring agentic workflows in Now Assist in Contract Management](../concept/cmpro-conf-agentic-workflow.md)**  
Configure agentic workflows in Now Assist in Contract Management so that contract fulfillers can use the AI agents to perform specific tasks autonomously.
-   **[Post-upgrade steps for Now Assist in Contract Management](cmpro-na-upgrade-steps.md)**  
If you are upgrading to Now Assist in Contract Management from Yokohama \(Patch 2 and lower\) or Xanadu \(Patch 8 and lower\), and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.

**Parent Topic:**[Now Assist in Contract Management](../concept/cncore-now-assit-landing.md)

