---
title: Example use case for Now Assist Skill Kit
description: As an AI developer, you can create custom skills with Now Assist Skill Kit. For this example, create a custom skill for child incident summarization.
locale: en-US
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Exploring Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Example use case for Now Assist Skill Kit

As an AI developer, you can create custom skills with Now Assist Skill Kit. For this example, create a custom skill for child incident summarization.

As an AI developer, you must create a skill for child incident summarization. Creating this skill can help you organize and understand multiple incidents that are related to the same parent.

## Create and configure the skill

To create the skill:

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.
2.  Select **Create new skill**.
3.  On the form, fill in the fields. The following information is used to fill in the form for this example:

    -   Skill name: `Child incident summarization`
    -   Description: `Summarization of child incidents`
    -   Default provider: `Now LLM Generic`
    -   Provider API: `Now LLM Generic`
    ![Create new skill modal for Now Assist Skill Kit.](../image/nask-new-skill.png)

4.  Select **Create skill**.

After you create the skill, you must configure the skill settings.

1.  Select **Configurations**.
2.  Select the model that you want to use. For this example, you can select `llm_generic`.
3.  Select a temperature between 0-1 to determine the randomness and creativity of the output, such as `0.2`.

## Develop the prompt

After you create the skill and configure the settings, you must develop the prompt. To follow this example, you can use the following prompt:

`You are a customer service representative. Summarize the child incidents of the below given parent incident. The summary should contain key issues and impact across the child incidents, highlighting any patterns, recurring problems, or significant outliers. When summarizing, please consider the following: Parent incident short description: {{incident.short_description}} Parent incident description: {{incident.description}} Here are the child incident details: {{ChildIncidents.output}}`

Select the **Inputs** for the skill. For this example, the record is selected as the input.

![Skill input modal for Now Assist Skill Kit.](../image/nask-add-skill-input.png)

Select insert inputs for the prompt.

![Prompt page for Now Assist Skill Kit with the Insert iIputs button outlined in red.](../image/nask-insert-inputs.png)

For this example, the following is used:

`Parent incident short description: {{incident.short_description}} Parent incident description: {{incident.description}} Here are the child incident details: {{ChildIncidents.output}}`

Select the tools for the skill. For this example, select Flow Action and the IncidentDetailsFetcher flow resource.

![Add tool modal in Now Assist Skill Kit.](../image/nask-add-tool-example.png)

## Configure the skill deployment options

The next step is to configure the skill deployment options. These options enable you to choose where to find the skill in Now Assist Admin.

1.  Select the **Skill settings** tab.
2.  Select **Deployment Settings**.
3.  Enable the admin to enable the skill from the Core UI by selecting the **UI Action** check box.
4.  Select **Save**.

## Test and publish the skill

It is important to test your skill prompt to ensure that the correct type of data is being pulled in.

1.  Select **Run tests**.
2.  Choose a record or incident.
3.  Select **Run test**.

Look at the response.

To see the data that was brought into the prompt from your skill inputs and tools, you can look at the grounded prompt tab.

If everything looks good, select **Finalize prompt**. After you finalize the prompt and you are ready to implement it, select **Publish**.

## Activate the skill

After you test, finalize, and publish your skill, an admin must activate it in Now Assist Admin. To learn more about activating skills, see [Activate a skill](../task/activate-skill.md).

