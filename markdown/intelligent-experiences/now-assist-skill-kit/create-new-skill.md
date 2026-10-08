---
title: Create a skill
description: Create a custom skill for Otto. Custom skills extend the generative AI capabilities of Otto to fit your own use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/create-new-skill.html
release: brazil
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Using AI Skill Kit, AI Skill Kit, Generative AI skills, Enable AI Experiences]
---

# Create a skill

Create a custom skill for Otto. Custom skills extend the generative AI capabilities of Otto to fit your own use cases.

## Before you begin

Role required: sn\_skill\_builder.admin

**Note:** When you update AI Skill Kit also update Generative AI Controller so that your skills continue to work as expected.

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Select **Create new skill**.

3.  On the form, fill in the fields.

    \[Omitted image "nask-new-skill.png"\] Alt text: New skill modal in AI Skill Kit.

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

You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

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

</td></tr><tr><td>

User access

</td><td>

-   Any authenticated user

Any logged-in user can access and run the skill.

-   Select roles

Select the roles that a user must have to execute the skill.

**Note:** If you select multiple roles, a user needs only one of the roles to run the skill.

</td></tr><tr><td>

Role restrictions

</td><td>

Roles that the skill runs as. Access control lists \(ACLs\) determine which user roles can trigger the skill, while role restrictions determine the roles that the skill operates with when it runs.

</td></tr></tbody>
</table>4.  Select how you want to create the prompt for the skill.

    -   Write from scratch
    -   Choose one from library
        1.  Find the prompt that you want to use.
        2.  Select **View**.
        3.  Select **Use prompt**.
    -   Use an AI-generated prompt
    \[Omitted image "nask-guided-setup.png"\] Alt text: Guided setup for AI Skill Kit

5.  Select **Next**.

6.  Add skill inputs and outputs.

7.  Select **Go to summary**.

8.  Select **Finish**.


## What to do next

After you create the skill, you must configure it. To learn more about configuring a skill, see [Configure a skill prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/configure-skill-prompt.md).

If you don't need to set any configurations for your skill, you can create your skill prompt and tools. To learn more, see [Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md) and [Add a tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/add-a-tool.md).

-   **[Clone and edit a ServiceNow skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/clone-and-edit-servicenow-skill.md)**  
Clone an eligible skill provided in ServiceNow Otto applications in AI Skill Kit so that you can edit its prompt or change its AI service provider. Editing the prompt lets you control the format and content of the large language model \(LLM\) response.

**Parent Topic:**[Using AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/using-now-assist-skill-kit.md)

**Related topics**  


[Create a prompt]()

[Use prompt assistance]()

[Test a prompt]()

[Evaluate a prompt]()

[Finalize and publish a skill]()

[Activate a skill]()

[Call a custom skill from a script]()

