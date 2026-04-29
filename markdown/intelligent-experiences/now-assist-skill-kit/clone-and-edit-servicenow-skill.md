---
title: Clone and edit a ServiceNow skill
description: Eligible skills provided in ServiceNow Now Assist applications can be cloned in Now Assist Skill Kit so that you can edit the prompt or change the AI service provider. Editing the prompt enables you to arrange the formatting and content of the LLM response.
locale: en-US
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a skill, Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Clone and edit a ServiceNow skill

Eligible skills provided in ServiceNow Now Assist applications can be cloned in Now Assist Skill Kit so that you can edit the prompt or change the AI service provider. Editing the prompt enables you to arrange the formatting and content of the LLM response.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select **ServiceNow skills**

3.  Select the ServiceNow skill that you want to clone.

4.  Select **Clone Skill**.

5.  Fill in the fields on the form.

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
</table>6.  Select **Clone**.

    **Note:** When you clone a skill, you can't change the skill outputs, tools, or deployment settings.

7.  Select the edit icon to add skill inputs.

    |Section|Description|
    |-------|-----------|
    |Base input table fields|Each skill relies on a base input table and input fields with descriptions to provide context for the LLM to generate a response.|
    |Rule conditions|Rule conditions determine when the input template is used. By default, record state determines which input template the LLM uses.|
    |Additional input data sources|You can add input data sources like related tables, activity streams and relationships to provide more context to the LLM. You can also add rule conditions to these additional data sources.|

8.  Select **Clone prompt** to edit the prompt.

    You will see all of the prompts that use the same supporting skill for each provider.

9.  Add **Prompt usage conditions**.

    These are conditions that determine when a prompt will be executed.

10. To test the prompt, select **Run test** and add test values.

11. Select the **Skill settings** tab.

12. Select **General information** to change the default provider by selecting the toggle.


## What to do next

Create your skill prompt. To learn more about creating a prompt, see [Create a prompt](create-prompt-template.md).

After you clone and edit the skill and prompt, you can evaluate your prompt.To learn more about evaluating a prompt, see [Evaluate a prompt](evaluate-prompt.md).

**Parent Topic:**[Create a skill](create-new-skill.md)

