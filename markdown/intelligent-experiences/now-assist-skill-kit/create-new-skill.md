---
title: Create a skill
description: Create a custom skill for Now Assist. Creating a custom skill enables you to have greater flexibility with Now Assist's generative AI capabilities.
locale: en-US
release: xanadu
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Create a skill

Create a custom skill for Now Assist. Creating a custom skill enables you to have greater flexibility with Now Assist's generative AI capabilities.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select **Create new skill**.

3.  On the form, fill in the fields.

    ![New skill modal in Now Assist Skill Kit.](../image/nask-new-skill.png)

<table id="table_chg_qth_lcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skill name

</td><td>

A name for the skill.

</td></tr><tr><td>

Description

</td><td>

A description of the skill.

</td></tr><tr><td>

Default provider

</td><td>

Available providers:-   Now LLM Service
-   External LLM
    -   Spokes
    -   Custom LLM

For more information on setting up a custom large language model \(LLM\), see [Configure a generic large language model \(LLM\) connector](../../generative-ai-controller/task/configure-a-generic-llm-connector.md)

Available prebuilt spokes that enable you to connect with an external LLM:

-   Microsoft Azure OpenAI Generative AI Spoke
-   OpenAI Generative AI Spoke
-   Aleph Alpha
-   WatsonX
-   Google Gemini \(MakerSuite and Vertex AI\)
**Note:** The spokes don't consume Integration Hub transactions. The spokes consume assists.

</td></tr><tr><td>

Provider API

</td><td>

The provider of the API for your chosen LLM.

</td></tr></tbody>
</table>4.  Select **Create skill**.


## What to do next

After you create the skill, you must configure it. To learn more about configuring a skill, see [Configure a skill prompt](configure-skill-prompt.md).

If you don't need to set any configurations for your skill, you can create your skill prompt. To learn more about creating a prompt, see [Create a prompt](create-prompt-template.md).

**Parent Topic:**[Using Now Assist Skill Kit](../concept/using-now-assist-skill-kit.md)

**Related topics**  


[Create a prompt](create-prompt-template.md)

[Use prompt assistance](use-prompt-assistance.md)

[Test a prompt](test-prompt-template.md)

[Evaluate a prompt](evaluate-prompt.md)

[Finalize and publish a skill](publish-skill.md)

[Activate a skill](activate-skill.md)

[Call a custom skill from a script](call-custom-skill-from-script.md)

