---
title: Exploring Now Assist Skill Kit
description: The Now Assist Skill Kit plugin for Now Assist enables you to create and activate custom prompts and skills for Now Assist.
locale: en-US
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Now Assist Skill Kit, Enable AI experiences]
---

# Exploring Now Assist Skill Kit

The Now Assist Skill Kit plugin for Now Assist enables you to create and activate custom prompts and skills for Now Assist.

## Now Assist Skill Kit overview

If the base system Now Assist skills don't fit your needs, you can use Now Assist Skill Kit to create custom skills. These custom skills enable you to have greater flexibility with Now Assist's generative AI capabilities.

## Get Now Assist Skill Kit

To use Now Assist Skill Kit, you must update your Now Assist plugins in the Application Manager. For example, update your Now Assist for ITSM plugin to the Xanadu release.

You must also assign the sn\_skill\_builder.admin role to anyone who uses Now Assist Skill Kit.

## Now Assist Skill Kit users

|User|Description|
|----|-----------|
|AI developer|AI developers manage skill development in Now Assist Skill Kit. They create new skills, write the prompts, and configure the skill settings.|
|Now Assist admin|Now Assist admins activate published skills.|

## Now Assist Skill Kit workflow

The following diagram shows the user journey for Now Assist Skill Kit.

![Define your LLM provider, then develop custom skills by specifying input sources and configuring the prompt. Test with data from your instance, and then deploy your new skill.](../image/nask-user-journey.png "User journey for Now Assist Skill Kit")

1.  Define the provider

    You must understand the benefits and potential downsides of each large language model \(LLM\) that you are considering using.

2.  Build the prompt

    You must have an understanding of the architecture of your Now Assist instance and be able to define where input data should come from. You should also have an understanding of LLM fundamentals to build an effective prompt.

3.  Test the prompt

    Now Assist Skill Kit enables you to test your prompt from the editor.

4.  Deploy the skill

    Now Assist Skill Kit enables you to deploy your skill to Now Assist panel, Now Assist Context Menu, Virtual Agent, Flow Action, or a UI Action.


## Now Assist Skill Kit benefits

Now Assist Skill Kit enables you to design your own custom generative AI functionality that is then easily deployed into the ServiceNow platform. Custom skills can be used to augment workflows with generative AI, allowing for increased effectiveness and efficiency.

|Benefit|Feature|Users|
|-------|-------|-----|
|Create custom solutions by building a custom skill or workflow.|[Create a skill](../task/create-new-skill.md)|AI developer|
|Create and edit prompts for skills and configure where you want to bring in data from to augment your prompt.|[Create a prompt](../task/create-prompt-template.md)|AI developer|
|Test and iterate on your skill before activating it.|[Test a prompt](../task/test-prompt-template.md)|AI developer|

## What to explore next

To learn more about configuring and using Now Assist Skill Kit, see:

-   [Configuring Now Assist Skill Kit](configuring-now-assist-skill-kit.md)
-   [Using Now Assist Skill Kit](using-now-assist-skill-kit.md)

