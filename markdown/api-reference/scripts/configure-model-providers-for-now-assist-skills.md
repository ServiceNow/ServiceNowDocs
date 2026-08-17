---
title: Configure AI model providers for ServiceNow Otto for Code skills
description: Select a large language model \(LLM\) as the AI service provider for ServiceNow Otto for Code skills.Select a large language model \(LLM\) as the AI service provider for ServiceNow Otto for Code skills.Select an AI model provider for specific skills within the script editor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/configure-model-providers-for-now-assist-skills.html
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 3
breadcrumb: [Configure, ServiceNow Otto for Code, Scripting, API implementation, API implementation and reference]
---

# Configure AI model providers for ServiceNow Otto for Code skills

Select a large language model \(LLM\) as the AI service provider for ServiceNow Otto for Code skills.

You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md).

AI stewards can enable or disable AI model providers in the AI Control Tower. Administrators set the default AI model providers for generative AI skills in your instance through the AI Admin Hub console. As a user, you can override the instance default AI model provider and select a different model provider for ServiceNow Otto for Code skills in the script editor.

**Parent Topic:**[Configuring ServiceNow Otto for Code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/configuring-now-assist-code.md)

## Set default AI model providers for your instance

Select a large language model \(LLM\) as the AI service provider for ServiceNow Otto for Code skills.

### Before you begin

Role required: admin

### About this task

Set the default AI model providers for generative AI skills in your instance through the AI Admin Hub console.

### Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Settings**.

2.  Go to the **Manage AI models** &gt; **Manage model providers** tab and select **Model providers**.

3.  Select **Edit model provider** to change the model provider.

4.  Select a model provider for either all skill groups or just a specific skill group.

<table id="choicetable_nkr_m3k_zfc"><thead><tr><th align="left" id="d728637e190">

Choice

</th><th align="left" id="d728637e193">

Description

</th></tr></thead><tbody><tr><td id="d728637e199">

**Select a model provider for all the skill groups and skills in the instance.**

</td><td>

1.  In the Edit model provider Window, set the edit scope to **Instance**.
2.  From the Default model provider list, select a model provider.
3.  Select **Save and activate**.
 \[Omitted image "soc-instance-edit-model-provider.png"\] Alt text: Select a model provider for all the skill groups and skills in the instance.

</td></tr><tr><td id="d728637e246">

**Select a model provider for a specific skill group.**

</td><td>

1.  In the Edit model provider Window, set the edit scope to **Customize**.
2.  To change the model provider for a skill group, do the following:
    1.  From the Skill group name list, select the skill group.
    2.  From the default model provider list, select a model provider.
    3.  Select **Save**.

\[Omitted image "soc-customize-group-edit-model-provider.png"\] Alt text: Select a model provider for a specific skill group.

</td></tr><tr><td id="d728637e289">

**Select a model provider for a specific skill.**

</td><td>

1.  In the Edit model provider Window, set the edit scope to **Customize**.
2.  To change the model provider for specific skills, do the following:

    1.  From the Select skills list, select the skill.
    2.  From the default model provider list, select a model provider.
    3.  Select **Save**.
\[Omitted image "soc-customize-skills-edit-model-provider.png"\] Alt text: Select a model provider for a specific skill.

</td></tr></tbody>
</table>
### Result

The skills and the skill groups are updated with the selected model providers.

## Select an AI model provider for ServiceNow Otto for Code skills in script editor

Select an AI model provider for specific skills within the script editor.

### Before you begin

Role required: authenticated user

### About this task

AI stewards can enable or disable AI model providers in the AI Control Tower. Administrators set the default AI model providers for generative AI skills in your instance through the AI Admin Hub console. As a user, you can override the instance default AI model provider and select a different model provider for ServiceNow Otto for Code skills in the script editor. You can only choose from the models that are enabled in the AI Control Tower.

### Procedure

1.  Navigate to any script editor enabled with ServiceNow Otto for Code.

    For example, to open a script include form, navigate to **All** &gt; **System Definition** &gt; **Script Includes** and select a script.

2.  Select **Settings**.

    A list of all available AI model providers is shown. The options displayed depend on the model providers enabled by the AI stewards in the AI Control Tower. The **Use instance defaults** option is selected by default.

3.  Select a model provider.

    \[Omitted image "soc-settings.png"\] Alt text: From the list of AI Providers, select a model provider.


### Result

All requests to ServiceNow Otto for Code, including Code auto-complete, Code explain, Code generation, and Code edit, use the model provider that you selected.

**Note:**

You can switch between models at any time and as many times as you like.

