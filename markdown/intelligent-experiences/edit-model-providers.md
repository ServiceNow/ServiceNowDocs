---
title: Manage model providers
description: Edit or customise the model provider for a skill or skill group at the instance level from the list of supported third party model providers, including the default Now LLM Service. You can also review the model policy set by your organisation, and view the change history here.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-02"
reading_time_minutes: 2
keywords: [Edit LLM provider, web search]
breadcrumb: [Manage AI models, Now Assist Admin Settings, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Manage model providers

Edit or customise the model provider for a skill or skill group at the instance level from the list of supported third party model providers, including the default Now LLM Service. You can also review the model policy set by your organisation, and view the change history here.

## Before you begin

Role required: admin

Let's take an example of editing the model provider for skill group.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin**.

2.  Navigate to **Settings** &gt; **Manage AI models**.

3.  Select **Manage model providers**.

    ![Manage model providers](../image/na-admin-edit-model-providers.png)

4.  Select **Edit model provider** to edit the model provider for the instance or customize it to update it at the skill or skill group level.

5.  Select **Instance** scope to update the model provider for all the skills and skill groups in the instance.

    1.  Choose the **Default model provider** and select **Save and activate** to update your selection.

        The impacted skills and skill groups will display alongside.

    2.  Select **Save** to update the model provider.

        You will receive a confirmation message if you have reviewed the change and the impact.

        **Note:** The agreement acceptance message is displayed only for the first time user.

6.  Edit the model provider for a skill or skill group, after selecting the instance level model provider.

    This customization will override the instance level selection and update all capabilities associated with that group.

7.  Select **Customize** to select the model provider for a particular skill or skill group.

    ![Custom edit model provider](../image/na-admin-edit-model-custom.png)

    1.  Select the **Default model provider** for specific skill or skill group.

        Select the skill group as **AI agents** to change the model provider for **Now Assist in Virtual Agent**.

    2.  Select **Save and activate** to update your selection.

    **Note:** The Websearch AI search answers skill is only compatible with Google Gemini as the LLM provider. If you want to change the LLM provider to Azure OpenAI for this skill, see [Configure AI Search answers capability for web search](../../generative-ai-controller/task/configure-ai-search-answers-capability-for-web-search.md) for more information.

8.  Select **Cancel, go back** to revert or **Yes, activate** to save the updates.

    The status summary of skills for which the model provider change updated successfully or failed, displays.

9.  Review and accept the consent modal message to accept the terms for changing the region scope of the selected model provider.

    There are certain market regions restricted for particular model providers. The region scope must be changed to global location for the skills to be able to use the selected model provider.

10. Select **Yes, activate** to accept and apply the selection.

    You receive a message confirming model provider selection. The selection will also notify if any of the skills within that capability are not updated with the selection.

    **Note:** The skill and skill level customizations are overwritten once you update the model providers at the instance level.

    You can also select **Cancel, go back** to review or reject the changes.

11. Follow similar steps for editing the model provider for a particular skill.


**Parent Topic:**[Manage AI models](manage-large-language-models.md)

