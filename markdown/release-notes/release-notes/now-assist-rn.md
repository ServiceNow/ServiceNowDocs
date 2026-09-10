---
title: AI Admin Hub release notes
description: The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 10
---

# AI Admin Hub release notes

The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.

## About AI Admin Hub

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)

-   AI Admin Hub is the new AI experience brand. This change is reflected in the name of ServiceNow products. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   AI Guardian is enabled by default and detects prompt injection attempts and offensive content without manual activation.
-   Configure prompt injection detection separately for each Now Assist skill.
-   Create knowledge articles from Now Assist using files stored in Box.
-   Improve the clarity and accessibility of your articles with the AI-powered prompt Reading Ease scan.

-   **[Merge duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/merge-duplicate-articles.md)**

    Merge selected duplicate knowledge articles into a new consolidated article using Now Assist in Knowledge Management. The merge preserves references to source articles and helps maintain a clean, high‑quality knowledge base.


## Activation and other requirements

**Important:** Now Assist is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**
    -   **[Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills.md)**

        Now Assist features are available with activation of any Now Assist plugin from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

-   **Upgrade information**

    If you customized actions on the user interface or other items that are associated with ServiceNow Otto skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

    If you run into issues when you're upgrading a ServiceNow Otto product, see the [Issues and mitigation for Now Assist \(generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

    The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new read\_only\_option field with granular control levels, including strict\_read\_only and client\_script\_modifiable. The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen instance security while preserving flexibility. If you have custom client scripts that modify read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to the [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) article in the Now Support Knowledge Base to identify affected fields and adjust the settings.

    The existing access control lists \(ACLs\) have been updated to replace the admin role with purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API is replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the admin role in the code have been substituted with the granular roles for authorization use cases. For more information, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md).

-   **Browser requirements**

    Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Internet Explorer.

-   **Additional requirements**

    The Next Experience UI Framework must be enabled before you can use the Now Assist panel.


## Accessibility and localization

-   **Localization information**

    Now Assist supports Dynamic Translation for Australia.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn-landing.md)

## September 2026

The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.

### What's new

-   **[Manage version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-version.md)**

    Experiment with new models for custom skills as a part of model preview program within AI Admin Hub. The program aims to provide an opportunity for the user to explore and experiment with the new models even before they are generally available.

