---
title: Create a skill
description: Create a custom skill for Otto. Custom skills extend the generative AI capabilities of Otto to fit your own use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-skill-kit/create-new-skill.html
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 6
breadcrumb: [Using AI Skill Kit, AI Skill Kit, Generative AI skills, Enable AI Experiences]
---

# Create a skill

Create a custom skill for Otto. Custom skills extend the generative AI capabilities of Otto to fit your own use cases.

## Before you begin

Role required: sn\_skill\_builder.admin

**Note:** When you update AI Skill Kit also update Generative AI Controller so that your skills continue to work as expected.

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Select **Create skill**.

    The **New skill** page opens on the **Add general info** tab.

3.  On the **Add general info** tab, describe the skill and choose its provider.

    1.  In the **Skill name** field, enter a unique name for the skill.

        Use only letters, numbers, and spaces. Special characters aren't allowed.

    2.  In the **Description** field, describe the purpose of the skill.

    3.  Select a **Default provider**.

        The list includes all providers. Providers that aren't available on your instance appear in the list but can't be selected.

        Available providers:

        -   Now LLM Service
        -   External LLM

            You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in AI Control Tower to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

            -   Spokes
            -   Custom LLM

                For more information on setting up a custom large language model \(LLM\), see [Configure a generic large language model \(LLM\) connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/generative-ai-controller/configure-a-generic-llm-connector.md)

        Available prebuilt spokes that enable you to connect with an external LLM:

        -   Microsoft Azure OpenAI Generative AI Spoke
        -   OpenAI Generative AI Spoke
        -   Aleph Alpha
        -   IBM watsonx
        -   Google Gemini \(MakerSuite and Vertex AI\)
        **Note:** The spokes don't consume Integration Hub transactions. The spokes consume assists.

    4.  Select a **Default provider API**.

        After you select a provider and an API, the models available for them appear in the **Models** area. This list is for reference only. You can't select a model from it.

        If the API that you select has no active models, the message `No active models found` appears and you can't continue.

4.  In the **Define user access with an Access Control List \(ACL\)** section, select who can access and run the skill.

    -   **Any authenticated user**: Any logged-in user can access and run the skill.
    -   **Select roles**: In the **Roles** field, select the roles that a user must have to run the skill. If you select multiple roles, a user needs only one of the roles to run the skill.
    When you save the skill, an ACL is created. The section then shows the ACL as an entry that you can edit.

5.  In the **Apply role restrictions to skill** section, select the roles that the skill can inherit from the user who runs it.

    Role restrictions are required. They limit the roles that the skill operates with when it runs, so that it doesn't access more resources than necessary. The ACL determines who can run the skill. Role restrictions determine what the skill can access while it runs.

    If you selected roles for user access, you can select **Copy roles from user access** to use the same roles.

6.  Select **Continue**.

7.  On the **Start prompt creation** tab, select how you want to create the prompt for the skill.

    -   **Write from scratch**: Start with an empty prompt.
    -   **Choose one from library**: On the card for the prompt that you want, select **View**, and then select **Use prompt**.
    -   **Use an AI-generated prompt**: Generate a prompt from the details that you entered on the **Add general info** tab.
8.  Select **Continue**.

9.  On the **Add skill inputs** tab, add the inputs that the skill uses.

    To add more inputs, select **Add** again. To remove an input, select the delete icon on its card. To hide or show the details of an input, select the expand or collapse icon on its card.

    1.  Select **Add**.

        A card for the new input appears.

    2.  In the **Data type** field, select the data type of the input.

        Available data types:

        -   **Record**
        -   **String**
        -   **Numeric**
        -   **Boolean**
        -   **Simple array**
        -   **JSON object**
        -   **JSON array**
    3.  In the **Name** field, enter a name for the input.

        The name is available in the pill picker.

    4.  In the **Description** field, describe the input.

    5.  To require the input for the skill to run, select **Make input mandatory**.

    6.  To trim the input when it's over the token limit and keep the prompt intact, select **Allow truncation**.

        This option is available only for **Record**, **String**, **Numeric**, and **Boolean** inputs.

    7.  In the ct **Finish setup**ld, enter the default values to use when the skill runs.

        You can override these values when the skill runs.

10. Select **Continue to summary**.

11. On the **Review summary** tab, review the skill details and select learn more, se.


## What to do next

After you create the skill, you must configure it. To learn more about configuring a skill, see [Configure a skill prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/configure-skill-prompt.md).

If you don't need to set any configurations for your skill, you can create your skill prompt and tools. To learn more, see [Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md) and [Add a tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/add-a-tool.md).

-   **[Clone and edit a ServiceNow skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/clone-and-edit-servicenow-skill.md)**  
Clone an eligible skill provided in ServiceNow Otto applications in AI Skill Kit so that you can edit its prompt or change its AI service provider. Editing the prompt lets you control the format and content of the large language model \(LLM\) response.

**Parent Topic:**[Using AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/using-now-assist-skill-kit.md)

**Related topics**  


[Create a prompt]()

[Use prompt assistance]()

[Test a prompt]()

[Evaluate a prompt]()

[Finalize and publish a skill]()

[Activate a skill]()

[Call a custom skill from a script]()

