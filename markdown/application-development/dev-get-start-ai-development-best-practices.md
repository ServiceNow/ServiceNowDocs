---
title: General guidelines for AI-assisted development
description: When using AI-assisted tools to build or vibe code applications and app components on the ServiceNow AI Platform, the quality of the output depends on the quality of your instructions. Use these guidelines to write effective instructions and improve the products of your conversations with AI tools.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-31"
reading_time_minutes: 2
breadcrumb: [Use AI to build apps faster, Getting Started guide for developers, Building applications]
---

# General guidelines for AI-assisted development

When using AI-assisted tools to build or vibe code applications and app components on the ServiceNow AI Platform, the quality of the output depends on the quality of your instructions. Use these guidelines to write effective instructions and improve the products of your conversations with AI tools.

A prompt or instruction is the primary input an AI tool uses to determine what to produce. Unlike a keyword search, generative and agentic AI treats your input as a task to complete. The quality of the output depends directly on the quality of the input. Therefore, instructions that are clear and specific produce the most accurate, usable results. A well-constructed instruction includes a goal, context, expectations, and optionally a source. Use the following guidelines to help you draft your instructions.

-   **Goal**

    A goal describes what you want the AI to produce or do. In describing your goal, lead with an action verb and be specific. For example, `Create a table for travel requests with fields for employee name, destination, and trip duration`.

-   **Context**

    Context describes the purpose of the application and the types of users it serves. Context helps the AI to generate appropriate roles, permissions, and interfaces.

-   **Expectations**

    Expectations describe how the application or output should look and sound. In your expectations prompts, specify tone, format, and structure.

-   **Source**

    If there are specific information or resources the AI should use to generate your application or app component, describe those sources in your instructions. For example, direct the AI to specific tables or existing knowledge articles.


When working with Build Agent or Now Assist for Creator skills such as app generation, these guidelines apply across the entire conversation, rather than just a single prompt. For detailed guidance and examples, see [General guidelines for using app generation](../../now-assist-app-gen/concept/sns-app-gen-guidelines.md).

**Important:**

Regardless of which AI tool you use, be sure to review AI-generated output before deploying the application or app component to a production instance. Verify that tables, fields, flows, scripts, and access controls match your requirements, and test generated logic to confirm that it behaves as expected.

## Additional resources

See the following additional resources for more information about prompting AI.

-   General guidelines for writing instructions for generative AI large language models \(LLMs\)
-   [General guidelines for using app generation](../../now-assist-app-gen/concept/sns-app-gen-guidelines.md)
-   [Now Assist for Creator skill and prompting guides](https://www.servicenow.com/community/now-assist-for-creator-articles/now-assist-for-creator-skill-and-prompting-guides/ta-p/3125858)

**Parent Topic:**[Use AI to build apps faster](dev-get-start-use-ai-to-build-faster.md)

