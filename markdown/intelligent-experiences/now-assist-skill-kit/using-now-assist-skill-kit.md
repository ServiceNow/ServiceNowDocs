---
title: Using Now Assist Skill Kit
description: Use Now Assist Skill Kit to create and publish prompts and custom skills for Now Assist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-skill-kit/using-now-assist-skill-kit.html
release: zurich
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: concept
last_updated: "2026-05-19"
reading_time_minutes: 4
breadcrumb: [Now Assist Skill Kit, Enable AI experiences]
---

# Using Now Assist Skill Kit

Use Now Assist Skill Kit to create and publish prompts and custom skills for Now Assist.

Building a custom skill in Now Assist Skill Kit is a sequential process. The following steps take you from an empty skill through to activation, where end users can trigger it from the platform.

## Create a skill

Create a skill or clone an existing base system skill. Clone a Now Assist skill if it's close to what you need but requires modification.

-   [Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/create-new-skill.md)
-   [Clone and edit a ServiceNow skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/clone-and-edit-servicenow-skill.md)

## Build the prompt

A prompt is an instruction template sent to the AI model when the skill runs. Define what information the skill receives as inputs, write the prompt text, and optionally add tools that gather additional context before the prompt executes.

-   [Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md)
-   [Add a tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/add-a-tool.md)
-   [Add a retriever](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/add-retriever.md)
-   [Add a web search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/add-web-search.md)
-   [Use prompt assistance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/use-prompt-assistance.md)

## Test and evaluate

Before publishing, test your prompt against real records on your instance to verify the output. You can also run a formal evaluation, which measures output quality against expected results using correctness and faithfulness scores.

-   [Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md)
-   [Evaluate a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/evaluate-prompt.md)

## Publish and activate

When your skill is ready, finalize the prompt and publish it. Publishing makes the skill visible to a Now Assist admin, who then activates it in Now Assist Admin to make it available to your users.

-   [Finalize and publish a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/publish-skill.md)
-   [Activate a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/activate-skill.md)

## Call a skill from a script

After a skill is published, you can call it from a server-side script, allowing you to integrate the skill into automated workflows or business rules.

-   [Call a custom skill from a script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/call-custom-skill-from-script.md)

-   **[Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/create-new-skill.md)**  
Create a custom skill for Now Assist. Creating a custom skill enables you to have greater flexibility with Now Assist's generative AI capabilities.
-   **[Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md)**  
After you create a custom skill, create a prompt. Creating a prompt enables you to choose what skill inputs to use, as well as the type of tool.
-   **[Use prompt assistance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/use-prompt-assistance.md)**  
Use prompt assistance to get a jump start with your prompt development by selecting an example from the prompt library or using Now Assist to generate one.
-   **[Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md)**  
After you create a prompt for your custom skill, test the prompt template before you finalize it. Testing the prompt verifies that you’re seeing the expected prompt results before it’s activated.
-   **[Evaluate a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/evaluate-prompt.md)**  
Use the Now Assist Skill Kit evaluation tools to evaluate the effectiveness of your skill prompts.
-   **[Finalize and publish a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/publish-skill.md)**  
When you’re satisfied with your prompt, you can publish your custom skill. Publishing the skill enables a Now Assist admin to activate it.
-   **[Activate a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/activate-skill.md)**  
After you create and publish a custom skill, you must activate it in Now Assist Admin. Activating the skill enables you to trigger the skill within the UI.
-   **[Call a custom skill from a script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/call-custom-skill-from-script.md)**  
You can use a script to call a custom skill.

**Parent Topic:**[Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/now-assist-skill-kit-landing.md)

