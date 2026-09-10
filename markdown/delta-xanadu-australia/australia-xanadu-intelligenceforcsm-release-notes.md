---
title: Combined Intelligence for CSM release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Intelligence for CSM from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-intelligenceforcsm-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Intelligence for CSM release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Intelligence for CSM from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Intelligence for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Intelligence for CSM to Australia

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

Between your current release family and Australia, new features were introduced for Intelligence for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Recommended Actions - Task Intelligence similarity models integration](https://www.servicenow.com/docs/access?context=ra-csm-resource-generators&family=xanadu&ft:locale=en-US)**

Use similarity models that are integrated with the Task Intelligence \(TI\) admin console to configure, train, and deploy machine learning models.

    -   Resource Generator: The Recommended Actions framework supports a new resource generator that leverages TI similarity models to configure recommendations.
    -   Admin Configuration: Administrators can configure the resource generator to point to TI solutions for predictions and use the topN optional parameter to fetch top recommendations.
-   **Task intelligence for Customer Service - Dependent field predictions**

Help improve the model performance by identifying the dependent fields in a model before displaying the predicted values.

-   **[Task intelligence for Customer Service - Records prediction](https://www.servicenow.com/docs/access?context=view-prediction-on-field-change&family=xanadu&ft:locale=en-US)**

Predict the configured fields on the case record after entering the short description or description and see the predicted values without saving the case form.

-   **[Task intelligence for Customer Service - On change predictions for interaction record](https://www.servicenow.com/docs/access?context=view-prediction-on-field-change&family=xanadu&ft:locale=en-US)**

Predict the configured fields on the interaction record after entering the short description or description and see the predicted values without saving the form.

-   **[Task Intelligence for Customer Service - Implement Task Intelligence for the CSM Similarity Model:](https://www.servicenow.com/docs/access?context=view-similar-case-recommendations&family=xanadu&ft:locale=en-US)**
    -   Similar cases recommendations:  Install the Task Intelligence for Customer Service plugin to view the preconfigured open and closed cases that are automatically trained and deployed as recommendations.
    -   Major case recommendations: Install the major issue management plugin and activate the feature as needed to get recommendations.
-   **[Recommended Actions - Create multiple contexts for a single record entity](https://www.servicenow.com/docs/access?context=ra-csm-contexts&family=xanadu&ft:locale=en-US)**

Support multiple contexts for the same table, such as the Case table, with one active context record that can be configured for the Recommended Actions component by using a UI Builder input property. By creating multiple contexts, you can create different experiences that are determined by criteria such as user attributes or domains. The recommendations and AI Search results adjust dynamically according to the configured active context.

-   **[Recommended Actions - Attach knowledge article guidance](https://www.servicenow.com/docs/access?context=ra-csm-guidances&family=xanadu&ft:locale=en-US)**

Enable agents to view and attach knowledge articles to task records and chat interaction records and share articles with customers by using the following guidances:

    -   Attach and share article: Enables the agent to share a recommended knowledge article in a comment, work note, or an email.
    -   Share article in chat interaction: Enables the agent to share a recommended knowledge article in a customer chat.
-   **[Guided Decisions - Run a guidance as a system user](https://www.servicenow.com/docs/access?context=components-installed-with-guided-decisions&family=xanadu&ft:locale=en-US)**

Enable the **guidance\_honor\_subflow** system property to run a guidance in a decision tree as the user that is specified in the guidance action subflow properties. If this property is set to false, the guidance runs as the current user.

-   **[Guided Decisions - Decision Tree as a catalog item content type](https://www.servicenow.com/docs/access?context=service-def-config-catalog-items&family=xanadu&ft:locale=en-US)**

Enable customers to add decision trees as catalog items in a service catalog. From the Customer Service Portal, customers can select the decision tree and open it in a new tab.

-   **[Guided Decisions - Search for decision trees on portal](https://www.servicenow.com/docs/access?context=search-service-portal&family=xanadu&ft:locale=en-US)**

Enable portal users to search for decision trees with keywords. Selecting a decision tree in the search results opens a page with the decision tree widget.

-   **[Guided Decisions - Enable a start node to contain only task input](https://www.servicenow.com/docs/access?context=guided-decision-tree-node-types&family=xanadu&ft:locale=en-US)**

Create start nodes for a decision tree that start directly from a task input and create paths that are derived from the data in the task reference. You have the option to create a start node from a question or from task input.

-   **[Guided Decisions - Restart a decision tree in a playbook](https://www.servicenow.com/docs/access?context=add-guided-decision-playbook&family=xanadu&ft:locale=en-US)**

Restart the execution of a decision tree. When a user completes the execution of a decision tree in a playbook, they can start and complete the decision tree again if desired. Restarting the playbook retains the history of the previous decision tree executions.


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

Between your current release family and Australia, some changes were made to existing Intelligence for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Guided Decisions - Question field updated to type HTML](https://www.servicenow.com/docs/access?context=guided-decision-tree-node-types&family=xanadu&ft:locale=en-US)**

The **Question** field has been updated from type=string to type=HTML. When adding a question to a decision node, decision tree authors can include the text, formatted text, and images in the **Question** field.


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

Between your current release family and Australia, some Intelligence for CSM features or functionality were removed.

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

Between your current release family and Australia, some Intelligence for CSM features or functionality were deprecated.

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

Review information on how to activate Intelligence for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install the Guided Decisions, Recommended Actions, and Task Intelligence applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **Activation information**

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

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

If any specific browser requirements were introduced or changed for Intelligence for CSM we have noted them here.

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

-   **Browser requirements**

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Browser requirements**

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
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


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

If there are specific highlight considerations for Intelligence for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Create multiple Recommended Actions context records for the same table to create different experiences that are based on criteria such as user attributes or domains.
-   Restart a decision tree in a playbook and retain the history of previous decision tree executions.
-   Enable customers to add decision trees as catalog items in a service catalog.
-   Enable your users to search for decision trees by using keywords and open a decision tree from the search results.

 See [Intelligence for CSM](https://www.servicenow.com/docs/access?context=intelligence-csm&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

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

-   Get enhanced visibility of knowledge base articles by marking and displaying a lock icon for articles that aren’t accessible to the case requester within the CRM Workspace.
-   Gain insights to the root causes of case service level agreement \(SLA\) breaches and view the suggested improvements to optimize process performance.

 See [Intelligence for CSM](https://www.servicenow.com/docs/access?context=intelligence-csm&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

