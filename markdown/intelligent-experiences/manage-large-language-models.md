---
title: Manage large language models
description: Access and select the LLM \(large language model\) used for various Now Assist skills. The selection impacts all the skills within the capability.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-02-24"
reading_time_minutes: 1
keywords: [Manage, LLM, Large language model]
breadcrumb: [Configuring Now Assist settings and features, Now Assist, Enable AI experiences]
---

# Manage large language models

Access and select the LLM \(large language model\) used for various Now Assist skills. The selection impacts all the skills within the capability.

## Before you begin

Role required: admin, sn\_nowassist\_admin.nsa\_admin

To enable LLM provider selection, ensure that the skill is available in that region. For example, to update the LLM provider for Now Assist Q&amp;A Genius Results, ensure that all the skills under Conversational skills are available and active in the region.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  Select **Now Assist Features** to find the workflow for which you want to select the LLM provider.

3.  Find the available skills in the workflow and select **Turn on** to change the region scope and hence, enable skill.

    ![Now Assist admin - Change region scope for skill](../image/na-admin-manage-llm-turnon-region.png)

4.  Review the terms and conditions to accept or revert to the LLM provider change.

5.  Navigate to **Settings** &gt; **Manage LLMs**.

    ![Now Assist admin settings - Manage LLMs](../image/na-admin-settings-manage-llm.png)

6.  Select the Now Assist skill for which you want to update the LLM.

    Choose from Platform, Code generation or App generation skill.

7.  Select the LLM in the **Provider** dropdown.

    You can choose between Now LLM Service and Azure OpenAI. Note that Azure OpenAI primarily utilizes GPT-4.0 series of models from Open AI.

8.  Select **Save** to update the LLM.

    You will receive an agreement message before confirming the LLM selection.

    **Note:** The agreement acceptance message is displayed only for the first time user.

    ![Change region scope to global location](../image/na-admin-change-region-agreement.png)

9.  Review the [https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/deployment-types\#global-standard](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/deployment-types#global-standard) to agree or deny the LLM change.

    **Note:** Selecting Azure OpenAI required the Gen AI data processing location change from APJ \(Asia-Pacific and Japan\) to global location.

10. Select **I agree** to accept and apply the LLM selection.

    You receive a message confirming LLM provider selection for that capability. The selection will also notify if any of the skills within that capability are not updated with the selected LLM.


**Parent Topic:**[Configuring Now Assist settings and features](../concept/configuring-na-landing.md)

