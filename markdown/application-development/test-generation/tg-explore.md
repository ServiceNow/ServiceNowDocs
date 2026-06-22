---
title: Exploring Test generation
description: If you are new to Test generation application, read this overview to learn what the app can do.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/test-generation/tg-explore.html
release: zurich
product: Test Generation
classification: test-generation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Test generation, Testing and debugging applications, Building applications]
---

# Exploring Test generation

If you are new to Test generation application, read this overview to learn what the app can do.

Follow the gif to create tests from natural language leveraging AI power.

\[Omitted image "tg-gif.gif"\] Alt text: Gif showing the working of Test generation

## Test generation overview

Revolutionize your test automation with Test generation application. Simply outline your test requirements, and Test generation will generate a comprehensive test script. You can then refine the generated test to meet your exact specifications. It helps you achieve the following:

-   Test generation store application simplifies the process of creating test cases, significantly reducing manual effort and time.
-   You can only provide high-level test requirements, making the process more accessible and less technical.
-   Test generation application generates comprehensive test cases, ensuring thorough testing coverage.
-   You can keep modifying the prompt without saving the generated tests until the final objective has been attained.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-control-tower/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

## Test generation users

Test generation has the following users.

|Users|Description|
|-----|-----------|
|system\_admin|This role is required for the setup of the Test generation store application and write Test generation tests.|
|atf\_test\_admin|This role is required to setup and write ATF tests, access the Test generation application, and write Test generation tests.|
|atf\_test\_designer|This role can write and debug ATF tests, access the Test generation application and write Test generation tests.|
|atf\_ws\_designer|This role can access web service modules for test development, build web service tests, write ATF tests, access the Test generation application and write Test generation tests.|

## Test generation benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Automate test generation|[Generate a test using Test generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/test-generation/tg-implement.md)|System Administrator|
|Edit a generated test after the preview|[Edit a generated test using Test generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/test-generation/tg-edit-test.md)|System Administrator|

## What to explore next

To learn more about using Test generation, see:

-   [Using Test generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/test-generation/tg-use.md)
-   [Test generation references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/test-generation/tg-reference.md)

