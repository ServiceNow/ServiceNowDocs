---
title: Configuring Recommended Actions
description: Use the Recommended Actions application to display relevant actions to agents based on a context of a record or enable agents to perform an AI search to find relevant resources. Agents can quickly and easily take action to help customers and resolve their issues.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Implement Intelligence, Configure, Customer Service Management]
---

# Configuring Recommended Actions

Use the Recommended Actions application to display relevant actions to agents based on a context of a recordor enable agents to perform an AI search to find relevant resources. Agents can quickly and easily take action to help customers and resolve their issues.

![Recommended actions and Search tabs in the contextual side panel in CSM Configurable Workspace](../image/ra-actions-overview-2.png "Recommended Actions in CSM Configurable Workspace")

With Recommended Actions:

-   Provide agents with optimal action in a context of a record.
-   Enable agents to focus their attention to the critical call-to-action.
-   Allow agents to take an action in a contextual side panel or in a subtab.
-   Enable agents to troubleshoot and provide a resolution to customers.
-   Rank actions that agents can take based on a configurable logic.
-   Recommend a value for a field on a form.
-   Enable agents to use AI search to find the most relevant resources.

## Example scenarios for implementing Recommended Actions

Use Recommended Actions to provide the following recommendations:

-   Apply resolution from a solved case: Recommend agents to apply resolution from a similar solved case and then close the case.
-   Reassign case: Recommend a field value for the Assignment group field so that the case is assigned to the relevant team.
-   View and attach article: Recommend a Knowledge article relevant to the customer issue so that agents can view and attach the article to the current case.
-   Review a refund request. Recommend a decision tree for agents to work through to determine if the customer is eligible for a refund.

For end-to-end configurations of recommended actions for specific scenarios, see [Example configurations of recommended actions](recommended-actions-use-case.md).

## Action types for Recommended Actions

With the Recommended Actions application, you can create the following types of actions for agents to take. For more information, see [Recommended Actions](configure-nba.md).

<table id="table_nxk_y1t_c5b"><thead><tr><th>

Action type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Guidance**

</td><td>

An action that an agent can take or information they can share. For example, guidance can recommend that an agent can attach a knowledge article in comment, work note, or mail of a case or create a work order.

</td></tr><tr><td>

**Guided decision tree**

</td><td>

A guided flow to follow. A decision tree is a multi-step process that includes a series of questions and answers and results in guidance.

</td></tr><tr><td>

**Field recommendation**

</td><td>

A recommended value to use for a field. For example, this type of action can recommend the assignment group based on the text in the case short description.

</td></tr></tbody>
</table>## AI search

Agents can enter their queries in the search bar to access AI-powered search results. The most relevant answers for the search query appear as genius result cards. Agents can take the actions from the search cards directly to resolve an issue. For more information, see [AI search in Recommended Actions](ra-csm-ai-search.md).

-   **Benefits of AI search integration with Recommended Actions**
    -   Unified search and recommendations: This integration combines AI-driven search capabilities with proactive recommendations, providing a unified toolset for agents.
    -   Contextual intelligence: The system leverages contextual data to deliver highly relevant search results and recommendations tailored to each case.
    -   Proactive recommendations: Agents receive actionable suggestions to accelerate case resolution, based on real-time case context.
    -   Seamless workflow: The integration streamlines the user workflow by providing access to search and recommendations within a single interface.

## Using recommended actions

Agents can access recommended actions in a workspace such as CSM Configurable Workspace by selecting the Recommended Actions icon \(![Recommended Actions icon](../image/nba-icon.png)\) in the contextual side panel. For more information, see [Using the Recommended Actions application](ra-csm-using-recommended-actions.md).

## Setting up recommended actions

Set up the Recommended Actions application so that you can create actions of type guidance or field recommendation. An admin can complete the following setup tasks.

<table id="table_vcr_lms_h5b"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Install the Recommended Actions application](../task/install-recommended-actions-cs-app.md)

</td><td>

Download the Recommended Actions application from the ServiceNow® Store.

</td></tr><tr><td>

[Assign roles to Recommended Actions users](../reference/ra-csm-installed-components.md)

</td><td>

Assign roles to your users to control access to Recommended Actions features and information.

</td></tr><tr><td>

[Configuring the Recommended Actions application](configure-recommended-actions.md)

</td><td>

Configure recommended actions to create a context, rule, and recommendations with action types such as guidance and field recommendation.**Note:** The Guided Decisions application \(sn\_gd\_core\) is required to create guided decision trees.

</td></tr></tbody>
</table>**Note:** To ensure Recommended Actions loads automatically and performs optimally, enable the **Enable prefetch** check box and verify that the **Get recommendations** data broker exists under Data Resources. This enhancement applies only to the Front-line Case page and CSM default record page and requires Recommended Actions to be enabled on the page. If you have any custom variants created before this enhancement, you must manually enable these settings.

**Note:** If Recommended Actions doesn't appear on a variant of a record page \(such as the CSM default record page, CSM Interaction record page, or Front-line case page\), ensure that the variant is marked active. For detailed steps, see [Restore Recommended Actions on record page variants after upgrade](../task/ra-csm-enable-ra-variant-record-page.md).

## Integrating decision trees in recommended actions

Optionally, set up the Guided Decisions Experience application so that you can create decision trees and then integrate them in recommended actions. Admins can complete the following setup tasks.

|Setup task|Description|
|----------|-----------|
|[Install the Guided Decisions Experience application](../task/install-guided-decisions-exp-app-new.md)|Install the Guided Decisions Experience application from the ServiceNow® Store. This application enables you to configure decision trees that you can use as recommendations.|
|[Configuring decision trees](configuring-guided-decisions.md)|Configure decision trees that agents can use to troubleshoot solutions for customer issues.|
|[Add Guided Decisions to Recommended Actions](../task/add-guided-decisions-to-recommended-actions.md)|Add decision trees to recommended actions, so that agents can take relevant action during troubleshooting based on a record context.|

## Request apps from the ServiceNow Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

