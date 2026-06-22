---
title: Combined Workflow Studio release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Workflow Studio from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-workflowstudio-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Workflow Studio release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Workflow Studio from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Workflow Studio release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Workflow Studio to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

To receive Workflow Studio performance improvements, install one of these versions of the Workflow Studio application from the ServiceNow Store.

 |Is Now Assist for Creator already installed?|Version of Workflow Studio to use for upgrade|
|--------------------------------------------|---------------------------------------------|
|No|Upgrade Workflow Studio to version 25.1.3|
|Yes|Upgrade Workflow Studio to version 25.0.0|

</td></tr><tr><td>

Xanadu

</td><td>

As of Washington DC patch 3, updating Workflow Studio automatically updates all of its application dependencies such as ServiceNow® Workflow Studio, Playbook, and ServiceNow® Decision Builder. You can no longer see or update the individual application dependencies of Workflow Studio from the ServiceNow® Store or the list of plugins.

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

Between your current release family and Australia, new features were introduced for Workflow Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Annotations support in diagramming view](https://www.servicenow.com/docs/access?context=flow-diagramming-view&family=washingtondc&ft:locale=en-US)**

Add and edit annotations in the diagramming view.

-   **[Content filtering for flow execution details](https://www.servicenow.com/docs/access?context=content-filtering-flow-designer&family=washingtondc&ft:locale=en-US)**

Restrict access to the sensitive content within the flow execution details with a content filtering rule.

-   **[Create an action input from a step input](https://www.servicenow.com/docs/access?context=create-action-input-from-step-input&family=washingtondc&ft:locale=en-US)**

Create an action input based on the data type of a step input. Map the step input value to the new action input.

-   **[Exit Loop flow logic](https://www.servicenow.com/docs/access?context=exit-loop-flow-logic&family=washingtondc&ft:locale=en-US)**

Exit from a flow logic loop when the conditions of an If flow logic are met. Continue running the flow from the next step after the flow logic loop. This flow logic is also known as break.

-   **[FDIH Dashboard](https://www.servicenow.com/docs/access?context=fdih-dashboard&family=washingtondc&ft:locale=en-US)**

View the average and maximum run times of flows during the last 14 days. Use the trend data to identify the flows that are running unexpectedly.

-   **[Flow generation](https://www.servicenow.com/docs/access?context=flow-generation&family=washingtondc&ft:locale=en-US)**

Create multi-step flow outlines with generative AI. Flow outlines require configuration to add input values and data references.

-   **[Generate flow execution details for all iterations of a loop.](https://www.servicenow.com/docs/access?context=flow-execution-settings&family=washingtondc&ft:locale=en-US)**

Create an execution settings record to generate flow execution details for all iterations of a loop rather than just the first and last iterations of a loop.

-   **[Go back to flow logic](https://www.servicenow.com/docs/access?context=go-back-to-flow-logic&family=washingtondc&ft:locale=en-US)**

Return to a prior step in the flow to repeat a sequence of actions.

-   **[Preview and rebuild flow outlines when creating a flow with Now Assist](https://www.servicenow.com/docs/access?context=create-flow-now-assist&family=washingtondc&ft:locale=en-US)**

See a diagram preview of the flow outline when creating a flow with Now Assist. If the generated flow preview does not meet your needs, update the text directions, and rebuild the flow outline.

-   **[Proactive Analytics trigger](https://www.servicenow.com/docs/access?context=flow-triggers&family=washingtondc&ft:locale=en-US)**

Use Performance Analytics indicators to start a flow. Define the flow start conditions as a set of Proactive Analytics KPI scores and KPI threshold values.

-   **[Show approver names in stage field](https://www.servicenow.com/docs/access?context=flow-designer-stages&family=washingtondc&ft:locale=en-US)**

Show the list of approvers assigned to a stage from a stage field. Control whether to show approvers and the maximum number of approvers to show with separate system properties.

-   **[Skip Iteration flow logic](https://www.servicenow.com/docs/access?context=skip-iteration-flow-logic&family=washingtondc&ft:locale=en-US)**

Skip the current iteration of a flow logic loop when the conditions of an If flow logic are met. Continue running the flow logic loop with the next item in the list. This flow logic is also known as continue.

-   **[Support for Retrieval Augmented Generation \(RAG\) with flow generation](https://www.servicenow.com/docs/access?context=flow-generation&family=washingtondc&ft:locale=en-US)**

Generate flows from directions that refer to custom actions and subflows or content from installed spokes. Include the names of commonly used and recently published actions and subflows available on your instance in your flow generation requests.

-   **[Try support in diagramming view](https://www.servicenow.com/docs/access?context=flow-diagramming-view&family=washingtondc&ft:locale=en-US)**

Add and configure Try flow logic in the diagramming view.

-   **[Undo and redo support](https://www.servicenow.com/docs/access?context=flow-edit&family=washingtondc&ft:locale=en-US)**

Undo changes that you've made while editing a flow. Redo the changes that you’ve undone. Workflow Studio only tracks changes while you're editing a flow.

-   **[User preference for default Flow Designer view](https://www.servicenow.com/docs/access?context=flow-preferences&family=washingtondc&ft:locale=en-US)**

Set the flow diagramming view as the default Workflow Studio view.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Create workflow items from a button on the tab header](https://www.servicenow.com/docs/access?context=exploring-workflow-studio&family=xanadu&ft:locale=en-US)**

Create workflow items from any Workflow Studio page by using the **Create** button on the tab header.

-   **[Create a category to organize your actions](https://www.servicenow.com/docs/access?context=create-action&family=xanadu&ft:locale=en-US)**

Create your own categories to organize actions.

-   **[Create a category to organize your data stream actions](https://www.servicenow.com/docs/access?context=create-data-stream-action&family=xanadu&ft:locale=en-US)**

Create your own categories to organize data stream actions.

-   **[Create a category to organize your subflows](https://www.servicenow.com/docs/access?context=create-subflow&family=xanadu&ft:locale=en-US)**

Create your own categories to organize subflows.

-   **[See when a new version of Workflow Studio is available](https://www.servicenow.com/docs/access?context=update-to-the-latest-version-of-workflow-studio&family=xanadu&ft:locale=en-US)**

See an information banner when a new version of Workflow Studio is available.


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

Between your current release family and Australia, some changes were made to existing Workflow Studio features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Flow execution details only record the first and last iterations of loops](https://www.servicenow.com/docs/access?context=flow-execution-settings&family=washingtondc&ft:locale=en-US)**

Flow execution details only record the first and last iterations of a loop. This setting reduces the amount of execution details that the instance has to generate and store. You can change this setting on a flow-by-flow basis by creating a flow execution settings record.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Update Workflow Studio and all its dependencies](https://www.servicenow.com/docs/access?context=update-to-the-latest-version-of-workflow-studio&family=xanadu&ft:locale=en-US)**

As of Washington DC patch 3, updating Workflow Studio automatically updates all of its application dependencies such as Workflow Studio, Playbook, and Decision Builder. You can no longer see or update the individual application dependencies of Workflow Studio from the ServiceNow Store or the list of plugins.


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

Between your current release family and Australia, some Workflow Studio features or functionality were removed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Workflow Studio features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Deprecated the system property com.snc.process\_flow.reporting.iteration.lastn that specifies the number of loop iterations that a flow generates execution details for. This property only applies to flows created prior to the Washington DC release. New flows only generate execution details for the first and last iterations of a loop. To report on all iterations of a loop, create a flow execution settings record for the flow instead. For more information about flow execution settings, see [Flow execution settings](https://www.servicenow.com/docs/access?context=flow-execution-settings&family=washingtondc&ft:locale=en-US).

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Workflow Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Workflow Studio is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Xanadu

</td><td>

Install Workflow Studio by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

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
</table>## Additional requirements

If any additional requirements were introduced or changed for Workflow Studio we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Workflow Studio we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Workflow Studio, such as specific requirements or compliance levels.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Workflow Studio we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Workflow Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Create multi-step flows with generative AI.
-   Open Workflow Studio from within Workflow Studio.
-   Preview and rebuild flow outlines with Now Assist
-   Save flows automatically as you work on them.
-   Start a flow when Performance Analytics conditions are met.
-   Undo changes that you've made while editing a flow.
-   Use the flow diagramming view to add annotations and Try flow logic.

 See [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Create workflow items from any Workflow Studio page by using the **Create** button on the tab header.
-   Create your own categories to organize actions, data streams, and subflows.
-   Monitor playbook and flow operations with new usage dashboards.
-   See an information banner when a new version of Workflow Studio is available.

 See [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&family=xanadu&ft:locale=en-US) for more information.

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

