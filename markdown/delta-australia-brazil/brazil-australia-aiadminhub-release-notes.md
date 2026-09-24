---
title: Combined AI Admin Hub release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for AI Admin Hub from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-aiadminhub-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined AI Admin Hub release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for AI Admin Hub from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Admin Hub release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Admin Hub to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Upgrade information**

If you customized actions on the user interface or other items that are associated with ServiceNow Otto skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

If you run into issues when you're upgrading a ServiceNow Otto product, see the [Issues and mitigation for Now Assist \(generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new read\_only\_option field with granular control levels, including strict\_read\_only and client\_script\_modifiable. The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen instance security while preserving flexibility. If you have custom client scripts that modify read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to the [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) article in the Now Support Knowledge Base to identify affected fields and adjust the settings.

The existing access control lists \(ACLs\) have been updated to replace the admin role with purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API is replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the admin role in the code have been substituted with the granular roles for authorization use cases. For more information, see [Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for AI Admin Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Manage version](https://www.servicenow.com/docs/access?context=manage-version&family=australia&ft:locale=en-US)**

Experiment with new models for custom skills as a part of model preview program within AI Admin Hub. The program aims to provide an opportunity for the user to explore and experiment with the new models even before they are generally available.

-   **[ServiceNow Otto panel premium chat](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=australia&ft:locale=en-US)**

Switch between records in ServiceNow Otto panel workspaces without disrupting your workflow or losing conversation context.


 -   **[Using the approval assistance AI agent](https://www.servicenow.com/docs/access?context=platform-approval-aia&family=australia&ft:locale=en-US)**

ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Platform Approval Assistance AI agent. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   **[Using the request status AI agent](https://www.servicenow.com/docs/access?context=ticket-status-aia&family=australia&ft:locale=en-US)**

ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Platform Request status AI agent. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   **[ServiceNow Otto panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=australia&ft:locale=en-US)**

Enable streaming responses and unified surface operations to deliver faster, more reliable ServiceNow Otto® interactions. Support both synchronous and asynchronous workflows while maintaining compatibility with various LLM providers.

-   **[AI skill details](https://www.servicenow.com/docs/access?context=now-assist-skill-details&family=australia&ft:locale=en-US)**

Map multiple skills under subsections and display all applicable products per common skill with distinct visual tags. A visual indicator will mark skills as common, based on schema data.

-   **[Install plugins for ServiceNow Otto](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&family=australia&ft:locale=en-US)**

Control default activation of skills configured for auto-activating when installed or updated. Review the skills active by default and, activate or deactivate them individually.

-   **[Usage alerts](https://www.servicenow.com/docs/access?context=usage-alerts&family=australia&ft:locale=en-US)**

Establish limit-based alert rules at the skill level to oversee assist consumption and skill execution counts. This solution seeks to prevent resource exhaustion, and offer clear insights via an alerts feed and rule management interface.


 -   **[Prompt library](https://www.servicenow.com/docs/access?context=now-assist-prompt-library&family=australia&ft:locale=en-US)**

Browse and select from promoted prompt templates or save your own custom prompts, eliminating the need to retype frequently-used prompts within your chats. Access your reusable templates instantly from the omnibar for faster, more consistent conversations.

-   **[Archive an AI skill](https://www.servicenow.com/docs/access?context=archive-a-now-assist-skill&family=australia&ft:locale=en-US)**

Find the Deprecated skills option in the navigation pane within AI Admin Hub to view skills deprecated by business unit, unavailable for use and no longer supported by ServiceNow.


 -   **[Create knowledge articles using AI and Box](https://www.servicenow.com/docs/access?context=kc-create-article-with-Box&family=australia&ft:locale=en-US)**

The Knowledge Center now integrates with Box. This integration enables authors to use stored files as a source for generating knowledge articles with Now Assist.

-   **[Now Assist Guardian enabled by default](https://www.servicenow.com/docs/access?context=now-assist-guardian&family=australia&ft:locale=en-US)**

Detect and log prompt injection attempts across all generative AI applications and features, and offensive content in supported Now Assist skills, by default. You can configure AI Guardian to block AI-generated responses when an attempt is detected.

-   **[Using AI Admin Hub](https://www.servicenow.com/docs/access?context=using-now-assist-admin_0&family=australia&ft:locale=en-US)**

Explore additional user interface tabs of a Now Assist skill within a selected workflow. Access the usage and analytics of that skill. You can also view and manage the security and governance details of the selected skills.

-   **[Create knowledge articles using AI and Box](https://www.servicenow.com/docs/access?context=kc-create-article-with-Box&family=australia&ft:locale=en-US)**

Knowledge Center integrates with **Box**, enabling authors to use stored files as a source for generating knowledge articles with Now Assist.

-   **[Article Optimization with Reading Ease scan](https://www.servicenow.com/docs/access?context=kc-reading-ease-scan&family=australia&ft:locale=en-US)**

The AI-based **Reading Ease** scan, integrated into the article optimization feature of Knowledge Center, scans articles for readability, provides actionable recommendations, and supports ongoing article improvement.

-   **[Configure prompt injection detection for Now Assist skills](https://www.servicenow.com/docs/access?context=configure-prompt-injection-attack-protection&family=australia&ft:locale=en-US)**

Set the prompt injection detection action and severity level for Now Assist skills. Prompt injection detection is enabled by default for all Now Assist skills, except Platform skills and custom skills. When a skill has its own setting, AI Guardian automatically applies the more protective of the two settings, the skill-level setting or the instance-level setting.

-   **[Visual Q&amp;A in Now Assist](https://www.servicenow.com/docs/access?context=now-assist-qa-genius-result&family=australia&ft:locale=en-US)**

Upload screenshots, error images, or documents in the Now Assist panel and get AI-generated answers about content without leaving your current context.

-   **[Catalog experience](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=australia&ft:locale=en-US)**

Navigate away from a catalog form mid-completion and a modal appears asking whether you want to stay or leave, preventing accidental loss of your work. After you submit a catalog item, you can select View Details to open the submitted record.

-   **[Enhancements](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=australia&ft:locale=en-US)**

Switch between multiple interactive views — such as knowledge articles, catalogs, and org charts — within a single conversation using a new dropdown in the Now Assist panel. When more than six promoted topics are available, you can select a category on the topic menu to see all of them at once.

-   **[Image and document upload](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=australia&ft:locale=en-US)**

Upload images and screenshots directly into the Now Assist panel as part of your conversation and the Now Assist interprets the visual content to answer your questions or generate summaries.

-   **[Maintain and display the right context](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=australia&ft:locale=en-US)**

Open the Now Assist panel while working on an incident record and you automatically see the most recent conversation tied to that incident. You can continue chatting about the incident or switch to unrelated topics in the same session, keeping your work in context without losing your place.

-   **[Post-chat surveys](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=australia&ft:locale=en-US)**

Collect user feedback in premium chats through post-chat surveys that trigger on agent task completion instead of waiting for a chat-end event. When an agent completes a task in an agentic flow, the survey can surface based on a configured probability, enabling you to gather insights that were previously unavailable.


 -   **[Using AI Admin Hub](https://www.servicenow.com/docs/access?context=using-now-assist-admin_0&family=australia&ft:locale=en-US)**

Explore the archive option from navigation pane within AI Admin Hub and archive custom and copies of Now Assist skills.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available:

    -   Foundation: AI agents and skills to deliver insights
    -   Advanced: AI agents and skills to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI agents and skills, and create your own
-   **[Merge duplicate articles](https://www.servicenow.com/docs/access?context=merge-duplicate-articles&family=australia&ft:locale=en-US)**

Use Now Assist in Knowledge Management to merge selected duplicate knowledge articles into a single consolidated article, preserving references to the original sources and maintaining a high‑quality, well‑organized knowledge base.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Manage version](https://www.servicenow.com/docs/access?context=manage-version&family=brazil&ft:locale=en-US)**

Experiment with new models for custom skills as a part of model preview program within AI Admin Hub. The program aims to provide an opportunity for the user to explore and experiment with the new models even before they are generally available.

-   **[ServiceNow Otto panel premium chat](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=brazil&ft:locale=en-US)**

Switch between records in ServiceNow Otto panel workspaces without disrupting your workflow or losing conversation context.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing AI Admin Hub features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Default model provider updated to third-party LLM](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


 -   **[Conversational Help](https://www.servicenow.com/docs/access?context=conversational-help-skills&family=australia&ft:locale=en-US)**

The discovery of Conversational Help Skills from the Now Assist panel is no longer configured as auto-enabled.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some AI Admin Hub features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some AI Admin Hub features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Starting with the [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US) release, Conversational Help Skills is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate AI Admin Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**
    -   **[Skills](https://www.servicenow.com/docs/access?context=now-assist-skills&family=australia&ft:locale=en-US)**

Now Assist features are available with activation of any Now Assist plugin from [https://www.servicenow.com/docs/access?context=external.sn-app-store&amp;family=australia&amp;ft:locale=en-US](https://www.servicenow.com/docs/access?context=external.sn-app-store&family=australia&ft:locale=en-US).


**Important:** Now Assist is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

AI Admin Hub is available from the ServiceNow® Store.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for AI Admin Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Additional requirements**

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for AI Admin Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Browser requirements**

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Internet Explorer.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for AI Admin Hub, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for AI Admin Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Localization information**

Now Assist supports Dynamic Translation for Australia.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for AI Admin Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   AI Admin Hub is the new AI experience brand. This change is reflected in the name of ServiceNow products. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   AI Guardian is enabled by default and detects prompt injection attempts and offensive content without manual activation.
-   Configure prompt injection detection separately for each Now Assist skill.
-   Create knowledge articles from Now Assist using files stored in Box.
-   Improve the clarity and accessibility of your articles with the AI-powered prompt Reading Ease scan.

 -   **[Merge duplicate articles](https://www.servicenow.com/docs/access?context=merge-duplicate-articles&family=australia&ft:locale=en-US)**

Merge selected duplicate knowledge articles into a new consolidated article using Now Assist in Knowledge Management. The merge preserves references to source articles and helps maintain a clean, high‑quality knowledge base.


</td></tr><tr><td>

Brazil

</td><td>

Get started right away with guided quick-start use cases that appear as actionable cards on the home page. This gives both new and experienced administrators a clear starting point for enabling AI.

 See [AI Admin Hub](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

