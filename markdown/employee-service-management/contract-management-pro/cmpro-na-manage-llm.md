---
title: Select large language models for use cases in Now Assist in Contract Management
description: Select a large language model \(LLM\) provider for a contract analysis or metadata extraction use case.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Set LLM for Now Assist skills, Set LLM at skill level]
breadcrumb: [Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Select large language models for use cases in Now Assist in Contract Management

Select a large language model \(LLM\) provider for a contract analysis or metadata extraction use case.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_admin

## About this task

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

In Now Assist in Contract Management, you can select the LLM provider at the use case level. This selected LLM is applicable only for the use case and overrides the LLM selected at the skill level.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  On the tile of your activated skill that you want to modify, select **Edit** in the options menu \(![Options menu icon.](../image/cmpro-na-three-dot-icon.png)\).

    ![Now Assist skills in Contract Management Pro.](../image/cmpro-na-active-skills.png "Active skills in Contract Management Pro")

4.  In the skill guided setup, select **Use cases**.

5.  Open the use case for which you want to set the LLM.

6.  Select the settings icon \(![Settings icon.](../../workplace-space-mapping/images/gear-icon.png)\).

    ![Settings in the Use case page.](../image/cmpro-na-use-case-gear.png "Use case settings")

7.  In the Settings window, select **Manage LLMs**.

    ![Manage LLM Provider in use case settings.](../image/cmpro-na-llm-setting.png "Manage LLMs")

8.  From the LLM provider drop-down list, select the LLM provider.

9.  In the Settings window, select **Save**.

10. In the use cases page, select **Save and continue**.

11. In the Review and activate page, select **Done**.


## Result

The LLM provider is set for the use case and is used for contract analysis or metadata extraction where this use case is applicable.

**Parent Topic:**[Configure Now Assist in Contract Management](confg-na-in-cmpro.md)

**Related topics**  


[Configure data permissions for Now Assist skills](cmpro-conf-roles-skills.md)

[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)

[Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md)

[Configuring contract obligation extraction](cncore-conf-obligation-extraction.md)

[Configuring agentic workflows in Now Assist in Contract Management](../concept/cmpro-conf-agentic-workflow.md)

[Post-upgrade steps for Now Assist in Contract Management](cmpro-na-upgrade-steps.md)

[Configure Now Assist in Contract Management](confg-na-in-cmpro.md)

[Create use cases for contract metadata extraction](cmpro-na-usecase-me.md)

[Create use cases for contract analysis](cmpro-na-usecase-ca.md)

