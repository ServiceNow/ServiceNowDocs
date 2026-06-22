---
title: Combined Intelligence for CSM release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Intelligence for CSM from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-intelligenceforcsm-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Intelligence for CSM release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Intelligence for CSM from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Intelligence for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Intelligence for CSM to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Between your current release family and Australia, new features were introduced for Intelligence for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

-   **[Recommended Actions - Question font size customization for a Decision tree](https://www.servicenow.com/docs/access?context=configure-decision-trees-gdb&family=yokohama&ft:locale=en-US)**

Enables you to customize the font size of questions in a Decision tree for a better look and feel. This font size is applied to the questions in the decision trees of playbooks, and recommendations, within the CSM Configurable Workspace and service portal.

-   **[Recommended Actions - Control the visibility of completed guidance information](https://www.servicenow.com/docs/access?context=create-guidances&family=yokohama&ft:locale=en-US)**

Allows you to manage the visibility of the completed guidance history information of a decision tree in playbooks, and recommendations for an agent, within the CSM Configurable Workspace, and service portal for a streamlined experience.

-   **[Recommended Actions – AI search on CSM default record page, Front line case page, and CSM interaction record page](https://www.servicenow.com/docs/access?context=ra-csm-ai-search&family=yokohama&ft:locale=en-US)**

The Recommended Actions – AI search is introduced on the [CSM default record page](https://www.servicenow.com/docs/access?context=csm-default-record-page&family=yokohama&ft:locale=en-US), [Front-line case page](https://www.servicenow.com/docs/access?context=csm-front-line-case-page&family=yokohama&ft:locale=en-US), and [CSM Interaction record page](https://www.servicenow.com/docs/access?context=csm-interaction-record-page&family=yokohama&ft:locale=en-US) \(for the chat, video, walk-up, and email type channels\) and it’s enabled by default for new customers. The default guidance is also enabled for these pages. Agents can attach and share knowledge article links in comments, work notes, and emails.

-   **[Recommended Actions - Catalog item source type for AI search](https://www.servicenow.com/docs/access?context=ra-csm-ai-search&family=yokohama&ft:locale=en-US)**

Search and filter the catalog items easily in the AI search tab of Recommended Actions in the CSM Configurable Workspace.

-   **[Recommended Actions - Ability to have multiple active contexts for the same table](https://www.servicenow.com/docs/access?context=ra-csm-contexts&family=yokohama&ft:locale=en-US)**

Enables multiple active contexts for the same table, so that tailored recommendations are displayed in the CSM Configurable Workspace:

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

-   **[Guided Decisions - Enable Guided Decisions as a Playbook Activity with Inputs and Outputs](https://www.servicenow.com/docs/access?context=add-gd-input-output-playbook&family=zurich&ft:locale=en-US)**

Added support for the Guided Decision with Inputs and Outputs activity in Playbook. Use this activity to embed decision trees that accept inputs and generate outputs, guiding users through complex decisions within your playbooks.

-   **[Recommended Actions - View the relevancy score of the AI search results](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

View the relevancy score on the search result recommendation cards in the Search tab of the Recommended Actions panel for the default guidance for search results, Attach and share article, Share KB in chat interactions, and all no-code \( Link incident to current case, Link problem to current case, and Link change request to current case\) guidances. To enable this feature, you must enable the Show relevancy score for results check box in the Context form.

-   **[Recommended Actions – Limit the number of search results for more precise output](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Limit the number of search results \(Top N\) that appear in the AI search tab in the Recommended Actions context side panel. To configure top N search results, you must enable the Top N check box in the Context form and then define the Search Results Limit in the Search Application Configuration.

-   **[Recommended Actions - Filter search results across multiple sources in the Contextual side panel](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Filter search results corresponding to multiple sources in the AI search tab of the Recommended Actions contextual side panel. You can also filter the search results at the facet-level.

-   **[Recommended Actions – Track the AI search usage trends with the AI search analytics dashboard](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Track and analyze the AI search usage in Recommended Actions using the AI search analytics dashboard. The AI search events and actions performed by the agent are captured in the Search Events, Search Source Events, Search Signal Events, Search Result Event, and Search Result Event Action tables. This data is used in the AI search analytics dashboard.

-   **[Recommended Actions - Read-only access to TI solutions for the Resource Generator author role](https://www.servicenow.com/docs/access?context=ra-csm-installed-components&family=zurich&ft:locale=en-US)**

Access Task Intelligence \(TI\) solution definitions in read-only mode as a Resource Generator author \[sn\_nb\_action.resource\_generator\_author\] to configure recommendations with Machine Learning \(ML\) solutions from TI models. In other words, the sn\_ti\_admin.tia\_user role is added to the Resource Generator author role.

-   **[Recommended Actions - Filter search results across multiple sources on the Search page](https://www.servicenow.com/docs/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Filter search results corresponding to multiple sources on the Search page. You can also filter the search results at facet-level.

-   **[Recommended Actions - Optimize the Recommended Actions refresh behavior by excluding non-critical field updates](https://www.servicenow.com/docs/access?context=ra-csm-contexts-create&family=zurich&ft:locale=en-US)**

Exclude the non-critical fields from triggering a Recommended Actions refresh on the record pages by adding the non-critical fields to the **Exclude fields** field on a context record. In a child context, you can also include the field exclusions of the parent context. You can enhance a user’s UI experience when you prevent excessive UI updates and still ensure that relevant updates trigger as intended.

-   **[Recommended Actions - Trigger Refresh for Recommendations explicitly or based on UI events](https://www.servicenow.com/docs/access?context=ra-csm-config-data-broker&family=zurich&ft:locale=en-US)**

Trigger recommendations refresh in the Recommended Actions tab on the contextual side panel when a UI or back-end event update is made. This provides dynamic and more contextually relevant recommendations based on the outcome of UI and back-end events. To trigger a recommendations refresh:

    -   configure UI component’s Data Broker in the UI builder for UI events
    -   execute the ForceRefreshRecommendationsscript include for back-end events
-   **[Recommended Actions - Configure dynamic JSON-based context inputs](https://www.servicenow.com/docs/access?context=ra-csm-create-context-inputs&family=zurich&ft:locale=en-US)**

Configure JSON-based context inputs in a context to populate accurate recommendations corresponding to dynamically changing contexts. You can conﬁgure parameters associated with the context table along with context table parameters. To support scenarios where a single workflow may leverage multiple active contexts simultaneously to generate recommendations. This uses the context inputs in rule condition builders, resource generators, and recommendation-action mappings, with minimal performance impact and backward compatibility.

-   **[Recommended Actions - Enhanced KB article sharing for Agents](https://www.servicenow.com/docs/access?context=ra-csm-guidances-attach-share-article&family=zurich&ft:locale=en-US)**

Identify the Knowledge Base \(KB\) articles that are not accessible to the case requester with the help of a Lock icon. In the recommendations on the contextual side panel of the CSM Configurable Workspace, a Lock icon on a recommendation card denotes that the recommended KB article cannot be accessed by the case requester.

-   **[Process Mining - SLA breach analysis](https://www.servicenow.com/docs/access?context=csm-integration-po&family=zurich&ft:locale=en-US)**

Identify and analyze cases where service level agreements \(SLAs\) have been violated. The SLA breach analysis project provides insights into the root causes of breaches, highlights bottlenecks, and recommends improvements to optimize the performance of your processes.

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&family=zurich&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Intelligence for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Between your current release family and Australia, some Intelligence for CSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Between your current release family and Australia, some Intelligence for CSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Review information on how to activate Intelligence for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Intelligence for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

If any specific browser requirements were introduced or changed for Intelligence for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Intelligence for CSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Intelligence for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

If there are specific highlight considerations for Intelligence for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Enabled Recommended Actions for chat interactions so that agents can select relevant actions that are based on the chat context.
-   Integrated enhanced knowledge guidance on the Front-line case page and enable agents to attach and add links to knowledge articles in comments, work notes, or emails by using modeless dialogs.
-   Enabled Recommended Actions – AI search for CSM default record page and CSM interaction record pages for the video, chat, walk-up, and email channels.
-   Automated the mapping configuration for search results along with default guidances.

 See [Intelligence for CSM](https://www.servicenow.com/docs/access?context=intelligence-csm&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Get enhanced visibility of knowledge base articles by marking and displaying a lock icon for articles that aren’t accessible to the case requester within the CSM Configurable Workspace.
-   Gain insights to the root causes of case service level agreement \(SLA\) breaches and view the suggested improvements to optimize process performance.

 See [Intelligence for CSM](https://www.servicenow.com/docs/access?context=intelligence-csm&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

