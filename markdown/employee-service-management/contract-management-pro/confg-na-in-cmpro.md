---
title: Configure Now Assist in Contract Management
description: As an AI administrator for contracts, you can configure Now Assist in Contract Management so that contract fulfillers can use the Now Assist capabilities while working on contract documents or search the contracts for information from the Now Assist panel.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [activate now assist in contract management, activate now assist in contract management pro, now assist in contract management pro, now assist for contract management pro, Now Assist in contract management pro, Now Assist for contract management pro, AI for contract management pro, AI in contract management pro]
breadcrumb: [Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Configure Now Assist in Contract Management

As an AI administrator for contracts, you can configure Now Assist in Contract Management so that contract fulfillers can use the Now Assist capabilities while working on contract documents or search the contracts for information from the Now Assist panel.

## Before you begin

Ensure that Contract Management Pro \(sn\_cm\_pro\) and Contract Workspace \(sn\_cm\_workspace\) are installed before installing Now Assist in Contract Management.

Ensure that the application is in Global or Now Assist in Contract Management scope.

Role required: sn\_cm\_gen\_ai.ai\_contract\_admin

## About this task

Use the Now Assist Admin console to configure Now Assist in Contract Management. The console contains everything that you need to configure the Now Assist skills. For more information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

The following table lists the feature and skills available for Contract Management Pro in the Now Assist Admin console.

<table id="table_xpw_w43_t2c"><thead><tr><th>

Features

</th><th>

Skills

</th></tr></thead><tbody><tr><td>

Contract Management Pro

</td><td>

-   Contract metadata extraction
-   Contract obligation extraction
-   Contract analysis

</td></tr></tbody>
</table>The Conversational contract search and insights skill is listed in the **Other** category of Now Assist skills page. To configure it, see [Configure Conversational contract search and insights](cncore-conf-converse-skill.md).

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\).

    -   For information about the plugin installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
    -   For information about the plugin dependencies and plugin activation order, see [Application information](../concept/cncore-support-info-na.md#cmpro-na-app-info).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

3.  Navigate to **Employee** &gt; **CM Pro**.

4.  On the tile for your skill, select **Activate skill**.

    ![Now Assist skills available for Contract Management Pro.](../image/cmpro-NA-skills.png "Now Assist skills for Contract Management Pro")

5.  In the skill guided setup, configure the use cases and other mappings for the skill.

    For more information on configuring contract metadata extraction, see [Configuring contract metadata extraction](cncore-conf-metadata-extraction.md).

    For more information on configuring contract obligation extraction, see [Configuring contract obligation extraction](cncore-conf-obligation-extraction.md).

    For more information on configuring contract analysis, see [Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md).

6.  In the Define access page, select the roles to specify who can access the skills.

    -   If custom roles were added before upgrading to Now Assist in Contract Management Yokohama patch 1, they are updated automatically by a script and appear in the Define access page.
    -   If custom roles were not added, the default role sn\_cm\_gen\_ai.ai\_contract\_fulfiller, sn\_cm\_gen\_ai.ai\_contract\_admin, and sn\_cm\_gen\_ai.ai\_contract\_config automatically appear in the Define access page.
    -   If new roles are created after the upgrade, add them manually in the Define access page.
7.  In the Review and activate page, select **Activate**.


## Result

The Now Assist skill is activated for Contract Management Pro.

You can update or deactivate the skill by selecting **Edit** and **Deactivate** the options menu icon \(![Options menu icon.](../image/cmpro-na-three-dot-icon.png)\) of the active skill. For more information, see [Deactivate skills for Now Assist in Contract Management](cmpro-deactivate-na-skills.md).

## What to do next

[Configure data permissions for Now Assist skills](cmpro-conf-roles-skills.md)

-   **[Select large language models for use cases in Now Assist in Contract Management](cmpro-na-manage-llm.md)**  
Select a large language model \(LLM\) provider for a contract analysis or metadata extraction use case.
-   **[Configure data permissions for Now Assist skills](cmpro-conf-roles-skills.md)**  
Add the user roles for a Now Assist skill to specify the roles that Now Assist uses to access data while performing a task. The user roles control the information that Now Assist can read, update, or share, based on the permissions of the selected roles.
-   **[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)**  
Configure system properties and use cases for metadata extraction so that a contract manager can use Now Assist to extract metadata from a contract and add the extracted information to the contract repository.
-   **[Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md)**  
Configure use cases with associated field groups and fields, and map them to clauses and expected responses. Now Assist uses the applicable use case to analyze a contract document and identify non-standard and missing clauses.
-   **[Configuring contract obligation extraction](cncore-conf-obligation-extraction.md)**  
Configure and map use cases for the contract obligation extraction skill in the Now Assist Admin console to automatically extract key contractual obligations from signed contracts.
-   **[Configuring agentic workflows in Now Assist in Contract Management](../concept/cmpro-conf-agentic-workflow.md)**  
Configure agentic workflows in Now Assist in Contract Management so that contract fulfillers can use the AI agents to perform specific tasks autonomously.
-   **[Post-upgrade steps for Now Assist in Contract Management](cmpro-na-upgrade-steps.md)**  
If you are upgrading to Now Assist in Contract Management starting with Yokohama \(Patch 3\) from a previous version and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.

**Parent Topic:**[Now Assist in Contract Management](../concept/cncore-now-assit-landing.md)

