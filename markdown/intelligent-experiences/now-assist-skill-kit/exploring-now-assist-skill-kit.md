---
title: Exploring Now Assist Skill Kit
description: Use the Now Assist Skill Kit plugin for Now Assist to create and activate custom prompts and skills for Now Assist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/exploring-now-assist-skill-kit.html
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: concept
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [Now Assist Skill Kit, Enable AI experiences]
---

# Exploring Now Assist Skill Kit

Use the Now Assist Skill Kit plugin for Now Assist to create and activate custom prompts and skills for Now Assist.

## Now Assist Skill Kit overview

Use Now Assist Skill Kit to create custom skills when base system Now Assist skills don't fit your needs. Custom skills enable you to have greater flexibility with Now Assist's generative AI capabilities.

## Before you build a custom skill

Because you write and refine the prompts that drive your skills, you should be comfortable with the fundamentals of prompt engineering and with how a large language model \(LLM\) behaves.

Before you begin, you should understand:

-   How an LLM produces output, including its probabilistic nature and the fact that the same prompt can produce different results on different models.
-   How to write, test, and refine a prompt based on the output it produces, rather than on how you expect the model to interpret your wording.
-   The use case you want to solve and the persona you're building the skill for.

Effective skill development depends on testing the prompt against representative data from your instance and refining it based on the results, not on a single example. For the full set of guidelines and the phases of building a skill, see [General guidelines for Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/na-skill-kit-guidelines.md). For help defining requirements and outcomes before you build, see [Scoping the skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/scoping-the-skill.md).

## Get Now Assist Skill Kit

To use Now Assist Skill Kit, you must update your Now Assist plugins in the Application Manager. For example, update your Now Assist for ITSM plugin to the latest available release.

You must also assign the **sn\_skill\_builder.admin** role to anyone who uses Now Assist Skill Kit.

## Now Assist Skill Kit users

|User|Description|
|----|-----------|
|AI developer|Creates new skills, writes and refines the prompts, and configures the skill settings. This user must have the **sn\_skill\_builder.admin** role. Building an effective skill requires prompt engineering experience and an understanding of LLM behavior.|
|Now Assist admin|Reviews and activates published skills so that they're available at the configured touch points. This user must have the **admin** role.|

## Now Assist Skill Kit workflow

The following diagram shows the user journey for Now Assist Skill Kit.

\[Omitted image "nask-user-journey.png"\] Alt text: Define your LLM provider, then develop custom skills by specifying input sources and configuring the prompt. Test with data from your instance, and then deploy your new skill.

-   **Define the provider**

    Understand the benefits and potential downsides of each large language model \(LLM\) that you're considering using.

-   **Build the prompt**

    You must have an understanding of the architecture of your Now Assist instance and be able to define where input data should come from. You should also have an understanding of LLM fundamentals to build an effective prompt.

-   **Test the prompt**

    Now Assist Skill Kit enables you to test your prompt from the editor.

-   **Deploy the skill**

    Now Assist Skill Kit enables you to deploy your skill to Now Assist panel, Now Assist Context Menu, Virtual Agent, Flow Action, or a UI Action.


## Now Assist Skill Kit benefits

Now Assist Skill Kit enables you to design your own custom generative AI functionality that is then easily deployed into the ServiceNow platform. Custom skills can augment workflows with generative AI to increase effectiveness and efficiency.

|Benefit|Feature|Users|
|-------|-------|-----|
|Create custom solutions by building a custom skill or workflow.|[Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/create-new-skill.md)|AI developer|
|Create and edit prompts for skills and configure where you want to bring in data from to augment your prompt.|[Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md)|AI developer|
|Test and iterate on your skill before activating it.|[Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md)|AI developer|

## What to explore next

To learn more about configuring and using Now Assist Skill Kit, see:

-   [Configuring Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/configuring-now-assist-skill-kit.md)
-   [Using Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/using-now-assist-skill-kit.md)

