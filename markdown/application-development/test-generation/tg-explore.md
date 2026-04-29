---
title: Exploring Test generation
description: If you are new to Test generation application, read this overview to learn what the app can do.
locale: en-US
release: australia
product: Test Generation
classification: test-generation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Test generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Exploring Test generation

If you are new to Test generation application, read this overview to learn what the app can do.

Follow the gif to create tests from natural language leveraging AI power.

![Gif showing the working of Test generation](../image/tg-gif.gif)

## Test generation overview

Revolutionize your test automation with Test generation application. Simply outline your test requirements, and Test generation will generate a comprehensive test script. You can then refine the generated test to meet your exact specifications. It helps you achieve the following:

-   Test generation store application simplifies the process of creating test cases, significantly reducing manual effort and time.
-   You can only provide high-level test requirements, making the process more accessible and less technical.
-   Test generation application generates comprehensive test cases, ensuring thorough testing coverage.
-   You can keep modifying the prompt without saving the generated tests until the final objective has been attained.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Test generation users

Test generation has the following users.

|Users|Description|
|-----|-----------|
|system\_admin + now.assist.creator|This role is required for the setup of the Test generation store application and write Test generation tests.|
|atf\_test\_admin + now.assist.creator|This role is required to setup and write ATF tests, access the Test generation application, and write Test generation tests.|
|atf\_test\_designer + now.assist.creator|This role can write and debug ATF tests, access the Test generation application and write Test generation tests.|
|atf\_ws\_designer + now.assist.creator|This role can access web service modules for test development, build web service tests, write ATF tests, access the Test generation application and write Test generation tests.|

## Test generation benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Automate test generation|[Generate a test using Test generation](../task/tg-implement.md)|System Administrator and Creator Pro|
|Edit a generated test after the preview|[Edit a generated test using Test generation](tg-edit-test.md)|System Administrator and Creator Pro|

## What to explore next

To learn more about using Test generation, see:

-   [Using Test generation](tg-use.md)
-   [Test generation references](tg-reference.md)

**Parent Topic:**[Test generation](test-generation-intro.md)

