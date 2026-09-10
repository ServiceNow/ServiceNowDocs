---
title: Generative AI Controller release notes
description: The ServiceNow Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.The ServiceNow Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.The ServiceNow Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.The ServiceNow Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.The ServiceNow Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.The ServiceNow Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.The ServiceNow Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# Generative AI Controller release notes

The ServiceNow® Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.

## About Generative AI Controller

[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

-   Generative AI event logs are now retained for 180 days, up from 30 days.

[Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)

-   Connect your Azure OpenAI deployment to Generative AI Controller by configuring a custom resource path in your bring your own key \(BYOK\) model configuration.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Access the Gen AI log for debugging insights, with HR-related records remaining restricted.
-   Promote stability with the Long-Term Stable \(LTS\) model for generative AI.

-   Identify third-party LLM information, including model, version, and language.
-   Restrict LLM usage based on domain.

See [Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/generative-ai-controller.md) for more information.

## Activation and other requirements

**Important:** Generative AI Controller is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Generative AI Controller is a ServiceNow AI Platform feature that is available with activation of a Now Assist application. For details, see [Installing Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/installing-generative-ai-controller.md) and [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

-   **Upgrade information**

    Generative AI Controller is installed or updated when you install or update a Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) or open a support case.


## Accessibility and localization

-   **Localization information**

    Generative AI Controller uses Microsoft Azure OEM for Dynamic Translation in Now Assist for multilanguage support. You can enable dynamic translation from the AI Admin Hub console. For more information, see [Microsoft Azure OEM for Dynamic Translation in Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/dynamic-translation-na-ms-azure-oem.md).


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/intelligent-experiences-rn-landing.md)

## June 2026

The ServiceNow® Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.

### What's new

-   **[Extended log retention for generative AI events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Retain records in the Generative AI Log \[sys\_generative\_ai\_log\] table for 180 days, up from 30 days, to stay compliant with retention requirements.


## April 2026

The ServiceNow® Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.

### What's new

-   **[Configure a custom resource path for BYOK models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-custom-resource-path-byok.md)**

    Connect Generative AI Controller to your Azure OpenAI deployment by configuring a custom resource path in your bring your own key \(BYOK\) model configuration. Use this when your Azure OpenAI endpoint includes a path segment that Generative AI Controller does not add by default.


## January 2026

The ServiceNow® Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.

### What's changed

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Direct action calls removed from Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skill-kit-landing.md)**

    Starting with Zurich Patch 5, the Generative AI Controller \(GAIC\) no longer supports direct action calls in order to support the security requirements that all AI capabilities be protected by Access Control Lists \(ACLs\). To create custom generative AI functionality, use AI Skill Kit instead.

    -   Configure actions in the Generative AI Controller
    -   Generate Content to create AI-generated text responses
    -   QnA to answer user questions
    -   Summarize to shorten long or complex text
    -   Generic Prompt to generate ideas or content on any topic
    -   Sentiment Analysis to identify the sentiment of user input
    For more information, refer to [KB KB2716977: Generative AI Controller actions are no longer avaliable for custom workflows](https://support.servicenow.com/kb?sys_kb_id=6460540047ee7a9048cb2920326d4302&id=kb_article_view).


## December 2025

The ServiceNow® Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.

### What's new

-   **[Administrator access to Gen AI log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Access the Gen AI log \[sys\_generative\_ai\_log\] table to gain insights for debugging purposes. HR-related records remain restricted to HR admins.

-   **[Enhanced AI asset inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Track the enhanced AI asset inventory through AI Control Tower using new metadata fields in the Model \[sys\_generative\_ai\_model\_config\] and Prompt \[sys\_generative\_ai\_config\] tables. Gain better visibility into AI asset status and life-cycle details, such as retirement dates.

-   **[Long-Term Stable model for generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/long-term-stable-models.md)**

    Promote stability and adoption for entitled users with a Long-Term Stable \(LTS\) model. The LTS model provides regulatory alignment, predictable behavior, and life cycle stability to integrate GenAI with confidence.


## October 2025

The ServiceNow® Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.

### What's new

-   **[AI Model Version Mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Review the mappings between AI model versions and their providers in the Gen AI Model Version Mapping \[sys\_gen\_ai\_model\_version\_mapping\] table. This table shows the mappings between source and target models, along with associated metadata, such as skill type, model type, resource associations, and provider information.


## Zurich

The ServiceNow® Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.

### What's new

-   **[Identify third-party LLM information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Access the Gen AI Log Metadata \[sys\_gen\_ai\_log\_metadata\] table to identify which LLM model, version, and requested language was used to generate the AI content.

-   **[Restrict LLM usage based on the domain](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Enable or disable Now Assist for each domain so that you can restrict the use of LLMs and avoid using AI for data processing, if needed.


