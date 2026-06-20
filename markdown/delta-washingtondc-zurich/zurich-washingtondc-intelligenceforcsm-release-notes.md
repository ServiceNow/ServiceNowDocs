---
title: Combined Intelligence for CSM release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Intelligence for CSM from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-intelligenceforcsm-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 18
breadcrumb: [Products combined by family]
---

# Combined Intelligence for CSM release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Intelligence for CSM from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Intelligence for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Intelligence for CSM to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Intelligence for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Task Intelligence for Customer Service - Document Classifier](https://servicenow-staging.fluidtopics.net/access?context=csm-document-intelligence&family=washingtondc&ft:locale=en-US)**

Quickly classify incoming documents as the appropriate document type by using the Document Classifier feature.

-   **[Task Intelligence for Customer Service - Performance reporting](https://servicenow-staging.fluidtopics.net/access?context=csm-task-intel-case-monitoring&family=washingtondc&ft:locale=en-US)**

Enhance the monitoring dashboard to display correct, incorrect, and skipped predictions by model and field, and compare models over a specified date range.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Recommended Actions - Task Intelligence similarity models integration](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-resource-generators&family=xanadu&ft:locale=en-US)**

Use similarity models that are integrated with the Task Intelligence \(TI\) admin console to configure, train, and deploy machine learning models.

    -   Resource Generator: The Recommended Actions framework supports a new resource generator that leverages TI similarity models to configure recommendations.
    -   Admin Configuration: Administrators can configure the resource generator to point to TI solutions for predictions and use the topN optional parameter to fetch top recommendations.
-   **Task intelligence for Customer Service - Dependent field predictions**

Help improve the model performance by identifying the dependent fields in a model before displaying the predicted values.

