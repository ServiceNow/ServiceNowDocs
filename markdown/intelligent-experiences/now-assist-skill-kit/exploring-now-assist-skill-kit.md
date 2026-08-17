---
title: Exploring AI Skill Kit
description: Use the AI Skill Kit plugin for Otto to create and activate custom prompts and skills for Otto.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/exploring-now-assist-skill-kit.html
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: concept
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [AI Skill Kit, Enable AI experiences]
---

# Exploring AI Skill Kit

Use the AI Skill Kit plugin for Otto to create and activate custom prompts and skills for Otto.

## AI Skill Kit overview

Use AI Skill Kit to create custom skills when base system Otto skills don't fit your needs. Custom skills enable you to have greater flexibility with Otto's generative AI capabilities.

## Before you build a custom skill

Because you write and refine the prompts that drive your skills, you should be comfortable with the fundamentals of prompt engineering and with how a large language model \(LLM\) behaves.

Before you begin, you should understand:

-   How an LLM produces output, including its probabilistic nature and the fact that the same prompt can produce different results on different models.
-   How to write, test, and refine a prompt based on the output it produces, rather than on how you expect the model to interpret your wording.
-   The use case you want to solve and the persona you're building the skill for.

Effective skill development depends on testing the prompt against representative data from your instance and refining it based on the results, not on a single example. For the full set of guidelines and the phases of building a skill, see [General guidelines for AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/na-skill-kit-guidelines.md). For help defining requirements and outcomes before you build, see [Scoping the skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/scoping-the-skill.md).

## Get AI Skill Kit

To use AI Skill Kit, you must update your Otto plugins in the [Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/exploring-application-manager.md). For example, update your ServiceNow Otto for ITSM plugin to the latest available release.

You must also assign the **sn\_skill\_builder.admin** role to anyone who uses AI Skill Kit.

## AI Skill Kit users

|User|Description|
|----|-----------|
|AI developer|Creates new skills, writes and refines the prompts, and configures the skill settings. This user must have the **sn\_skill\_builder.admin** role. Building an effective skill requires prompt engineering experience and an understanding of LLM behavior.|
|Otto admin|Reviews and activates published skills so that they're available at the configured touch points. This user must have the **admin** role.|

## AI Skill Kit workflow

The following diagram shows the user journey for AI Skill Kit.

\[Omitted image "nask-user-journey.png"\] Alt text: Define your LLM provider, then develop custom skills by specifying input sources and configuring the prompt. Test with data from your instance, and then deploy your new skill.

-   **Define the provider**

    Understand the benefits and potential downsides of each large language model \(LLM\) that you're considering using.

-   **Build the prompt**

    You must have an understanding of the architecture of your Otto instance and be able to define where input data should come from. You should also have an understanding of LLM fundamentals to build an effective prompt.

-   **Test the prompt**

    AI Skill Kit enables you to test your prompt from the editor.

-   **Deploy the skill**

    AI Skill Kit enables you to deploy your skill to ServiceNow Otto panel, ServiceNow Otto Context Menu, Virtual Agent, Flow Action, or a UI Action.


## AI Skill Kit benefits

AI Skill Kit enables you to design your own custom generative AI functionality that is then easily deployed into the ServiceNow platform. Custom skills can augment workflows with generative AI to increase effectiveness and efficiency.

|Benefit|Feature|Users|
|-------|-------|-----|
|Create custom solutions by building a custom skill or workflow.|[Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/create-new-skill.md)|AI developer|
|Create and edit prompts for skills and configure where you want to bring in data from to augment your prompt.|[Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md)|AI developer|
|Test and iterate on your skill before activating it.|[Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md)|AI developer|

## What to explore next

To learn more about configuring and using AI Skill Kit, see:

-   [Configuring AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/configuring-now-assist-skill-kit.md)
-   [Using AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/using-now-assist-skill-kit.md)

