---
title: Combined Generative AI Controller release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Generative AI Controller from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-generativeaicontroller-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Generative AI Controller release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Generative AI Controller from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Generative AI Controller release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Generative AI Controller to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Generative AI Controller.

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

-   **[Administrator access to Gen AI log](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=yokohama&ft:locale=en-US)**

Access the Gen AI log \[sys\_generative\_ai\_log\] table to gain insights for debugging purposes. HR-related records remain restricted to HR admins.

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


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Generative AI Controller features.

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

-   **[Some Now Assist skills are now turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   ****

-   **[Configure Data Privacy and Data Discovery to protect the personally identifying information \(PII\) of your users.](https://www.servicenow.com/docs/access?context=configure-now-assist-data-privacy&family=yokohama&ft:locale=en-US)**

Generative AI Controller has changed to use the Data Privacy application instead of the Sensitive Data Handler to help anonymize PII. The process for choosing what gets anonymized and how has shifted to different tables and forms that your administrator must configure for your organization.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Generative AI Controller features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Generative AI Controller features or functionality were deprecated.

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

