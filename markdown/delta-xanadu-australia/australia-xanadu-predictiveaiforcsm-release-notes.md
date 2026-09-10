---
title: Combined Predictive AI for CSM release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Predictive AI for CSM from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-predictiveaiforcsm-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Predictive AI for CSM release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Predictive AI for CSM from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Predictive AI for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Predictive AI for CSM to Australia

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

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Predictive AI for CSM.

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

-   **[Recommended Actions - Front-line case page integration with knowledge guidance](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&family=yokohama&ft:locale=en-US)**

Enable agents to attach and share knowledge article links in comments, work notes, or emails by using modeless dialogs.

-   **[Recommended Actions - Default guidance for search results](https://www.servicenow.com/docs/access?context=ra-csm-guidances-default-guidance-search&family=yokohama&ft:locale=en-US)**

Enable agents to view search results for any records. Use a default guidance for any search sources that don't have a dedicated, mapped guidance.

-   **[Recommended Actions - Improved timeout handling for resource generators](https://www.servicenow.com/docs/access?context=ra-csm-resource-generators&family=yokohama&ft:locale=en-US)**

Handle timeout errors when calling Machine Learning \(ML\) resource generators. The system uses a subflow API with a 1-second timeout ensures the RA generation engine prioritizes faster response times by terminating stalled ML prediction calls.

-   **[Recommended Actions - Custom guidances](https://www.servicenow.com/docs/access?context=ra-csm-custom-guidances&family=yokohama&ft:locale=en-US)**

Use a custom guidance to provide actions that are based on the search results from the Case, Problem, Incident, or Change Request tables. Agents can use these actions to link records to the current case and copy resolution codes and notes from resolved cases.

-   **[Recommended Actions - Field values for predicted records](https://www.servicenow.com/docs/access?context=ra-csm-guidances&family=yokohama&ft:locale=en-US)**

Leverage the actual field value for a predicted record and show it in a custom guidance in place of the display value.

-   **[Recommended Actions for Customer Service - Display Recommended Actions on the CSM Interaction record page](https://www.servicenow.com/docs/access?context=ra-csm-chat-interaction-record&family=yokohama&ft:locale=en-US)**

Enable agents to view Recommended Actions in the contextual side panel on the CSM Interaction record page. The search tab dynamically displays relevant actions based on the context of the chat interaction.

-   **[Recommended Actions for Customer Service - Interaction Context record](https://www.servicenow.com/docs/access?context=ra-csm-context-records&family=yokohama&ft:locale=en-US)**

Use the Interaction Context record to display the search results from the Knowledge table. The results are based on the interaction's short description. This context record includes a search-mapping record that maps knowledge results to the Share KB in chat interactions guidance.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Guided Decisions - Enable Guided Decisions as a Playbook Activity with Inputs and Outputs](https://www.servicenow.com/docs/access?context=add-gd-input-output-playbook&family=zurich&ft:locale=en-US)**

Added support for the Guided Decision with Inputs and Outputs activity in Playbook. Use this activity to embed decision trees that accept inputs and generate outputs, guiding users through complex decisions within your playbooks.


</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Now Assist for CSM-AI workflow tab added in Core UI](https://www.servicenow.com/docs/access?context=ai-workflow-pattern-in-customer-service-management&family=australia&ft:locale=en-US)**

Availability of AI Workflow tab within case view of case table records and email interaction view of interaction records in Core UI, showing agentic workflows and actionable AI-driven insights directly in the record UI.

-   **[Now Assist for CSM-Filter controls in Now Assist Guardian](https://www.servicenow.com/docs/access?context=now-assist-guardian-csm-filters&family=australia&ft:locale=en-US)**

Availability of filter controls for CSM in the AI Guardian interface, allowing users to toggle the base system filters on and off. Filtered results display in a user-friendly format for quick case review and action.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Predictive AI for CSM features.

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

-   **[Knowledge generation](https://www.servicenow.com/docs/access?context=configure-knowledge-generation-in-now-assist_0&family=australia&ft:locale=en-US)**

Enable users with the **sn\_skill\_builder.admin** role to generate knowledge base articles in ServiceNow Otto for CSM by selecting the required input fields from a task record, reducing manual effort and streamlining the knowledge base generation process.

-   **[Sidebar summarization](https://www.servicenow.com/docs/access?context=configure-sidebar-summarization-in-now-assist&family=australia&ft:locale=en-US)**

Enable customer agents to generate summaries built from the required case and task tables in ServiceNow Otto for CSM as default tables can now be pre-selected and locked.

-   **[Provide Customer 360 insights agentic workflow](https://www.servicenow.com/docs/access?context=customer-service-management-ai-agent-collection-customer-360&family=australia&ft:locale=en-US)**

Enhanced Provide Customer 360 Insights with Enterprise Graph and AI agent deep research for richer, more contextual query results.

-   **[Triage cases agentic workflow](https://www.servicenow.com/docs/access?context=case-resolving-use-case&family=australia&ft:locale=en-US)**

Multilingual and localization flows in the Triage Cases workflow are now fully supported.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Predictive AI for CSM features or functionality were removed.

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

Between your current release family and Australia, some Predictive AI for CSM features or functionality were deprecated.

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

