---
title: Clone and edit a ServiceNow skill
description: Clone an eligible skill provided in ServiceNow Otto applications in AI Skill Kit so that you can edit its prompt or change its AI service provider. Editing the prompt lets you control the format and content of the large language model \(LLM\) response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/clone-and-edit-servicenow-skill.html
release: brazil
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-11-05"
reading_time_minutes: 2
breadcrumb: [Create a skill, Using AI Skill Kit, AI Skill Kit, Generative AI skills, Enable AI Experiences]
---

# Clone and edit a ServiceNow skill

Clone an eligible skill provided in ServiceNow Otto applications in AI Skill Kit so that you can edit its prompt or change its AI service provider. Editing the prompt lets you control the format and content of the large language model \(LLM\) response.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Select the **AI skills** tab.

3.  Select the skill that you want to clone.

4.  In the **Clone and modify** banner, select **Clone skill**.

5.  In the **Clone skill** dialog, enter the details for the new skill.

    1.  In the **Skill name** field, enter a name for the skill.

    2.  In the **Description** field, describe the skill.

    3.  Select a **Default provider** and a **Default provider API**.

        For more information about the available providers, see [Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/create-new-skill.md).

    4.  To clone the skill without its prompts, select **Skill configuration only**.

        A clone made with this option appears on the **AI skills** tab. A clone made without it includes the prompts and appears on the **Custom skills** tab.

6.  Select **Clone**.

    The cloned skill opens on the **Edit prompt** tab.

7.  To add an input, in the **Skill contents** pane, select the add icon \(**+**\) next to **inputs**.

    To remove an input, select the remove icon \(**X**\) next to it.

    1.  In the **Data type** field, select the data type of the input.

    2.  In the **Name** field, enter a name for the input.

    3.  In the **Description** field, describe the input.

    4.  To require the input for the skill to run, select **Make input mandatory**.

    5.  To trim the input when it's over the token limit and keep the prompt intact, select **Allow truncation**.

    6.  Select **Add skill input**.

8.  To edit a prompt, in the **Skill contents** pane, under **Prompts**, select the prompt.

    Prompts are grouped by provider. Edit the text in the **Prompt** field, and then select **Save**.

9.  To set when the prompt runs, select the prompt usage conditions icon \(diamond\) on the right side of the page, and add the conditions.

    Prompt usage conditions determine when a prompt runs.

10. To test the prompt, in the **Test prompt** section, select **Run test**.

    The results appear in the **Test prompt** section.

11. Select the **Deployment and skill settings** tab.

12. To change the default provider, in the provider list, turn on **Set as default** for the provider that you want the skill to use.

    Only one provider can be the default. Turning on the toggle for one provider turns it off for the others.


## What to do next

To add another prompt to the skill, see [Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md).

After you clone and edit the skill and prompt, you can evaluate your prompt. To learn more about evaluating a prompt, see [Evaluate a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/evaluate-prompt.md).

**Parent Topic:**[Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/create-new-skill.md)