-   **[Task intelligence for Customer Service - Records prediction](https://servicenow-staging.fluidtopics.net/access?context=view-prediction-on-field-change&family=xanadu&ft:locale=en-US)**

Predict the configured fields on the case record after entering the short description or description and see the predicted values without saving the case form.

-   **[Task intelligence for Customer Service - On change predictions for interaction record](https://servicenow-staging.fluidtopics.net/access?context=view-prediction-on-field-change&family=xanadu&ft:locale=en-US)**

Predict the configured fields on the interaction record after entering the short description or description and see the predicted values without saving the form.

-   **[Task Intelligence for Customer Service - Implement Task Intelligence for the CSM Similarity Model:](https://servicenow-staging.fluidtopics.net/access?context=view-similar-case-recommendations&family=xanadu&ft:locale=en-US)**
    -   Similar cases recommendations:  Install the Task Intelligence for Customer Service plugin to view the preconfigured open and closed cases that are automatically trained and deployed as recommendations.
    -   Major case recommendations: Install the major issue management plugin and activate the feature as needed to get recommendations.
-   **[Recommended Actions - Create multiple contexts for a single record entity](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-contexts&family=xanadu&ft:locale=en-US)**

Support multiple contexts for the same table, such as the Case table, with one active context record that can be configured for the Recommended Actions component by using a UI Builder input property. By creating multiple contexts, you can create different experiences that are determined by criteria such as user attributes or domains. The recommendations and AI Search results adjust dynamically according to the configured active context.

-   **[Recommended Actions - Attach knowledge article guidance](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-guidances&family=xanadu&ft:locale=en-US)**

Enable agents to view and attach knowledge articles to task records and chat interaction records and share articles with customers by using the following guidances:

    -   Attach and share article: Enables the agent to share a recommended knowledge article in a comment, work note, or an email.
    -   Share article in chat interaction: Enables the agent to share a recommended knowledge article in a customer chat.
-   **[Guided Decisions - Run a guidance as a system user](https://servicenow-staging.fluidtopics.net/access?context=components-installed-with-guided-decisions&family=xanadu&ft:locale=en-US)**

Enable the **guidance\_honor\_subflow** system property to run a guidance in a decision tree as the user that is specified in the guidance action subflow properties. If this property is set to false, the guidance runs as the current user.

-   **[Guided Decisions - Decision Tree as a catalog item content type](https://servicenow-staging.fluidtopics.net/access?context=service-def-config-catalog-items&family=xanadu&ft:locale=en-US)**

Enable customers to add decision trees as catalog items in a service catalog. From the Customer Service Portal, customers can select the decision tree and open it in a new tab.

-   **[Guided Decisions - Search for decision trees on portal](https://servicenow-staging.fluidtopics.net/access?context=search-service-portal&family=xanadu&ft:locale=en-US)**

Enable portal users to search for decision trees with keywords. Selecting a decision tree in the search results opens a page with the decision tree widget.

-   **[Guided Decisions - Enable a start node to contain only task input](https://servicenow-staging.fluidtopics.net/access?context=guided-decision-tree-node-types&family=xanadu&ft:locale=en-US)**

Create start nodes for a decision tree that start directly from a task input and create paths that are derived from the data in the task reference. You have the option to create a start node from a question or from task input.

-   **[Guided Decisions - Restart a decision tree in a playbook](https://servicenow-staging.fluidtopics.net/access?context=add-guided-decision-playbook&family=xanadu&ft:locale=en-US)**

Restart the execution of a decision tree. When a user completes the execution of a decision tree in a playbook, they can start and complete the decision tree again if desired. Restarting the playbook retains the history of the previous decision tree executions.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Recommended Actions - Front-line case page integration with knowledge guidance](https://servicenow-staging.fluidtopics.net/access?context=csm-front-line-case-page&family=yokohama&ft:locale=en-US)**

Enable agents to attach and share knowledge article links in comments, work notes, or emails by using modeless dialogs.

-   **[Recommended Actions - Default guidance for search results](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-guidances-default-guidance-search&family=yokohama&ft:locale=en-US)**

Enable agents to view search results for any records. Use a default guidance for any search sources that don't have a dedicated, mapped guidance.

-   **[Recommended Actions - Improved timeout handling for resource generators](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-resource-generators&family=yokohama&ft:locale=en-US)**

Handle timeout errors when calling Machine Learning \(ML\) resource generators. The system uses a subflow API with a 1-second timeout ensures the RA generation engine prioritizes faster response times by terminating stalled ML prediction calls.

-   **[Recommended Actions - Custom guidances](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-custom-guidances&family=yokohama&ft:locale=en-US)**

Use a custom guidance to provide actions that are based on the search results from the Case, Problem, Incident, or Change Request tables. Agents can use these actions to link records to the current case and copy resolution codes and notes from resolved cases.

-   **[Recommended Actions - Field values for predicted records](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-guidances&family=yokohama&ft:locale=en-US)**

Leverage the actual field value for a predicted record and show it in a custom guidance in place of the display value.

-   **[Recommended Actions for Customer Service - Display Recommended Actions on the CSM Interaction record page](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-chat-interaction-record&family=yokohama&ft:locale=en-US)**

Enable agents to view Recommended Actions in the contextual side panel on the CSM Interaction record page. The search tab dynamically displays relevant actions based on the context of the chat interaction.

-   **[Recommended Actions for Customer Service - Interaction Context record](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-context-records&family=yokohama&ft:locale=en-US)**

Use the Interaction Context record to display the search results from the Knowledge table. The results are based on the interaction's short description. This context record includes a search-mapping record that maps knowledge results to the Share KB in chat interactions guidance.

-   **[Recommended Actions - Question font size customization for a Decision tree](https://servicenow-staging.fluidtopics.net/access?context=configure-decision-trees-gdb&family=yokohama&ft:locale=en-US)**

Enables you to customize the font size of questions in a Decision tree for a better look and feel. This font size is applied to the questions in the decision trees of playbooks, and recommendations, within the CSM Configurable Workspace and service portal.

-   **[Recommended Actions - Control the visibility of completed guidance information](https://servicenow-staging.fluidtopics.net/access?context=create-guidances&family=yokohama&ft:locale=en-US)**

Allows you to manage the visibility of the completed guidance history information of a decision tree in playbooks, and recommendations for an agent, within the CSM Configurable Workspace, and service portal for a streamlined experience.

-   **[Recommended Actions – AI search on CSM default record page, Front line case page, and CSM interaction record page](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-ai-search&family=yokohama&ft:locale=en-US)**

The Recommended Actions – AI search is introduced on the [CSM default record page](https://servicenow-staging.fluidtopics.net/access?context=csm-default-record-page&family=yokohama&ft:locale=en-US), [Front-line case page](https://servicenow-staging.fluidtopics.net/access?context=csm-front-line-case-page&family=yokohama&ft:locale=en-US), and [CSM Interaction record page](https://servicenow-staging.fluidtopics.net/access?context=csm-interaction-record-page&family=yokohama&ft:locale=en-US) \(for the chat, video, walk-up, and email type channels\) and it’s enabled by default for new customers. The default guidance is also enabled for these pages. Agents can attach and share knowledge article links in comments, work notes, and emails.

-   **[Recommended Actions - Catalog item source type for AI search](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-ai-search&family=yokohama&ft:locale=en-US)**

Search and filter the catalog items easily in the AI search tab of Recommended Actions in the CSM Configurable Workspace.

-   **[Recommended Actions - Ability to have multiple active contexts for the same table](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-contexts&family=yokohama&ft:locale=en-US)**

Enables multiple active contexts for the same table, so that tailored recommendations are displayed in the CSM Configurable Workspace:

    -   For different user personas based on their requirements.
    -   For different Predictive Intelligence models or AI model variants.
    -   For the same record in different channels, such as chat, email, and so on.
-   **[Recommended Actions - Ability to inherit active rules and their recommendations from a parent table context to extended table context](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-contexts&family=yokohama&ft:locale=en-US)**

Assign the active rules and their recommendations from the parent table context to the extended context table for a streamlined process.

-   **[Recommended Actions - Asynchronous evaluation for recommendations](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-contexts&family=yokohama&ft:locale=en-US)**

Enables you to configure loading behavior at the context level by choosing between synchronous and asynchronous modes. In the asynchronous mode, recommendations load in the background without blocking the UI, allowing agents to interact with the record immediately.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Guided Decisions - Enable Guided Decisions as a Playbook Activity with Inputs and Outputs](https://servicenow-staging.fluidtopics.net/access?context=add-gd-input-output-playbook&family=zurich&ft:locale=en-US)**

Added support for the Guided Decision with Inputs and Outputs activity in Playbook. Use this activity to embed decision trees that accept inputs and generate outputs, guiding users through complex decisions within your playbooks.

-   **[Recommended Actions - View the relevancy score of the AI search results](https://servicenow-staging.fluidtopics.net/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

View the relevancy score on the search result recommendation cards in the Search tab of the Recommended Actions panel for the default guidance for search results, Attach and share article, Share KB in chat interactions, and all no-code \( Link incident to current case, Link problem to current case, and Link change request to current case\) guidances. To enable this feature, you must enable the Show relevancy score for results check box in the Context form.

-   **[Recommended Actions – Limit the number of search results for more precise output](https://servicenow-staging.fluidtopics.net/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Limit the number of search results \(Top N\) that appear in the AI search tab in the Recommended Actions context side panel. To configure top N search results, you must enable the Top N check box in the Context form and then define the Search Results Limit in the Search Application Configuration.

-   **[Recommended Actions - Filter search results across multiple sources in the Contextual side panel](https://servicenow-staging.fluidtopics.net/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Filter search results corresponding to multiple sources in the AI search tab of the Recommended Actions contextual side panel. You can also filter the search results at the facet-level.

-   **[Recommended Actions – Track the AI search usage trends with the AI search analytics dashboard](https://servicenow-staging.fluidtopics.net/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Track and analyze the AI search usage in Recommended Actions using the AI search analytics dashboard. The AI search events and actions performed by the agent are captured in the Search Events, Search Source Events, Search Signal Events, Search Result Event, and Search Result Event Action tables. This data is used in the AI search analytics dashboard.

-   **[Recommended Actions - Read-only access to TI solutions for the Resource Generator author role](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-installed-components&family=zurich&ft:locale=en-US)**

Access Task Intelligence \(TI\) solution definitions in read-only mode as a Resource Generator author \[sn\_nb\_action.resource\_generator\_author\] to configure recommendations with Machine Learning \(ML\) solutions from TI models. In other words, the sn\_ti\_admin.tia\_user role is added to the Resource Generator author role.

-   **[Recommended Actions - Filter search results across multiple sources on the Search page](https://servicenow-staging.fluidtopics.net/access?context=nba-use-ai-search&family=zurich&ft:locale=en-US)**

Filter search results corresponding to multiple sources on the Search page. You can also filter the search results at facet-level.

-   **[Recommended Actions - Optimize the Recommended Actions refresh behavior by excluding non-critical field updates](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-contexts-create&family=zurich&ft:locale=en-US)**

Exclude the non-critical fields from triggering a Recommended Actions refresh on the record pages by adding the non-critical fields to the **Exclude fields** field on a context record. In a child context, you can also include the field exclusions of the parent context. You can enhance a user’s UI experience when you prevent excessive UI updates and still ensure that relevant updates trigger as intended.

-   **[Recommended Actions - Trigger Refresh for Recommendations explicitly or based on UI events](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-config-data-broker&family=zurich&ft:locale=en-US)**

Trigger recommendations refresh in the Recommended Actions tab on the contextual side panel when a UI or back-end event update is made. This provides dynamic and more contextually relevant recommendations based on the outcome of UI and back-end events. To trigger a recommendations refresh:

    -   configure UI component’s Data Broker in the UI builder for UI events
    -   execute the ForceRefreshRecommendationsscript include for back-end events
-   **[Recommended Actions - Configure dynamic JSON-based context inputs](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-create-context-inputs&family=zurich&ft:locale=en-US)**

Configure JSON-based context inputs in a context to populate accurate recommendations corresponding to dynamically changing contexts. You can conﬁgure parameters associated with the context table along with context table parameters. To support scenarios where a single workflow may leverage multiple active contexts simultaneously to generate recommendations. This uses the context inputs in rule condition builders, resource generators, and recommendation-action mappings, with minimal performance impact and backward compatibility.

-   **[Recommended Actions - Enhanced KB article sharing for Agents](https://servicenow-staging.fluidtopics.net/access?context=ra-csm-guidances-attach-share-article&family=zurich&ft:locale=en-US)**

Identify the Knowledge Base \(KB\) articles that are not accessible to the case requester with the help of a Lock icon. In the recommendations on the contextual side panel of the CSM Configurable Workspace, a Lock icon on a recommendation card denotes that the recommended KB article cannot be accessed by the case requester.

-   **[Process Mining - SLA breach analysis](https://servicenow-staging.fluidtopics.net/access?context=csm-integration-po&family=zurich&ft:locale=en-US)**

Identify and analyze cases where service level agreements \(SLAs\) have been violated. The SLA breach analysis project provides insights into the root causes of breaches, highlights bottlenecks, and recommends improvements to optimize the performance of your processes.

-   **[Quick start tests for Customer Service Management](https://servicenow-staging.fluidtopics.net/access?context=quick-start-tests-csm&family=zurich&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Intelligence for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Task Intelligence Admin Console](https://servicenow-staging.fluidtopics.net/access?context=csm-task-intel-admin-center&family=washingtondc&ft:locale=en-US) enhancements**

Use the Task Intelligence Admin Console to perform the following tasks:

    -   View the model performance for the top three recommendations and decide between auto-fill or recommend mode as the prediction preference based on the data.
    -   View the model performance by field on the Admin Console dashboard.
    -   Filter out inactive choice predictions.
-   **[Task intelligence model and UI enhancements](https://servicenow-staging.fluidtopics.net/access?context=case-categorization-overview&family=washingtondc&ft:locale=en-US)**

The following enhancements have been made in Task intelligence:

    -   Introduced a new Now Assist system user for AI applications that captures AI changes in the card in the activity stream. This feature is also supported for Document Intelligence for Customer Service predictions.
    -   Added an "Updating" message in the banner to let users know that AI predictions are currently being processed.
-   **[Guided Decisions](https://servicenow-staging.fluidtopics.net/access?context=setting-up-guided-decisions&family=washingtondc&ft:locale=en-US) enhancements**

Use Guided Decisions to perform the following tasks:

    -   Enable self-service for internal users by rendering decision trees in a Service Portal.
    -   Link existing decision trees as children to your current decision tree.
    -   Enable agents or customers to revisit or change the previous responses in the decision tree run-time experience.
    -   Control the appearance of the **Dismiss** button in the decision tree run-time experience.
Added the following enhancements to the decision trees:

    -   Decision tree portal widgets that are available to external users
    -   Outputs to decision trees so users can embed decision trees inside other trees.
    -   Intermediate nodes to decision trees.
-   **[Recommended Actions](https://servicenow-staging.fluidtopics.net/access?context=nba&family=washingtondc&ft:locale=en-US) enhancements**

Define the number of records or values to return for the Task Intelligence Classification resource generator through the Top N Results feature.

    -   User interface improvements so that agents can more easily replace Agent Assist with Recommended Actions. These improvements include a new Recommended Actions icon, configuration fields to support automatic search result experience, and the ability to filter on facets within a search source entity.
    -   User interface improvements to the “Review and attach article” guidance.
    -   A full view search experience in a subtab.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Guided Decisions - Question field updated to type HTML](https://servicenow-staging.fluidtopics.net/access?context=guided-decision-tree-node-types&family=xanadu&ft:locale=en-US)**

The **Question** field has been updated from type=string to type=HTML. When adding a question to a decision node, decision tree authors can include the text, formatted text, and images in the **Question** field.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Intelligence for CSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Intelligence for CSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Intelligence for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Install the Guided Decisions, Recommended Actions, and Task Intelligence applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Install the Guided Decisions, Recommended Actions, and Task Intelligence applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateCustomerService&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateCustomerService&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Intelligence for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Intelligence for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Intelligence for CSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **Support for reflow**

The following components were updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

Version 28.0.0 of Recommended Actions:

    -   sn-template-modal-worknotes
    -   sn-component-attach-article-guidance
    -   sn-next-best-action-list-connected
    -   sn-guidance-experience-list-connected
Version 25.1.0 of Guided Decisions:

    -   sn-guided-decision-card
    -   sn-guided-decision-playbook-card
This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=washingtondc&ft:locale=en-US) for details.


</td></tr><tr><td>

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

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Intelligence for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Intelligence for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Increase efficiency and automation by using the document classifier feature to categorize incoming documents.
-   View prediction performance during model training to determine your preference for either an auto-fill or recommendation as the prediction method.
-   Render decision trees in a Service Portal for internal users.
-   Reduce the effort in decision tree re-creation by reusing an activated child tree in the current decision tree.

 See [Intelligence](https://servicenow-staging.fluidtopics.net/access?context=intelligence-csm&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Create multiple Recommended Actions context records for the same table to create different experiences that are based on criteria such as user attributes or domains.
-   Restart a decision tree in a playbook and retain the history of previous decision tree executions.
-   Enable customers to add decision trees as catalog items in a service catalog.
-   Enable your users to search for decision trees by using keywords and open a decision tree from the search results.

 See [Intelligence for CSM](https://servicenow-staging.fluidtopics.net/access?context=intelligence-csm&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Enabled Recommended Actions for chat interactions so that agents can select relevant actions that are based on the chat context.
-   Integrated enhanced knowledge guidance on the Front-line case page and enable agents to attach and add links to knowledge articles in comments, work notes, or emails by using modeless dialogs.
-   Enabled Recommended Actions – AI search for CSM default record page and CSM interaction record pages for the video, chat, walk-up, and email channels.
-   Automated the mapping configuration for search results along with default guidances.

 See [Intelligence for CSM](https://servicenow-staging.fluidtopics.net/access?context=intelligence-csm&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Get enhanced visibility of knowledge base articles by marking and displaying a lock icon for articles that aren’t accessible to the case requester within the CSM Configurable Workspace.
-   Gain insights to the root causes of case service level agreement \(SLA\) breaches and view the suggested improvements to optimize process performance.

 See [Intelligence for CSM](https://servicenow-staging.fluidtopics.net/access?context=intelligence-csm&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

