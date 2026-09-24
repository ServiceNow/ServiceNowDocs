---
title: Combined Predictive AI for CSM release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Predictive AI for CSM from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-predictiveaiforcsm-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Predictive AI for CSM release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Predictive AI for CSM from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Predictive AI for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Predictive AI for CSM to Brazil

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

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Predictive AI for CSM.

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

-   **[Recommended Actions – AI search on CSM default record page, Front line case page, and CSM interaction record page](https://www.servicenow.com/docs/access?context=ra-csm-ai-search&family=yokohama&ft:locale=en-US)**

The Recommended Actions – AI search is introduced on the [CSM default record page](https://www.servicenow.com/docs/access?context=csm-default-record-page&family=yokohama&ft:locale=en-US), [Front-line case page](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&family=yokohama&ft:locale=en-US), and [CSM Interaction record page](https://www.servicenow.com/docs/access?context=csm-interaction-record-page&family=yokohama&ft:locale=en-US) \(for the chat, video, walk-up, and email type channels\) and it’s enabled by default for new customers. The default guidance is also enabled for these pages. Agents can attach and share knowledge article links in comments, work notes, and emails.

-   **[Recommended Actions - Catalog item source type for AI search](https://www.servicenow.com/docs/access?context=ra-csm-ai-search&family=yokohama&ft:locale=en-US)**

Search and filter the catalog items easily in the AI search tab of Recommended Actions in the CRM Workspace.

-   **[Recommended Actions - Ability to have multiple active contexts for the same table](https://www.servicenow.com/docs/access?context=ra-csm-contexts&family=yokohama&ft:locale=en-US)**

Enables multiple active contexts for the same table, so that tailored recommendations are displayed in the CRM Workspace:

    -   For different user personas based on their requirements.
    -   For different Predictive Intelligence models or AI model variants.
    -   For the same record in different channels, such as chat, email, and so on.
-   **[Recommended Actions - Ability to inherit active rules and their recommendations from a parent table context to extended table context](https://www.servicenow.com/docs/access?context=ra-csm-contexts&family=yokohama&ft:locale=en-US)**

Assign the active rules and their recommendations from the parent table context to the extended context table for a streamlined process.

-   **[Recommended Actions - Asynchronous evaluation for recommendations](https://www.servicenow.com/docs/access?context=ra-csm-contexts&family=yokohama&ft:locale=en-US)**

Enables you to configure loading behavior at the context level by choosing between synchronous and asynchronous modes. In the asynchronous mode, recommendations load in the background without blocking the UI, allowing agents to interact with the record immediately.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Recommended Actions - View the relevancy score of the AI search results](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

View the relevancy score on the search result recommendation cards in the Search tab of the Recommended Actions panel for the default guidance for search results, Attach and share article, Share KB in chat interactions, and all no-code \( Link incident to current case, Link problem to current case, and Link change request to current case\) guidances. To enable this feature, you must enable the Show relevancy score for results check box in the Context form.

-   **[Recommended Actions – Limit the number of search results for more precise output](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Limit the number of search results \(Top N\) that appear in the AI search tab in the Recommended Actions context side panel. To configure top N search results, you must enable the Top N check box in the Context form and then define the Search Results Limit in the Search Application Configuration.

-   **[Recommended Actions - Optimize the Recommended Actions refresh behavior by excluding non-critical field updates](https://www.servicenow.com/docs/access?context=ra-csm-contexts-create&family=zurich&ft:locale=en-US)**

Exclude the non-critical fields from triggering a Recommended Actions refresh on the record pages by adding the non-critical fields to the **Exclude fields** field on a context record. In a child context, you can also include the field exclusions of the parent context. You can enhance a user’s UI experience when you prevent excessive UI updates and still ensure that relevant updates trigger as intended.

-   **[Recommended Actions - Trigger Refresh for Recommendations explicitly or based on UI events](https://www.servicenow.com/docs/access?context=ra-csm-config-data-broker&family=zurich&ft:locale=en-US)**

Trigger recommendations refresh in the Recommended Actions tab on the contextual side panel when a UI or back-end event update is made. This provides dynamic and more contextually relevant recommendations based on the outcome of UI and back-end events. To trigger a recommendations refresh:

    -   configure UI component’s Data Broker in the UI builder for UI events
    -   execute the ForceRefreshRecommendationsscript include for back-end events
-   **[Recommended Actions - Configure dynamic JSON-based context inputs](https://www.servicenow.com/docs/access?context=ra-csm-create-context-inputs&family=zurich&ft:locale=en-US)**

Configure JSON-based context inputs in a context to populate accurate recommendations corresponding to dynamically changing contexts. You can conﬁgure parameters associated with the context table along with context table parameters. To support scenarios where a single workflow may leverage multiple active contexts simultaneously to generate recommendations. This uses the context inputs in rule condition builders, resource generators, and recommendation-action mappings, with minimal performance impact and backward compatibility.

-   **[Recommended Actions - Enhanced KB article sharing for Agents](https://www.servicenow.com/docs/access?context=ra-csm-guidances-attach-share-article&family=zurich&ft:locale=en-US)**

Identify the Knowledge Base \(KB\) articles that are not accessible to the case requester with the help of a Lock icon. In the recommendations on the contextual side panel of the CRM Workspace, a Lock icon on a recommendation card denotes that the recommended KB article cannot be accessed by the case requester.

-   **[Process Mining - SLA breach analysis](https://www.servicenow.com/docs/access?context=csm-integration-po&family=zurich&ft:locale=en-US)**

Identify and analyze cases where service level agreements \(SLAs\) have been violated. The SLA breach analysis project provides insights into the root causes of breaches, highlights bottlenecks, and recommends improvements to optimize the performance of your processes.

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&family=zurich&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Australia

</td><td>

-   **[Recommended Actions - Support for the Now Assist Multi-Content Response \(MCR\) genius model](https://www.servicenow.com/docs/access?context=ra-configuring-ai-search&family=australia&ft:locale=en-US)**

Recommended Actions now supports the Now Assist Multi-Content Response \(MCR\) genius model. When an author configures a recommendation backed by the MCR model, the agent sees a single MCR recommendation card in the Suggested Actions tab. The card appears in the Recommended Actions Contextual Side Panel in the agent workspace. The MCR recommendation card displays all its content blocks and citations grouped together under that one card.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Predictive AI for CSM features.

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

-   **[Recommended Actions - The primary call-to-action changes on the KB article recommendation card](https://www.servicenow.com/docs/access?context=ra-csm-contexts&family=zurich&ft:locale=en-US)**

The primary call-to-action \(CTA\) on a recommended knowledge base article is determined by the source channel of the case. If the case originates from an email, the primary CTA displayed is Attach and share link in the email. For all the other channels, the primary CTA is Attach and add link in comments. If the article isn’t accessible to the requester, the primary CTA is set to Read article. Accessible articles display the full set of actions \(Attach and add link in comments, Add link in work note, and so on\). Inaccessible articles are limited to internal-use actions only \(Read article, Share link in work notes, and so on\).

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


</td></tr><tr><td>

Australia

</td><td>

-   **[Now Assist &gt; ServiceNow Otto announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**

ServiceNow Otto® introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Predictive AI for CSM features or functionality were removed.

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

Between your current release family and Brazil, some Predictive AI for CSM features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Predictive AI for CSM.

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

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=australia&ft:locale=en-US).

Now Assist features are available with activation of the ServiceNow Otto for CSM plugin. For more information, see [Install plugins for ServiceNow Otto](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&family=australia&ft:locale=en-US).

Starting with Vancouver Patch 4, ServiceNow Otto for CSM is supported.

Starting with Zurich Patch 7, Customer Service Management AI agent collection is supported. Check your entitlements to determine whether you have access to the ServiceNow Otto for CSM


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Predictive AI for CSM we have noted them here.

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
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Predictive AI for CSM we have noted them here.

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

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Predictive AI for CSM, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Predictive AI for CSM we have noted them here.

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
</table>## Highlight information

If there are specific highlight considerations for Predictive AI for CSM we have noted them here.

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

-   Starting with Zurich Patch 12, ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Customer Service Management \(CSM\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Resolve cases faster with a new case insights section that consolidates key case details, customer history, sentiment scores, and special handling notes into a single view.
-   Use AI to proactively detect emerging issues from case patterns and automatically propose major cases when similar cases trend together.
-   View automated sentiment scores and trends from conversations directly on the email interaction page.
-   Enable customers to make case updates through AI voice agent.
-   Use Live Agent Assist for voice calls to generate recommendations during live voice calls.

 [Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US)

-   Automatically evaluate post-interaction customer conversations using AI models that score against a configurable quality rubric, eliminating manual effort.
-   Receive intelligent email reply recommendations on extended table record pages in ServiceNow Otto for CSM, helping agents respond faster with less manual effort.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Availability of filter controls in Now Assist Guardian for ServiceNow Otto for CSM.
-   Availability of AI Workflow tab in Core UI.

 -   Use AI to populate interaction wrap-up codes and notes, saving agents time.
-   Simplify metadata management by granting developer roles and privileges to your granular admin users.

 See [Intelligence for CSM](https://www.servicenow.com/docs/access?context=intelligence-csm&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

