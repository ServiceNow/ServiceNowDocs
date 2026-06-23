---
title: Exploring Now Assist Skill Kit
description: The Now Assist Skill Kit plugin for Now Assist enables you to create and activate custom prompts and skills for Now Assist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/intelligent-experiences/now-assist-skill-kit/exploring-now-assist-skill-kit.html
release: xanadu
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: concept
last_updated: "2024-08-13"
reading_time_minutes: 2
breadcrumb: [Now Assist Skill Kit, Enable AI experiences]
---

# Exploring Now Assist Skill Kit

The Now Assist Skill Kit plugin for Now Assist enables you to create and activate custom prompts and skills for Now Assist.

## Now Assist Skill Kit overview

If the base system Now Assist skills don't fit your needs, you can use Now Assist Skill Kit to create custom skills. These custom skills enable you to have greater flexibility with Now Assist's generative AI capabilities.

## Get Now Assist Skill Kit

To use Now Assist Skill Kit, you must update your Now Assist plugins in the [Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/application-manager/exploring-application-manager.md). For example, update your Now Assist for ITSM plugin to the Xanadu release.

You must also assign the sn\_skill\_builder.admin role to anyone who uses Now Assist Skill Kit.

## Now Assist Skill Kit users

|User|Description|
|----|-----------|
|AI developer|AI developers manage skill development in Now Assist Skill Kit. They create new skills, write the prompts, and configure the skill settings.|
|Now Assist admin|Now Assist admins activate published skills.|

## Now Assist Skill Kit workflow

The following diagram shows the user journey for Now Assist Skill Kit.

\[Omitted image "nask-user-journey.png"\] Alt text: Journey for users to define, build, test, and deploy skills.

1.  Define the provider

    You must understand the benefits and potential downsides of each large language model \(LLM\) that you are considering using.

2.  Build the prompt

    You must have an understanding of the architecture of your Now Assist instance and be able to define where input data should come from. You should also have an understanding of LLM fundamentals to build an effective prompt.

3.  Test the prompt

    Now Assist Skill Kit enables you to test your prompt from the editor.

4.  Deploy the skill

    Now Assist Skill Kit enables you to deploy your skill directly to a UI action.


## Now Assist Skill Kit benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Create custom solutions by building a custom skill or workflow.|[Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/now-assist-skill-kit/create-new-skill.md)|AI developer|
|Create and edit prompts for skills and configure where you want to bring in data from to augment your prompt.|[Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md)|AI developer|
|Test and iterate on your skill before activating it.|[Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md)|AI developer|

## What to explore next

To learn more about configuring and using Now Assist Skill Kit, see:

-   [Configuring Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/now-assist-skill-kit/configuring-now-assist-skill-kit.md)
-   [Using Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/now-assist-skill-kit/using-now-assist-skill-kit.md)

