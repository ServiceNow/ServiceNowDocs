---
title: Using AI Skill Kit
description: Use AI Skill Kit to create and publish prompts and custom skills for Otto.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-skill-kit/using-now-assist-skill-kit.html
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [AI Skill Kit, Enable AI experiences]
---

# Using AI Skill Kit

Use AI Skill Kit to create and publish prompts and custom skills for Otto.

Building a custom skill in AI Skill Kit is a sequential process. The following steps take you from an empty skill through to activation, where end users can trigger it from the platform.

## Create a skill

Create a skill or clone an existing base system skill. Clone a Otto skill if it's close to what you need but requires modification.

-   [Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/create-new-skill.md)
-   [Clone and edit a ServiceNow skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/clone-and-edit-servicenow-skill.md)

## Build the prompt

A prompt is an instruction template sent to the AI model when the skill runs. Define what information the skill receives as inputs, write the prompt text, and optionally add tools that gather additional context before the prompt executes.

-   [Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md)
-   [Add a tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/add-a-tool.md)
-   [Add a retriever](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/add-retriever.md)
-   [Add a web search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/add-web-search.md)
-   [Use prompt assistance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/use-prompt-assistance.md)

## Test and evaluate

Before publishing, test your prompt against real records on your instance to verify the output. You can also run a formal evaluation, which measures output quality against expected results using correctness and faithfulness scores.

-   [Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md)
-   [Evaluate a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/evaluate-prompt.md)

## Publish and activate

When your skill is ready, finalize the prompt and publish it. Publishing makes the skill visible to a Otto admin, who then activates it in AI Admin Hub to make it available to your users.

-   [Finalize and publish a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/publish-skill.md)
-   [Activate a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/activate-skill.md)

## Call a skill from a script

After a skill is published, you can call it from a server-side script, so that you can integrate the skill into automated workflows or business rules. For more information, see [Call a custom skill from a script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/call-custom-skill-from-script.md).

-   **[Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/create-new-skill.md)**  
Create a custom skill for Otto. Custom skills extend the generative AI capabilities of Otto to fit your own use cases.
-   **[Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md)**  
After you create a custom skill, create a prompt. The prompt defines the instructions that the skill sends to the LLM and the skill inputs that it uses.
-   **[Use prompt assistance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/use-prompt-assistance.md)**  
Use prompt assistance to start your prompt from an example in the prompt library or from a prompt that ServiceNow Otto generates.
-   **[Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md)**  
After you create a prompt for your custom skill, test it before you finalize it to verify that it returns the expected results.
-   **[Evaluate a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/evaluate-prompt.md)**  
Use the AI Skill Kit evaluation tools to measure how your skill prompts perform against a dataset, using automated metrics and human feedback.
-   **[Finalize and publish a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/publish-skill.md)**  
Finalize at least one prompt and publish your custom skill so that a Otto admin can activate it.
-   **[Activate a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/activate-skill.md)**  
After you create and publish a custom skill, you must activate it in AI Admin Hub. Activating the skill enables you to trigger the skill within the UI.
-   **[Call a custom skill from a script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/call-custom-skill-from-script.md)**  
Call a custom skill from a UI action script so that you can run the skill and use its output in your instance logic.

**Parent Topic:**[AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/now-assist-skill-kit-landing.md)

