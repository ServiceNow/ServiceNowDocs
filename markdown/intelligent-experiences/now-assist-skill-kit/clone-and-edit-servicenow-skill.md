---
title: Clone and edit a ServiceNow skill
description: Clone an eligible skill provided in ServiceNow Otto applications in AI Skill Kit so that you can edit its prompt or change its AI service provider. Editing the prompt lets you control the format and content of the large language model \(LLM\) response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/clone-and-edit-servicenow-skill.html
release: brazil
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 2
breadcrumb: [Create a skill, Using AI Skill Kit, AI Skill Kit, Generative AI skills, Enable AI Experiences]
---

# Clone and edit a ServiceNow skill

Clone an eligible skill provided in ServiceNow Otto applications in AI Skill Kit so that you can edit its prompt or change its AI service provider. Editing the prompt lets you control the format and content of the large language model \(LLM\) response.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Select **ServiceNow skills**

3.  Select the ServiceNow skill that you want to clone.

4.  Select **Clone Skill**.

5.  On the form, fill in the fields.

<table id="table_chg_qth_lcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skill name

</td><td>

Name of the skill.

</td></tr><tr><td>

Description

</td><td>

Description of the skill.

</td></tr><tr><td>

Default provider

</td><td>

Available providers:-   Now LLM Service
-   External LLM
    -   Spokes
    -   Custom LLM

For more information on setting up a custom large language model \(LLM\), see [Configure a generic large language model \(LLM\) connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/generative-ai-controller/configure-a-generic-llm-connector.md)

Available prebuilt spokes that enable you to connect with an external LLM:

-   Microsoft Azure OpenAI Generative AI Spoke
-   OpenAI Generative AI Spoke
-   Aleph Alpha
-   IBM watsonx
-   Google Gemini \(MakerSuite and Vertex AI\)
**Note:** The spokes don't consume Integration Hub transactions. The spokes consume assists.

</td></tr><tr><td>

Provider API

</td><td>

Provider of the API for the selected LLM.

</td></tr></tbody>
</table>6.  Select **Clone**.

    **Note:** When you clone a skill, you can't change the skill outputs, tools, or deployment settings.

7.  Select the edit icon to add skill inputs.

    |Section|Description|
    |-------|-----------|
    |Base input table fields|Each skill relies on a base input table and input fields with descriptions to provide context for the LLM to generate a response.|
    |Rule conditions|Rule conditions determine when the input template is used. By default, record state determines which input template the LLM uses.|
    |Additional input data sources|You can add input data sources such as related tables, activity streams, and relationships to provide more context to the LLM. You can also add rule conditions to these additional data sources.|

8.  Select **Clone prompt** to edit the prompt.

    The list shows all prompts that use the same supporting skill for each provider.

9.  Add **Prompt usage conditions**.

    Prompt usage conditions determine when a prompt runs.

10. To test the prompt, select **Run test** and add test values.

11. Select the **Skill settings** tab.

12. In the **General information** section, select the toggle to change the default provider.


## What to do next

Create your skill prompt. To learn more about creating a prompt, see [Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md).

After you clone and edit the skill and prompt, you can evaluate your prompt. To learn more about evaluating a prompt, see [Evaluate a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/evaluate-prompt.md).

**Parent Topic:**[Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/create-new-skill.md)

