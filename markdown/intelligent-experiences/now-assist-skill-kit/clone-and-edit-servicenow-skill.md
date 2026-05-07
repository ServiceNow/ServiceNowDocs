---
title: Clone a skill
description: Clone an existing skill to use it as a starting point for a new one. You can clone both base system ServiceNow skills and custom skills you have created.
locale: en-US
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 2
keywords: [clone, clone skill, Now Assist Skill Kit]
breadcrumb: [Create a skill, Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Clone a skill

Clone an existing skill to use it as a starting point for a new one. You can clone both base system ServiceNow skills and custom skills you have created.

## Before you begin

Role required: sn\_skill\_builder.admin

## About this task

Cloning a skill creates a copy in Draft state with the original prompt content, inputs, and outputs carried over. You can then edit the prompt, change the provider, or adjust other settings without affecting the original skill.

**Important:** Deployment settings for clones of base system ServiceNow skills cannot be edited after cloning. If you need custom deployment settings, create a new skill instead. Deployment settings for clones of custom skills can be edited normally.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you want to clone.

3.  Open the **Clone skill** dialog.

    There are two ways to access this dialog depending on the skill type:

    -   For base system ServiceNow skills, select **Clone Skill** in the banner at the top of the skill page, or select the three-dot menu next to **Publish skill** and then select **Clone**.
    -   For custom skills, select the three-dot menu next to **Publish skill** and then select **Clone**.
4.  Fill in the fields and select **Clone**.

<table id="table_chg_qth_lcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \(required\)

</td><td>

A name for the cloned skill. Defaults to "Clone of \[original skill name\]".

</td></tr><tr><td>

Description

</td><td>

A description of the cloned skill.

</td></tr><tr><td>

Default provider \(required\)

</td><td>

The LLM provider for the cloned skill. Available providers include Now LLM Service and external LLM options including prebuilt spokes for Microsoft Azure OpenAI Generative AI Spoke, OpenAI Generative AI Spoke, Aleph Alpha, WatsonX, and Google Gemini, or a custom LLM. For more information on setting up a custom LLM, see [Configure a generic large language model \(LLM\) connector](../../generative-ai-controller/task/configure-a-generic-llm-connector.md). **Note:** Spokes consume assists, not Integration Hub transactions.

</td></tr><tr><td>

Provider API \(required\)

</td><td>

The API for the selected provider.

</td></tr><tr><td>

Skill configuration only

</td><td>

Available for base system ServiceNow skills only.

</td></tr></tbody>
</table>
## What to do next

Create your skill prompt. To learn more about creating a prompt, see [Create a prompt](create-prompt-template.md).

After you clone and edit the skill and prompt, you can evaluate your prompt.To learn more about evaluating a prompt, see [Evaluate a prompt](evaluate-prompt.md).

**Parent Topic:**[Create a skill](create-new-skill.md)

