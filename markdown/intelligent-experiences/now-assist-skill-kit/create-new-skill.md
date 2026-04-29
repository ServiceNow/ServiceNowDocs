---
title: Create a skill
description: Create a custom skill for Now Assist. Creating a custom skill enables you to have greater flexibility with Now Assist's generative AI capabilities.
locale: en-US
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Create a skill

Create a custom skill for Now Assist. Creating a custom skill enables you to have greater flexibility with Now Assist's generative AI capabilities.

## Before you begin

Role required: sn\_skill\_builder.admin

**Note:** When you update Now Assist Skill Kit you should also update Generative AI Controller to ensure that your skills continue to perform correctly.

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

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](../../ai-governance-workspace/concept/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](../../now-assist-admin/task/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform](../../general/concept/exploring-large-language-models.md).

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

</td></tr><tr><td>

User access

</td><td>

-   Any authenticated user

As long as a user is logged in, they can access and execute the skill.

-   Select roles

Select the roles that a user must have to execute the skill.

**Note:** If you select multiple roles, a user must only have one of the roles to execute the skill.

</td></tr><tr><td>

Role restrictions

</td><td>

Role restrictions define the specific roles under which a skill in ServiceNow executes. While ACLs determine which user roles are permitted to trigger the skill, role restrictions determine the roles the skill will operate with during execution.

</td></tr></tbody>
</table>4.  Select how you want to create the prompt for the skill.

    -   Write from scratch
    -   Choose one from library
        1.  Find the prompt that you want to use.
        2.  Select View.
        3.  Select Use prompt.
    -   Use an AI-generated prompt
    ![Guided set up for Now Assist Skill Kit](../image/nask-guided-setup.png)

5.  Select **Next**.

6.  Add skill inputs and outputs.

7.  Select **Go to summary**.

8.  Select **Finish**.


## What to do next

After you create the skill, you must configure it. To learn more about configuring a skill, see [Configure a skill prompt](configure-skill-prompt.md).

If you don't need to set any configurations for your skill, you can create your skill prompt and tools. To learn more, see [Create a prompt](create-prompt-template.md) and [Add a tool](../concept/add-a-tool.md).

-   **[Clone and edit a ServiceNow skill](clone-and-edit-servicenow-skill.md)**  
Eligible skills provided in ServiceNow Now Assist applications can be cloned in Now Assist Skill Kit so that you can edit the prompt or change the AI service provider. Editing the prompt enables you to arrange the formatting and content of the LLM response.

**Parent Topic:**[Using Now Assist Skill Kit](../concept/using-now-assist-skill-kit.md)

**Related topics**  


[Create a prompt](create-prompt-template.md)

[Use prompt assistance](use-prompt-assistance.md)

[Test a prompt](test-prompt-template.md)

[Evaluate a prompt](evaluate-prompt.md)

[Finalize and publish a skill](publish-skill.md)

[Activate a skill](activate-skill.md)

[Call a custom skill from a script](call-custom-skill-from-script.md)

