---
title: Configure a skill prompt
description: Configure your skill prompt to set the model that is used and the randomness and creativity of the response.
locale: en-US
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Configure a skill prompt

Configure your skill prompt to set the model that is used and the randomness and creativity of the response.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you want to configure.

3.  In the **Skill contents** sidebar, select the prompt that you want to configure.

4.  Select **Manage prompt**, then select **Prompt settings**.

5.  Fill in the fields.

<table id="table_vxy_rqh_lcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

The model is the large language model \(LLM\) that you want to use for the prompt.

</td></tr><tr><td>

Temperature

</td><td>

The randomness and creativity of the output. A higher value increases the randomness. The value must be between 0 and 1.

</td></tr><tr><td>

Thinking mode

</td><td>

Controls how much reasoning effort the LLM applies when generating a response. Higher levels improve output quality but increase latency. Thinking mode is available when using *llm\_generic\_small\_v2* or *llm\_generic\_large\_v2*.

</td></tr><tr><td>

Maximum response tokens

</td><td>

The maximum number of tokens the model can return. Token limits are set by your admin for controlled usage.

</td></tr><tr><td>

Maximum request tokens

</td><td>

The maximum number of tokens allowed in a request. Token limits are set by your admin for controlled usage.

</td></tr><tr><td>

Structured output

</td><td>

Returns prompt responses in a consistent JSON format. **Note:** Only Google Gemini and Azure OpenAI support structured output. This option is not available when using Now LLM Service.

</td></tr></tbody>
</table>6.  To configure when this prompt runs, select **Manage prompt**, then select **Usage conditions**.

    Usage conditions are filters built from your skill inputs. When a skill has multiple prompts, usage conditions determine which prompt runs for a given execution. The prompt without usage conditions is the default and runs when no other prompt's conditions are met.

    **Important:** Usage conditions require at least one skill input to be defined. If your skill has no inputs, the Usage conditions panel will have no available keys to filter on.


## What to do next

After you configure your prompt settings, you can test your skill. To learn more about testing skills, see [Test a prompt](test-prompt-template.md).

To learn more about configuring models and tokens, see [Now Assist Skill Kit FAQs on the ServiceNow Community.](https://www.servicenow.com/community/now-assist-articles/now-assist-skill-kit-nask-faq/ta-p/3007953)

**Parent Topic:**[Configuring Now Assist Skill Kit](../concept/configuring-now-assist-skill-kit.md)

**Related topics**  


[Configure skill deployment settings](configure-skill-settings.md)

[Configure security controls for a skill](nask-access-control.md)

