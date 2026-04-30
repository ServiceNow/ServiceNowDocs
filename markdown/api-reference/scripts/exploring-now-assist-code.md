---
title: Exploring code generation
description: Learn about how AI-generated code can empower developers scripting on the ServiceNow AI Platform.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Now Assist for code generation, Scripting, API implementation, API implementation and reference]
---

# Exploring code generation

Learn about how AI-generated code can empower developers scripting on the ServiceNow AI Platform.

Now Assist for Code supports both the Now LLM Service and Azure OpenAI model providers.

This capability is a part of Creator Pro Plus offering and includes the following skills:

-   Code generation
-   Code editing
-   Code explain and summarize
-   Code autocomplete

You can switch between Now LLM Services and Azure OpenAI. For more information, see [Exploring code generation](exploring-now-assist-code.md)

## Code generation overview

Now Assist for Creator activates the code generation skill. With code generation, you provide text describing the code to generate and get code suggestions in the JavaScript editor on forms in the ServiceNow AI Platform and in Script steps in Workflow Studio. Developers with varying levels of experience in scripting on the ServiceNow AI Platform can benefit from using code generation to get started writing custom scripts or iterate on scripts more efficiently.

To generate code suggestions, you describe the goal of the code to generate in the Code with Now Assist dialog box. The code suggestion appears in the lines following your prompt but isn’t added to your script until it's accepted.

![Code with Now Assist dialog box with the text "Validate emails using regex" and a code suggestion in the script editor.](../image/now-assist-code-dialog.png)

**Note:** Developers must be assigned the now.assist.creator role to use code generation. For more information about using code generation, see [Generate scripts with AI-powered code generation](generate-code.md#).

## Code generation workflow

1.  From the script editor, a developer opens the Code with Now Assist dialog box and describes the code that they want to generate.
2.  The developer triggers generating a code suggestion.

    In the following example, a developer describes what they want the script to do in the Code with Now Assist dialog box. The code suggestion appears highlighted in the script editor.![Code with Now Assist dialog box with the text "Validate emails using regex" and a code suggestion in the script editor.](../image/now-assist-code-dialog.png)

3.  The developer reviews the AI-generated code suggestion and either accepts or rejects it.

    -   If the developer accepts it, the code is added to the script. The developer can make any necessary edits based on further review.
    -   If the developer rejects it, the code isn’t added to the script. The developer can rephrase the prompt to generate a new code suggestion.
    In the following example, a line next to the line numbers indicates which code was created by AI and hasn't been edited. If you edit AI-generated code, the line indicator doesn’t appear for those lines of code.

    ![Line that indicates which lines of code are AI-generated.](../image/now-assist-code-indicator-modal.png "AI-generated code lines")


Optionally, you can turn on code completion functionality to use code or single-shot prompts in script editors with Now Assist for code generation.

## Code autocomplete overview

The autocomplete feature of Now Assist for Code provides you with contextually relevant code suggestions while typing.

**Note:** It takes a few seconds for the code suggestions to appear.

## Code autocomplete workflow

1.  A developer begins coding in the script editor.

    Within a few seconds, contextually relevant code suggestions are displayed in grey.

2.  The developer reviews the AI-generated code suggestions and either accepts or rejects them:
    -   The developer must press the **tab** key to accept the suggestions.

        If the developer accepts, the code is added to the script.

    -   The developer must press the **esc** key to reject the suggestions.

        If the developer rejects, the code isn’t added. The developer can continue to code and wait for a few seconds for the suggestions to appear.

3.  After accepting the code suggestions, the developer selects **Update** to save the script.

## Code explain and summarize overview

The code explain and summarize features are only available with the Azure OpenAI model provider.

The code explain and summarize features provide a summary of the code and a comprehensive explanation of its functionality.

## Code generation benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Improve quality of scripts, automate repetitive coding tasks, and reduce time spent searching for or recalling code|[Text-to-code and code complete](generate-code.md#)|Developers|
|Identify code generated by AI|[Tracking AI-generated code](tracking-ai-generated-code.md#)|Developers, administrators|

