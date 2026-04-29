---
title: Configure LLM to generate descriptions for conversational actions
description: Choose which LLM you want to use by default to generate descriptions for inputs, outputs, and skills for conversational actions.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Build actions, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Configure LLM to generate descriptions for conversational actions

Choose which LLM you want to use by default to generate descriptions for inputs, outputs, and skills for conversational actions.

## Before you begin

Role required: admin

## About this task

In the conversational actions settings, you can use generative AI to generate descriptions for skills, inputs, and outputs of a conversational action. You can select a default LLM to generate these descriptions out of any of the following preconfigured LLMs:

-   Anthropic Claude on AWS
-   Azure OpenAI
-   Google Gemini
-   Now LLM

**Note:** This configuration affects only the capability to generate the descriptions.

## Procedure

1.  Select **All**.

2.  In the **Filter** search box, enter `sys_one_extend_capability.list`.

3.  In the OneExtend Capabilities list, search for the application `Conversational subflows and actions`.

    ![OneExtend Capabilities page shows entries for input - output description generator and skill description generator.](../images/csa-llm-generate-description.png)

4.  Select the record for which you want to change the LLM:

    -   Input output description generator
    -   Skill description generator
    The **OneExtend Definition Configs** tab displays separate rows for each configured LLM. The following image shows one row each for Now LLM and Azure OpenAI.![Options to select the default LLM.](../images/csa-llm-list.png)

5.  In the **Default** column of your selected LLM, set the value as **true**.

    ![Selecting the default LLM for conversational subflows description generation skill.](../images/CSA-change-default-llm.png)

    Once you select the default LLM, ensure that the Default field value for any other LLM is set to **false**.

6.  Select **Update**.


**Parent Topic:**[Building actions](../concept/actions.md)

