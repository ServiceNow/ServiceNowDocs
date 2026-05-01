---
title: Configure AI model providers for Now Assist for Code skills
description: Select a large language model \(LLM\) as the AI service provider for Now Assist for Code skills.Select a large language model \(LLM\) as the AI service provider for Now Assist for Code skills in your instance.Select an AI model provider for specific skills within the script editor.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 3
breadcrumb: [Configure, Now Assist for Code, Scripting, API implementation, API implementation and reference]
---

# Configure AI model providers for Now Assist for Code skills

Select a large language model \(LLM\) as the AI service provider for Now Assist for Code skills.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

AI stewards can enable or disable AI model providers in the AI Control Tower. Administrators set the default AI model providers for Now Assist skills in your instance through the Now Assist Admin console. As a user, you can override the instance default AI model provider and select a different model provider for Now Assist for Code skills in the script editor.

**Parent Topic:**[Configuring Now Assist for Code](../concept/configuring-now-assist-code.md)

## Set default AI model providers for your instance

Select a large language model \(LLM\) as the AI service provider for Now Assist for Code skills in your instance.

### Before you begin

Role required: admin

### About this task

Set the default AI model providers for Now Assist skills in your instance through the Now Assist Admin console.

### Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  Go to the **Manage model providers** tab and select **Model Providers**.

    ![Manage model providers](../image/now-assist-code-manage-model-provider.png)

3.  Change the model provider by selecting **Edit LLM Provider**.

4.  Select a model provider for either all skill groups or just a specific skill group.

<table id="choicetable_nkr_m3k_zfc"><thead><tr><th align="left" id="d711103e207">

Choice

</th><th align="left" id="d711103e210">

Description

</th></tr></thead><tbody><tr><td id="d711103e216">

**Select a model provider for all the skill groups and skills in the instance.**

</td><td>

1.  In the Edit model provider Window, set the edit scope to **Instance**.
2.  From the Default model provider list, select a model provider.
3.  Select **Save and activate**.
 ![Select a model provider for all the skill groups and skills in the instance.](../image/now-assist-code-llm-instance.png)

</td></tr><tr><td id="d711103e261">

**Select a model provider for a specific skill group.**

</td><td>

1.  In the Edit model provider Window, set the edit scope to **Customize**.
2.  To change the model provider for a skill group, do the following:
    1.  From the Skill group name list, select the skill group.
    2.  From the Default LLM provider list, select a model provider.
    3.  Select **Save and activate**

![Select model provider for a skill group.](../image/now-assist-code-llm-customize-skill-group.png)

</td></tr><tr><td id="d711103e314">

**Select a model provider for a specific skill.**

</td><td>

1.  In the Edit model provider Window, set the edit scope to **Customize**.
2.  To change the model provider for specific skills, do the following:

    1.  From the Select skills list, select the skill.
    2.  From the Default LLM provider list, select a model provider.
    3.  Select **Save and activate**.
**Note:** You can select a different model provider for each skill.

![Select model provider for specific skills.](../image/now-assist-code-llm-customize-skill.png)

</td></tr></tbody>
</table>
### Result

The skills and the skill groups are updated with the selected model providers.

## Select an AI model provider for Now Assist for Code skills in script editor

Select an AI model provider for specific skills within the script editor.

### Before you begin

Role required: authenticated user

### About this task

AI stewards can enable or disable AI model providers in the AI Control Tower. Administrators set the default AI model providers for Now Assist skills in your instance through the Now Assist Admin console. As a user, you can override the instance default AI model provider and select a different model provider for Now Assist for Code skills in the script editor. You can only choose from the models that are enabled in the AI Control Tower.

### Procedure

1.  Navigate to any script editor enabled with Now Assist for Code.

    For example, to open a script include form, navigate to **All** &gt; **System Definition** &gt; **Script Includes** and select a script include.

2.  Select **Settings**.

    A list of all available AI model providers is shown. The options displayed depend on the model providers enabled by the AI stewards in the AI Control Tower. The **Use instance defaults** option is selected by default.

3.  Select a model provider.

    ![From the list of AI Providers, select a model provider.](../image/now-assist-code-settings.png)


### Result

All requests to Now Assist for Code, including Code auto-complete, Code explain, Code generation, and Code edit, use the model provider that you selected.

**Note:**

You can switch between models at any time and as many times as you like.

