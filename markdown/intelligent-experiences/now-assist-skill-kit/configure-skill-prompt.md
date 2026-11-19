---
title: Configure a skill prompt
description: Configure a skill prompt to set its large language model \(LLM\), the randomness of its responses, and its token limits.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-skill-kit/configure-skill-prompt.html
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring AI Skill Kit, AI Skill Kit, Enable AI experiences]
---

# Configure a skill prompt

Configure a skill prompt to set its large language model \(LLM\), the randomness of its responses, and its token limits.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Select the skill that you want to configure.

3.  Select **Configurations**.

    \[Omitted image "nask-configurations.png"\] Alt text: Configuration panel for the AI Skill Kit prompt.

4.  On the form, fill in the fields.

<table id="table_vxy_rqh_lcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

Large language model \(LLM\) to use for the prompt.

</td></tr><tr><td>

Temperature

</td><td>

Randomness and creativity of the output. A higher value increases randomness. The value must be from 0 through 1.

</td></tr><tr><td>

Maximum response tokens

</td><td>

Maximum number of tokens that the model can return. If you’re using Now LLM Service, the maximum is 1,000.

</td></tr><tr><td>

Maximum request tokens

</td><td>

Maximum number of tokens allowed in a request.

</td></tr><tr><td>

Structured output

</td><td>

Option to return prompt responses in a consistent JSON format. **Note:** Only Google Gemini and Azure OpenAI support structured output. This option is not available when using Now LLM Service.

</td></tr></tbody>
</table>5.  Add **Usage conditions** to determine when to use the prompt.


## What to do next

After you configure your skill prompt, you can test it. To learn more about testing skills, see [Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md).

To learn more about configuring the skill, including models and tokens, see [AI Skill Kit FAQs on the ServiceNow Community.](https://www.servicenow.com/community/now-assist-articles/now-assist-skill-kit-nask-faq/ta-p/3007953)

**Parent Topic:**[Configuring AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/configuring-now-assist-skill-kit.md)

**Related topics**  


[Configure deployment and skill settings]()

[Configure security controls for a skill]()

