---
title: Combined AI Admin Hub release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for AI Admin Hub from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-aiadminhub-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined AI Admin Hub release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for AI Admin Hub from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family AI Admin Hub release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading AI Admin Hub to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[AI Guardian analytics](https://www.servicenow.com/docs/access?context=now-assist-guardian-analytics&family=yokohama&ft:locale=en-US)**

Monitor the performance of offensive content and prompt injections guardrails with the help of the AI Guardian analytics dashboard.

-   **[Configuring Now Assist settings and features](https://www.servicenow.com/docs/access?context=configuring-na-landing&family=yokohama&ft:locale=en-US)**

For custom skills, explore an additional display option in the form of **Conversational experiences**. You can select Now Assist Virtual Agent to assist you with the display.Create and activate a Now Assist skill copy, and have both the original skill and its copy to remain active simultaneously.


 -   **[Now Assist Context Menu usage dashboard](https://www.servicenow.com/docs/access?context=now-assist-context-menu-dashboard&family=yokohama&ft:locale=en-US)**

View and monitor the use of the Now Assist context menu across the different applications. Gain insights into the usage patterns, frequency, and effectiveness of the context menu actions with the Now Assist context menu usage dashboard.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Requester Approval Checklist](https://www.servicenow.com/docs/access?context=service-portal-approval-checklist-skill&family=zurich&ft:locale=en-US)**

The Requester Approval Checklist skill in the ServiceNow AI Platform® generates a structured checklist by mapping real-time request data against your organization’s knowledge articles.

**Note:** The skill is on by default.


</td></tr><tr><td>

Australia

</td><td>

-   **[Manage version](https://www.servicenow.com/docs/access?context=manage-version&family=australia&ft:locale=en-US)**

Experiment with new models for custom skills as a part of model preview program within AI Admin Hub. The program aims to provide an opportunity for the user to explore and experiment with the new models even before they are generally available.

-   **[ServiceNow Otto panel premium chat](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=australia&ft:locale=en-US)**

Switch between records in ServiceNow Otto panel workspaces without disrupting your workflow or losing conversation context.


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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Now Assist data sharing opt-out moved to Data sharing and processing tab.](https://www.servicenow.com/docs/access?context=opt-out-of-data-sharing-for-now-assist&family=yokohama&ft:locale=en-US)**

The opt-out button in the data sharing card from the AI Admin Hub Account page has moved to the Settings page on the **Data sharing and processing** tab.

-   **[Now Assist context menu](https://www.servicenow.com/docs/access?context=now-assist-write-overview&family=yokohama&ft:locale=en-US)**

You can now open the Now Assist context menu by selecting the Now Assist context menu icon \(\[Omitted image "image.wwna-icon"\] Alt text: Now Assist Context menu icon.\) for effortless access.The Now Assist context menu enables users to automatically select a sentence, paragraph, or the entire content even if they initially make a partial selection. Administrators can configure the selection to be a sentence, paragraph, or the entire content.The dynamic header label next to the Now Assist context menu icon can be customized to display the query status.The new Now Assist context menu icon \(\[Omitted image "image.wwna-icon"\] Alt text: Context menu icon .\) was updated with an enhanced animation.


 -   **[Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&family=yokohama&ft:locale=en-US)**

Enable translation settings is now Multilingual service in Now Assist admin console.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Manage model providers](https://www.servicenow.com/docs/access?context=edit-model-providers&family=zurich&ft:locale=en-US)**

Explore the **Manage integrations** option within **Manage model providers** tab now.


 -   **[Manage version](https://www.servicenow.com/docs/access?context=manage-version&family=zurich&ft:locale=en-US)**

Update the model provider version at the instance or the skill level form **Manage model versions** within **Manage AI models** option under Now Assist **Settings** tab.


 -   **[Updates made to labels.](https://www.servicenow.com/docs/access?context=agentic-ai-assessment-dashboard&family=zurich&ft:locale=en-US)**

On the Agentic AI- Assessments tab,**Issues** are now renamed **findings**.


 -   **[Updated the name of status buttons.](https://www.servicenow.com/docs/access?context=assessing-go-no-go&family=zurich&ft:locale=en-US)**

**Go** button on Now Assist Assessment Home page is now renamed to **Ready**.


 -   **[Updates made to legend labels.](https://www.servicenow.com/docs/access?context=reviewing-now-assist-assessment&family=zurich&ft:locale=en-US)**

The **No Blockers** label is now renamed **Informational**. The **Blockers found** label is now renamed **Required**. The **Review for blockers** label is now renamed **Recommended**.


</td></tr><tr><td>

Australia

</td><td>

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

-   In Patch 5, the **Select Use Case** drop-down menu was removed from the Agentic AI - ITSM tab.

</td></tr><tr><td>

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

-   **Activation information**
    -   **[Skills](https://www.servicenow.com/docs/access?context=now-assist-skills&family=australia&ft:locale=en-US)**

Now Assist features are available with activation of any Now Assist plugin from [https://www.servicenow.com/docs/access?context=external.sn-app-store&amp;family=australia&amp;ft:locale=en-US](https://www.servicenow.com/docs/access?context=external.sn-app-store&family=australia&ft:locale=en-US).


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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

