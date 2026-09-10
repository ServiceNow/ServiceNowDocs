---
title: AI Skill Kit release notes
description: The ServiceNow AI Skill Kit application enables AI developers to create custom skills and to have greater flexibility with the generative AI capabilities of Now Assist. AI Skill Kit was enhanced and updated in the Zurich release.The ServiceNow AI Skill Kit application enables AI developers to create custom skills and to have greater flexibility with the generative AI capabilities of Now Assist. AI Skill Kit was enhanced and updated in the Zurich release.The ServiceNow AI Skill Kit application enables AI developers to create custom skills and to have greater flexibility with the generative AI capabilities of Now Assist. AI Skill Kit was enhanced and updated in the Zurich release.The ServiceNow AI Skill Kit application enables AI developers to create custom skills and to have greater flexibility with the generative AI capabilities of Now Assist. AI Skill Kit was enhanced and updated in the Zurich release.The ServiceNow AI Skill Kit application enables AI developers to create custom skills and to have greater flexibility with the generative AI capabilities of Now Assist. AI Skill Kit was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# AI Skill Kit release notes

The ServiceNow® AI Skill Kit application enables AI developers to create custom skills and to have greater flexibility with the generative AI capabilities of Now Assist. AI Skill Kit was enhanced and updated in the Zurich release.

## About AI Skill Kit

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Use labeling workflows to annotate UI templates.
-   Use structured output to constrain AI responses to predefined JSON schemas.
-   Improve overisght and compliance with AI Control Tower integration with your custom large language model.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Create a custom model to meet your specific needs and control behavior.
-   Customize ServiceNow skills by modifying the prompt, inputs, and providers.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Set up a security access control list to verify user authentication for AI Skill Kit.
-   Use Document Intelligence as a tool when you create a skill.

-   Use UI Builder to deploy custom skills.
-   Use a custom data generator to create synthetic datasets.

See [AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skill-kit-landing.md) for more information.

## Activation and other requirements

**Important:** AI Skill Kit is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Now Assist features are available with activation of any Now Assist plugins from ServiceNow Store. The following plugins are available:

-   **Browser requirements**

    Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.


## Accessibility and localization

-   **Localization information**

    Now Assist supports Dynamic Translation for Zurich.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/intelligent-experiences-rn-landing.md)

## March 2026

The ServiceNow® AI Skill Kit application enables AI developers to create custom skills and to have greater flexibility with the generative AI capabilities of Now Assist. AI Skill Kit was enhanced and updated in the Zurich release.

### What's new

-   **[Labelling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/nadk-labelling.md)Use labeling workflows to annotate UI templates**

    Use the labeling framework to create and manage ground truth data. Published data collections can now be turned into labeling projects. Each record becomes a task assigned to labelers who annotate using pre-configured UI templates

-   **[s](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-skill-prompt.md)Structured output support for AI responses**

    Enables consistent parsing in agentic workflows and reduces ambiguity in downstream automation.

-   **[Use multi-table data generator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/use-multi-table-data-generator.md)New multi-table synthetic data generation option**

    You can generate related records across multiple tables in a single operation. You no longer need to generate each table separately and manually link records. Define your table relationships, set the cardinality and AI Data Kit generates coherent, referentially linked records across all tables in one pass, with foreign key integrity maintained automatically. 

-   **[Create a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-model.md)AI Control Tower integration with custom LLMs.**

    Improve oversight and compliance for AI deployments with formal approval flows for custom models.

-   **[AI Skill Kit roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/na-skill-kit-roles.md)Update to the abilities of the admin role**

    The sn\_skill\_builder.admin role is now broken into smaller, task-specific roles, including a custom LLM-specific admin role.


## January 2026

The ServiceNow® AI Skill Kit application enables AI developers to create custom skills and to have greater flexibility with the generative AI capabilities of Now Assist. AI Skill Kit was enhanced and updated in the Zurich release.

### What's changed

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## December 2025

The ServiceNow® AI Skill Kit application enables AI developers to create custom skills and to have greater flexibility with the generative AI capabilities of Now Assist. AI Skill Kit was enhanced and updated in the Zurich release.

### What's new

-   **[Create a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-model.md)**

    When you bring your own model you can keep data in your own environment and fine-tune it to meet your specific needs.


## Zurich

The ServiceNow® AI Skill Kit application enables AI developers to create custom skills and to have greater flexibility with the generative AI capabilities of Now Assist. AI Skill Kit was enhanced and updated in the Zurich release.

### What's new

-   **[New third-party AI model provider options available for all AI applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.

-   **[New skill deployment option](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-skill-settings.md)**

    Deploy skills using UI Builder.

-   **[Choose a language for data generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/na-data-kit-generate-data.md)**

    When you create synthetic data, you can select what language you want to receive the data in.

-   **AI-assisted ground truth**

    Use AI to assist creating ground truth for your data.

-   **[Import data with a CSV file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/add-dataset.md)**

    Import data from a CSV file to create a dataset.

-   **Create a custom data generator**

    Create and use a custom data generator to create synthetic data.


