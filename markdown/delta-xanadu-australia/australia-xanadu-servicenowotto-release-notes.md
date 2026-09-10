---
title: Combined ServiceNow Otto release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for ServiceNow Otto from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-servicenowotto-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for ServiceNow Otto from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto to Australia

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

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Upgrade information**

Customers who have not opted into third-party, large language models may be routed to them during skill execution. If the new model is not provisioned or available in your environment, this will result in skill execution failures. Check the models your skills use within ServiceNow Otto admin console.

If you customized UI actions or other items that are associated with ServiceNow Otto skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

If you run into issues when you're upgrading a ServiceNow Otto product, see the [Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

The Zurich release introduces enhanced protections for read‑only fields across the ServiceNow® AI Platform. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back-end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. If you have custom client scripts that modify ServiceNow® ‑owned read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122). This article provides additional technical details on how to identify affected fields and adjust their settings.

The existing Access Control Lists \(ACLs\) will be updated to replace the 'admin' role with specific, purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API will be replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the 'admin' role in the code will be substituted with the new feature-specific granular roles for authorization use cases. Read [https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html](https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html) to learn more.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow Otto.

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
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow Otto features.

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
</table>## Removed

Between your current release family and Australia, some ServiceNow Otto features or functionality were removed.

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

Between your current release family and Australia, some ServiceNow Otto features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate ServiceNow Otto.

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

-   **Activation information**
    -   **[Skills](https://www.servicenow.com/docs/access?context=now-assist-skills&family=zurich&ft:locale=en-US)**

Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto we have noted them here.

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

-   **Additional requirements**

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow Otto we have noted them here.

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

-   **Browser requirements**

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Internet Explorer.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ServiceNow Otto, such as specific requirements or compliance levels.

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

-   **Accessibility information**
    -   **[Voice Input in Now Assist](https://www.servicenow.com/docs/access?context=enable-voice-input-for-now-assist-panel&family=zurich&ft:locale=en-US)**

Administrators can enable an optional voice input setting for the Now Assist panel in the AI Admin Hub console. This feature, Voice Input, gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. Voice Input helps users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or users using hand-held devices on the go, such as field service agents.

Once enabled, Voice Input can be changed using the individual user accessibility preferences. See [Configure accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&family=zurich&ft:locale=en-US) for more information.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow Otto we have noted them here.

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

-   **Localization information**

Now Assist supports Dynamic Translation for Zurich.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow Otto we have noted them here.

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

[Zurich Patch 12](https://www.servicenow.com/docs/access?context=zurich-patch-12&family=zurich&ft:locale=en-US)

-   Starting with Zurich Patch 12, Now Assist is now ServiceNow Otto. ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 [Zurich Patch 10](https://www.servicenow.com/docs/access?context=zurich-patch-10&family=zurich&ft:locale=en-US)

-   AI Guardian is enabled by default and detects prompt injection attempts and offensive content without manual activation.
-   Configure prompt injection detection separately for each Now Assist skill.

 [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US)

-   Now Assist panel premium chat gives you a full-featured AI assistant experience with support for file uploads, web search, agentic workflows, and voice input — so you can get answers, take action on records, and complete complex tasks without leaving your current context.
-   Get accurate results without having to repeat yourself or correct a wrong action because Now Assist now recognizes when your request needs clarification and asks a focused follow-up question before acting.
-   Upload documents directly in your Now Assist panel conversation and Now Assist automatically extracts the relevant information to fill in required fields, answer your questions, and keep the conversation moving without switching modes or restarting the flow.
-   Select specific reasons when you give a thumbs up or thumbs down to a Now Assist response, so your feedback is more meaningful and helps improve future responses.

 [Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Explore revamped **Manage AI models** option within AI Admin Hub for managing and configuring model providers, and updating model provider versions.
-   Select a record from the Now Assist context menu inline citation to navigate directly to the record page, where the referenced section will be highlighted for easy identification.
-   View all AI-generated content, now visually highlighted for easier recognition.
-   Set the minimum word count required for the Now Assist icon to appear, allowing you to control when the icon is displayed based on content length.

 [Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   View improved legend and icon descriptions for the Now Assist Readiness Evaluation app.
-   Work with new system properties to improve performance and customization within the Now Assist Readiness Evaluation app.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Select your preferred integration type, either Bring Your Own Key \(BYOK\) or Original Equipment Manufacturer \(OEM\), for the configuration of the available model providers within AI Admin Hub.
-   Explore the Data and Analytics workflow skills under Now Assist skills within AI Admin Hub.
-   Adopt AI responsibly and minimize operational and compliance risks by configuring and subscribing to Long Term Stable Models \(LTS\) as a model provider in AI Admin Hub.
-   Ask a follow-up question in the Now Assist panel for additional information or clarification.
-   Experience an enhanced conversational interaction by viewing synthesized Now Assist responses from within Google Chat.
-   Initiate and view agentic workflows from within Google Chat.
-   Use the Now Assist context menu open prompt feature to create and edit knowledge articles.
-   Use Advanced settings to add conditions to hide or show the Now Assist Context Menu quick actions.
-   Create multiple Now Assist context menu configurations for the same field.
-   Use the Enable for extended tables option in parent table configuration, to enable or disable the inheritance model for the child table configurations.

 [Zurich Patch 2](https://www.servicenow.com/docs/access?context=zurich-patch-2&family=zurich&ft:locale=en-US)

-   Use the Now Assist Readiness Evaluation app to automate the implementation assessment process before implementing Now Assist agentic and generative AI.

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Enable administrators to set up a security Access Control Lists \(ACLs\) that checks user authentication for Now Assist context menu skills and new setup options. This feature gives them control over who can use Now Assist context menu skills and actions, as well as built-in options like shorten, elaborate, and change tone.
-   Use the Open Prompt Capability available in ServiceNow Otto for Strategic Portfolio Management to ask questions and refine generated content through open-ended queries.

 Zurich

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.
-   Select your preferred large language model \(LLM\) provider for Now Assist base system skills. Apart from Now LLM Service, the platform supports Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.5 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow® third-party model strategy.
-   Suppress the modeless window for a custom Now Assist context menu event.
-   View numbered citations and links to the information sources when you use the Now Assist context menu for email reply recommendation.

 See [AI Admin Hub](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&family=zurich&ft:locale=en-US) for more information.

 For more Platform Now Assist feature release notes, see the following topics:

-   [AI Search release notes](https://www.servicenow.com/docs/access?context=ai-search-rn&family=zurich&ft:locale=en-US)
-   [Document Intelligence release notes](https://www.servicenow.com/docs/access?context=document-intelligence-rn&family=zurich&ft:locale=en-US)
-   [AI Skill Kit release notes](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-rn&family=zurich&ft:locale=en-US)
-   [Now Assist in Virtual Agent release notes](https://www.servicenow.com/docs/access?context=now-assist-va-rn&family=zurich&ft:locale=en-US)

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