-   **[ServiceNow Otto panel premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Switch between records in ServiceNow Otto panel workspaces without disrupting your workflow or losing conversation context.


## August 2026

The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.

### What's new

-   **[Using the approval assistance AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/plat-approval-assistance-ai-agent.md)**

    ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Platform Approval Assistance AI agent. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   **[Using the request status AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/plat-request-status-agent-ai-agent.md)**

    ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Platform Request status AI agent. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   **[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Enable streaming responses and unified surface operations to deliver faster, more reliable ServiceNow Otto® interactions. Support both synchronous and asynchronous workflows while maintaining compatibility with various LLM providers.

-   **[AI skill details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-details.md)**

    Map multiple skills under subsections and display all applicable products per common skill with distinct visual tags. A visual indicator will mark skills as common, based on schema data.

-   **[Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md)**

    Control default activation of skills configured for auto-activating when installed or updated. Review the skills active by default and, activate or deactivate them individually.

-   **[Usage alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/usage-alerts.md)**

    Establish limit-based alert rules at the skill level to oversee assist consumption and skill execution counts. This solution seeks to prevent resource exhaustion, and offer clear insights via an alerts feed and rule management interface.


## July 2026

The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.

### What's new

-   **[Prompt library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-prompt-library.md)**

    Browse and select from promoted prompt templates or save your own custom prompts, eliminating the need to retype frequently-used prompts within your chats. Access your reusable templates instantly from the omnibar for faster, more consistent conversations.

-   **[Archive an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/archive-a-now-assist-skill.md)**

    Find the Deprecated skills option in the navigation pane within AI Admin Hub to view skills deprecated by business unit, unavailable for use and no longer supported by ServiceNow.


### What's changed

-   **[Default model provider updated to third-party LLM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


## June 2026

The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.

### What's new

-   **[Create knowledge articles using AI and Box](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-create-article-with-Box.md)**

    The Knowledge Center now integrates with Box. This integration enables authors to use stored files as a source for generating knowledge articles with Now Assist.

-   **[Now Assist Guardian enabled by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-guardian.md)**

    Detect and log prompt injection attempts across all generative AI applications and features, and offensive content in supported Now Assist skills, by default. You can configure AI Guardian to block AI-generated responses when an attempt is detected.

-   **[Using AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/using-now-assist-admin_0.md)**

    Explore additional user interface tabs of a Now Assist skill within a selected workflow. Access the usage and analytics of that skill. You can also view and manage the security and governance details of the selected skills.

-   **[Create knowledge articles using AI and Box](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-create-article-with-Box.md)**

    Knowledge Center integrates with **Box**, enabling authors to use stored files as a source for generating knowledge articles with Now Assist.

-   **[Article Optimization with Reading Ease scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-reading-ease-scan.md)**

    The AI-based **Reading Ease** scan, integrated into the article optimization feature of Knowledge Center, scans articles for readability, provides actionable recommendations, and supports ongoing article improvement.

-   **[Configure prompt injection detection for Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/configure-prompt-injection-attack-protection.md)**

    Set the prompt injection detection action and severity level for Now Assist skills. Prompt injection detection is enabled by default for all Now Assist skills, except Platform skills and custom skills. When a skill has its own setting, AI Guardian automatically applies the more protective of the two settings, the skill-level setting or the instance-level setting.

-   **[Visual Q&amp;A in Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-qa-genius-result.md)**

    Upload screenshots, error images, or documents in the Now Assist panel and get AI-generated answers about content without leaving your current context.

-   **[Catalog experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Navigate away from a catalog form mid-completion and a modal appears asking whether you want to stay or leave, preventing accidental loss of your work. After you submit a catalog item, you can select View Details to open the submitted record.

-   **[Enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Switch between multiple interactive views — such as knowledge articles, catalogs, and org charts — within a single conversation using a new dropdown in the Now Assist panel. When more than six promoted topics are available, you can select a category on the topic menu to see all of them at once.

-   **[Image and document upload](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Upload images and screenshots directly into the Now Assist panel as part of your conversation and the Now Assist interprets the visual content to answer your questions or generate summaries.

-   **[Maintain and display the right context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Open the Now Assist panel while working on an incident record and you automatically see the most recent conversation tied to that incident. You can continue chatting about the incident or switch to unrelated topics in the same session, keeping your work in context without losing your place.

-   **[Post-chat surveys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Collect user feedback in premium chats through post-chat surveys that trigger on agent task completion instead of waiting for a chat-end event. When an agent completes a task in an agentic flow, the survey can surface based on a configured probability, enabling you to gather insights that were previously unavailable.


## Australia General Availability

The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.

### What's new

-   **[Using AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/using-now-assist-admin_0.md)**

    Explore the archive option from navigation pane within AI Admin Hub and archive custom and copies of Now Assist skills.


## April 2026

The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.

### What's deprecated or removed

-   Starting with the [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md) release, Conversational Help Skills is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Australia Early Availability

The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.

### What's changed

-   **[Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/conversational-help-skills.md)**

    The discovery of Conversational Help Skills from the Now Assist panel is no longer configured as auto-enabled.


## Australia

The ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Australia release.

### What's new

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available:

    -   Foundation: AI agents and skills to deliver insights
    -   Advanced: AI agents and skills to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI agents and skills, and create your own
-   **[Merge duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/merge-duplicate-articles.md)**

    Use Now Assist in Knowledge Management to merge selected duplicate knowledge articles into a single consolidated article, preserving references to the original sources and maintaining a high‑quality, well‑organized knowledge base.


### Plugin information

-   **Plugins planned for deprecation**

    The following plugin is planned for deprecation in a future release:

    Conversational Help Skills: Planned for deprecation in May 2026. Install the External Content Connectors Application Suite from the [ServiceNow store](https://store.servicenow.com/store/app/dd69bc781bd9a650396216db234bcb0b). For configuration guidance, see [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ext-cont-connectors-landing-page.md).


