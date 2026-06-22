---
title: Combined Generative AI Controller release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Generative AI Controller from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-generativeaicontroller-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Generative AI Controller release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Generative AI Controller from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Generative AI Controller release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Generative AI Controller to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Generative AI Controller is installed and updated when you install or update any Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) for steps that may address your issue. Otherwise, you can make a Support case.

</td></tr><tr><td>

Zurich

</td><td>

Generative AI Controller is installed or updated when you install or update a Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) or open a support case.

</td></tr><tr><td>

Australia

</td><td>

Generative AI Controller is installed or updated when you install or update a Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) or open a support case.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Generative AI Controller.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Metadata log table for generative AI requests](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=xanadu&ft:locale=en-US)**

Use the new metadata log table that includes information about the requesting conversation, the capability definition, provided feedback \(if any\), and error codes.

-   **[Translation for Now Assist](https://www.servicenow.com/docs/access?context=translation-for-now-assist&family=xanadu&ft:locale=en-US)**

Support users who speak different languages with new language information in LLM request metadata, better controls for Dynamic Translation, and translated text logging.


-   **Global Model selection for conversational skills**

Enable Now Assist Admins to choose between GPT4.o and Now Assist LLM model for data routing at a global level. This ensures compliance with any regional restrictions and helpful for APAC users who may face limitations with US-based models, such as GPT-4.0.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[\[Placeholder link text to key configure-custom-resource-path-byok\]](https://www.servicenow.com/docs/access?context=configure-custom-resource-path-byok&family=yokohama&ft:locale=en-US)**

Connect Generative AI Controller to your Azure OpenAI deployment by configuring a custom resource path in your bring your own key \(BYOK\) model configuration. Use this when your Azure OpenAI endpoint includes a path segment that Generative AI Controller does not add by default.


-   **[Administrator access to Gen AI log](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=yokohama&ft:locale=en-US)**

Access the Gen AI log \[sys\_generative\_ai\_log\] table to gain insights for debugging purposes. Records related to HR remain restricted to HR admins.

-   **[Enhanced AI asset inventory](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=yokohama&ft:locale=en-US)**

Track the enhanced AI asset inventory through AI Control Tower using new metadata fields in the Model \[sys\_generative\_ai\_model\_config\] and Prompt \[sys\_generative\_ai\_config\] tables. Gain better visibility into AI asset status and life-cycle details, such as retirement dates.


-   **[AI Model Version Mappings](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=yokohama&ft:locale=en-US)**

Review the mappings between AI model versions, their providers in the Gen AI Model Version Mapping \[sys\_gen\_ai\_model\_version\_mapping\] table. It shows mapping between source and target models, along with associated metadata, such as skill type, model type, resource associations, and provider information.


-   **[Identify third-party LLM information](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=yokohama&ft:locale=en-US)**

Access the Gen AI Log Metadata \[sys\_gen\_ai\_log\_metadata\] table to identify which LLM model, version, and requested language was used to generate the AI content.

-   **[Restrict LLM usage based on the domain](https://www.servicenow.com/docs/access?context=generative-ai-controller-rn&family=yokohama&ft:locale=en-US)**

Enable or disable Now Assist for each domain so that you can restrict the use of LLMs and avoid using AI for data processing, if needed.


-   **[Global Model selection for conversational skills](https://www.servicenow.com/docs/access?context=manage-large-language-models&family=yokohama&ft:locale=en-US)**

Enable Now Assist Admins to choose between GPT4.o and Now Assist LLM model for data routing at a global level. This ensures compliance with any regional restrictions and helpful for APAC users who may face limitations with US-based models, such as GPT-4.0.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Extended log retention for generative AI events](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=zurich&ft:locale=en-US)**

Retain records in the Generative AI Log \[sys\_generative\_ai\_log\] table for 180 days, up from 30 days, to stay compliant with retention requirements.


-   **[Configure a custom resource path for BYOK models](https://www.servicenow.com/docs/access?context=configure-custom-resource-path-byok&family=zurich&ft:locale=en-US)**

Connect Generative AI Controller to your Azure OpenAI deployment by configuring a custom resource path in your bring your own key \(BYOK\) model configuration. Use this when your Azure OpenAI endpoint includes a path segment that Generative AI Controller does not add by default.


-   **[Administrator access to Gen AI log](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=zurich&ft:locale=en-US)**

Access the Gen AI log \[sys\_generative\_ai\_log\] table to gain insights for debugging purposes. HR-related records remain restricted to HR admins.

-   **[Enhanced AI asset inventory](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=zurich&ft:locale=en-US)**

Track the enhanced AI asset inventory through AI Control Tower using new metadata fields in the Model \[sys\_generative\_ai\_model\_config\] and Prompt \[sys\_generative\_ai\_config\] tables. Gain better visibility into AI asset status and life-cycle details, such as retirement dates.

-   **[Long-Term Stable model for generative AI](https://www.servicenow.com/docs/access?context=long-term-stable-models&family=zurich&ft:locale=en-US)**

Promote stability and adoption for entitled users with a Long-Term Stable \(LTS\) model. The LTS model provides regulatory alignment, predictable behavior, and life cycle stability to integrate GenAI with confidence.


-   **[AI Model Version Mappings](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=zurich&ft:locale=en-US)**

Review the mappings between AI model versions and their providers in the Gen AI Model Version Mapping \[sys\_gen\_ai\_model\_version\_mapping\] table. This table shows the mappings between source and target models, along with associated metadata, such as skill type, model type, resource associations, and provider information.


-   **[Identify third-party LLM information](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=zurich&ft:locale=en-US)**

Access the Gen AI Log Metadata \[sys\_gen\_ai\_log\_metadata\] table to identify which LLM model, version, and requested language was used to generate the AI content.

-   **[Restrict LLM usage based on the domain](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=zurich&ft:locale=en-US)**

Enable or disable Now Assist for each domain so that you can restrict the use of LLMs and avoid using AI for data processing, if needed.


</td></tr><tr><td>

Australia

</td><td>

-   **[Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)**
-   **[Extended log retention for generative AI events](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=australia&ft:locale=en-US)**

Retain records in the Generative AI Log \[sys\_generative\_ai\_log\] table for 180 days, up from 30 days, to stay compliant with retention requirements.

-   **[Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)**
-   **[Configure a custom resource path for BYOK models](https://www.servicenow.com/docs/access?context=configure-custom-resource-path-byok&family=australia&ft:locale=en-US)**

Connect Generative AI Controller to your Azure OpenAI deployment by configuring a custom resource path in your bring your own key \(BYOK\) model configuration. Use this when your Azure OpenAI endpoint includes a path segment that Generative AI Controller does not add by default.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Generative AI Controller features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Directions for generative AI updates for Generative AI Controller](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=xanadu&ft:locale=en-US)**

The prompts, which are the instructions to the large language model \(LLM\), for all four capabilities \(Generic Prompt, Generate Content, Summarization, and Sentiment Analysis\), semantic filtering, and recursive summarization have been updated.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   ****

-   **[Configure Data Privacy and Data Discovery to protect the personally identifying information \(PII\) of your users.](https://www.servicenow.com/docs/access?context=configure-now-assist-data-privacy&family=yokohama&ft:locale=en-US)**

Generative AI Controller has changed to use the Data Privacy application instead of the Sensitive Data Handler to help anonymize PII. The process for choosing what gets anonymized and how has shifted to different tables and forms that your administrator must configure for your organization.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Direct action calls removed from Generative AI Controller](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&family=zurich&ft:locale=en-US)**

Starting with Zurich Patch 5, the Generative AI Controller \(GAIC\) no longer supports direct action calls in order to support the security requirements that all AI capabilities be protected by Access Control Lists \(ACLs\). To create custom generative AI functionality, use Now Assist Skill Kit instead.

    -   Configure actions in the Generative AI Controller
    -   Generate Content to create AI-generated text responses
    -   QnA to answer user questions
    -   Summarize to shorten long or complex text
    -   Generic Prompt to generate ideas or content on any topic
    -   Sentiment Analysis to identify the sentiment of user input
For more information, refer to [KB KB2716977: Generative AI Controller actions are no longer avaliable for custom workflows](https://support.servicenow.com/kb?sys_kb_id=6460540047ee7a9048cb2920326d4302&id=kb_article_view).


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Generative AI Controller features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Generative AI Controller features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

The dependency on Sensitive Data Handler has been removed. Regular expressions that are configured with Sensitive Data Handler are applied to the Data Privacy application with a fix script when you upgrade to Yokohama.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Generative AI Controller.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Generative AI Controller is a ServiceNow AI Platform feature that is available with activation of any ServiceNow® Now Assist application. For details, see [Installing Generative AI Controller](https://www.servicenow.com/docs/access?context=installing-generative-ai-controller&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Generative AI Controller is a ServiceNow AI Platform feature that is available with activation of a Now Assist application. For details, see [Installing Generative AI Controller](https://www.servicenow.com/docs/access?context=installing-generative-ai-controller&family=yokohama&ft:locale=en-US) and [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Generative AI Controller is a ServiceNow AI Platform feature that is available with activation of a Now Assist application. For details, see [Installing Generative AI Controller](https://www.servicenow.com/docs/access?context=installing-generative-ai-controller&family=zurich&ft:locale=en-US) and [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Generative AI Controller is a ServiceNow AI Platform feature that is available with activation of a Now Assist application. For details, see [Installing Generative AI Controller](https://www.servicenow.com/docs/access?context=installing-generative-ai-controller&family=australia&ft:locale=en-US) and [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Generative AI Controller we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Generative AI Controller we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Generative AI Controller, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Generative AI Controller we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Generative AI Controller uses [Microsoft Azure OEM for Dynamic Translation in Now Assist](https://www.servicenow.com/docs/access?context=dynamic-translation-na-ms-azure-oem&family=xanadu&ft:locale=en-US) for multi-language support. You can enable dynamic translation from the Now Assist Admin console.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Generative AI Controller uses Microsoft Azure OEM for Dynamic Translation in Now Assist for multilanguage support. You can enable dynamic translation from the Now Assist Admin console. For more information, see [Microsoft Azure OEM for Dynamic Translation in Now Assist](https://www.servicenow.com/docs/access?context=dynamic-translation-na-ms-azure-oem&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Generative AI Controller uses Microsoft Azure OEM for Dynamic Translation in Now Assist for multilanguage support. You can enable dynamic translation from the Now Assist Admin console. For more information, see [Microsoft Azure OEM for Dynamic Translation in Now Assist](https://www.servicenow.com/docs/access?context=dynamic-translation-na-ms-azure-oem&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Generative AI Controller we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Xanadu Patch 3

-   Review a read-only metadata log table for generative AI requests.
-   Use the improved language support for skills and capabilities, including the Dynamic Translation services and native translation by the LLMs.

 Xanadu Patch 1

-   Updated prompts for capabilities, semantic filtering, and recursive summarization that improve latency and processing for Generative AI Controller capabilities and Now Assist skills.

 See [Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://www.servicenow.com/docs/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

 Previous Patch releases

-   Protect your users by configuring settings for anonymization of personally identifiable information \(PII\) with the Data Privacy application.

 See [Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 10](https://www.servicenow.com/docs/access?context=zurich-patch-10&family=zurich&ft:locale=en-US)

-   Generative AI event logs are now retained for 180 days, up from 30 days.

 [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US)

-   Connect your Azure OpenAI deployment to Generative AI Controller by configuring a custom resource path in your bring your own key \(BYOK\) model configuration.

 [Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Access the Gen AI log for debugging insights, with HR-related records remaining restricted.
-   Promote stability with the Long-Term Stable \(LTS\) model for generative AI.

 -   Identify third-party LLM information, including model, version, and language.
-   Restrict LLM usage based on domain.

 See [Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)Generative AI event logs are now retained for 180 days, up from 30 days.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)Connect your Azure OpenAI deployment to Generative AI Controller by configuring a custom resource path in your bring your own key \(BYOK\) model configuration.

 See [Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

