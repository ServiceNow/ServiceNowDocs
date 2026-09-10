---
title: Combined Flows, subflows, and actions release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Flows, subflows, and actions from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-flowssubflowsandactions-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Flows, subflows, and actions release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Flows, subflows, and actions from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Flows, subflows, and actions release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Flows, subflows, and actions to Australia

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

-   **Upgrade information**

An earlier version of the save as you go feature was released and withdrawn from the Washington DC release. If you're upgrading from the Washington DC release, you might have manually turned off the save as you go features by setting a system property. To restore the save as you go features, see [Restore save as you go functionality](https://www.servicenow.com/docs/access?context=restore-save-as-you-go-functionality&family=australia&ft:locale=en-US).

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Flows, subflows, and actions.

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

-   **[Configure conversational settings](https://www.servicenow.com/docs/access?context=configure-subflow-conversation-settings&family=yokohama&ft:locale=en-US)**

View the subflows and actions that are conversational compatible. Configure conversational settings to make a subflow or action available to conversational interfaces.


 -   **[Debug flows and subflows](https://www.servicenow.com/docs/access?context=flow-debugger&family=yokohama&ft:locale=en-US)**

Debug flows and subflows from a dedicated Workflow Studio tab. Set breakpoints and step through a paused flow to review configuration and runtime values.

-   **[Save a flow trigger for reuse in other flows](https://www.servicenow.com/docs/access?context=saved-flow-triggers&family=yokohama&ft:locale=en-US)**

Save a set of trigger definitions as a reusable trigger. Enable flow authors to select the saved trigger from some or all application flows. Specify whether flow authors can see the trigger details or add conditions to the trigger.

-   **[Use the Flow API to send a message to a paused flow](https://www.servicenow.com/docs/access?context=FlowAPI-sendMessage_S_S_S&family=yokohama&ft:locale=en-US)**

Send a specific message and payload response to a flow that is paused and waiting for a message.

-   **[Wait for a specific message from the Flow API](https://www.servicenow.com/docs/access?context=wait-for-message-action&family=yokohama&ft:locale=en-US)**

Pause a flow until it receives a specific message from the flow API. Specify the string message that resumes running the flow, and optionally provide a time out value to resume the flow if no message is received after a specific amount of time.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Create and manage external event sources](https://www.servicenow.com/docs/access?context=manage-external-event-sources&family=zurich&ft:locale=en-US)**

Create an external event source on your ServiceNow instance that listens to events occurring in an application or system outside of the ServiceNow AI Platform®. Based on the external event source, you can define one or more external trigger definitions in your instance and then associate the external trigger definitions with the external event source. When an event that you specified in the external trigger definition occurs, the external trigger definition executes one or more flows. You can update or remove external event sources that you create.

-   **[Create a domain-separated saved external trigger](https://www.servicenow.com/docs/access?context=create-saved-external-trigger&family=zurich&ft:locale=en-US)**

Create a domain-separated saved external trigger. Configurations that you make to the trigger are auto-saved. After the trigger is published, you can edit only the **Label** field values.

-   **[Create a reusable scheduled trigger](https://www.servicenow.com/docs/access?context=create-scheduled-trigger&family=zurich&ft:locale=en-US)**

Create a scheduled trigger that starts your flow when you need. Use the trigger across your flows.

-   **[Make a flow wait for an email reply](https://www.servicenow.com/docs/access?context=wait-for-email-reply-action&family=zurich&ft:locale=en-US)**

Pause a flow until an email reply is received to an outbound email record

-   **[Show subflow stages in a parent flow](https://www.servicenow.com/docs/access?context=show-subflow-stages-in-a-parent-flow&family=zurich&ft:locale=en-US)**

Show subflow stages as part of the execution details of a parent flow.

-   **[Save flows, subflows, and actions automatically](https://www.servicenow.com/docs/access?context=save-as-you-go-flows&family=zurich&ft:locale=en-US)**

Save flows, subflows, and actions automatically as you work on them.

-   **[View flow history](https://www.servicenow.com/docs/access?context=flow-history&family=zurich&ft:locale=en-US)**

View and manage the history of a flow. See past configurations of a flow to copy, restore, or remove them.

-   **[View subflow history](https://www.servicenow.com/docs/access?context=subflow-history&family=zurich&ft:locale=en-US)**

View and manage the history of a subflow. See past configurations of a subflow to copy, restore, or remove them.


</td></tr><tr><td>

Australia

</td><td>

-   **[Business calendar as a scheduled trigger](https://www.servicenow.com/docs/access?context=create-trigger-business-calendar&family=australia&ft:locale=en-US)**

Use the business calendar to trigger flows on existing business schedules. The business calendar trigger helps align automation with shifts, holidays, and operating hours.

-   **[Flow history compare view](https://www.servicenow.com/docs/access?context=flow-history-compare-view&family=australia&ft:locale=en-US)**

Compare two flow history entries in a side-by-side view. Use the step highlighting and change type icons to determine what flow components have been added, removed, and changed.

-   **[Flow execution analysis](https://www.servicenow.com/docs/access?context=flow-execution-analysis-landing&family=australia&ft:locale=en-US)**

Analyze flow execution details to identify errors and suggest potential fixes.

-   **[Test conversational action](https://www.servicenow.com/docs/access?context=test-conversational-action&family=australia&ft:locale=en-US)**

Test a conversational action to verify it responds correctly to user inputs and performs the expected operations before deploying it in production.

-   **[Test conversational subflow](https://www.servicenow.com/docs/access?context=test-conversational-subflow&family=australia&ft:locale=en-US)**

Test a conversational subflow to verify it responds correctly to user inputs and performs the expected operations before deploying it in production.

-   **[Use an AI agent action](https://www.servicenow.com/docs/access?context=use-an-ai-agent-action&family=australia&ft:locale=en-US)**

Use flow data to run an AI agent and configure the expected agent output for use later in the flow.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Flows, subflows, and actions features.

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

-   **[Display text descriptions of data changes](https://www.servicenow.com/docs/access?context=exploring-flows&family=yokohama&ft:locale=en-US)**

See a natural language description of the data each component of a flow uses. Understand what data flow triggers, actions, and flow logic blocks use without having to open their configuration details.


</td></tr><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Display flow recommendations in flow diagramming view](https://www.servicenow.com/docs/access?context=exploring-flow-recommendations&family=zurich&ft:locale=en-US)**

Get a list of recommendations for the next item in your flow while in a flow diagramming view.

-   **[Launch the flow debugger from an updated button](https://www.servicenow.com/docs/access?context=flow-debugger&family=zurich&ft:locale=en-US)**

Start the flow debugger from an updated button.

-   **[Open conversational subflow settings from an updated button](https://www.servicenow.com/docs/access?context=configure-subflow-conversation-settings&family=zurich&ft:locale=en-US)**

The option to open subflow conversational settings has moved from the more action menu to the sidebar.

-   **[Open conversational action settings from an updated button](https://www.servicenow.com/docs/access?context=configure-action-conversation-settings&family=zurich&ft:locale=en-US)**

The option to open action conversational settings has moved from the more action menu to the sidebar.

-   **[See event sources from a new menu](https://www.servicenow.com/docs/access?context=create-an-external-event-source&family=zurich&ft:locale=en-US)**

Create, read, update, or delete external event sources with the Event sources menu. An Event sources menu has been added to a panel of the spokes page that appears after you select a spoke under the **Integrations** tab.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Flows, subflows, and actions features or functionality were removed.

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

Between your current release family and Australia, some Flows, subflows, and actions features or functionality were deprecated.

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

The now.assist.creator role is no longer a required role to use generative AI features with Now Assist.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Flows, subflows, and actions.

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

Workflow Studio is a ServiceNow AI Platform feature that is active by default.

Get the latest Workflow Studio features by updating the app from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Flows, subflows, and actions we have noted them here.

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

If any specific browser requirements were introduced or changed for Flows, subflows, and actions we have noted them here.

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
</table>## Accessibility information

Review details on accessibility information for Flows, subflows, and actions, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Flows, subflows, and actions we have noted them here.

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

If there are specific highlight considerations for Flows, subflows, and actions we have noted them here.

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

-   Compare two flow histories to see what content was added, removed, and updated.
-   Summarize flow execution details to identify errors and suggest potential fixes.
-   Test conversation-enabled actions and subflows from a conversation.
-   Use an AI agent from a flow.

 See [Flows](https://www.servicenow.com/docs/access?context=exploring-flows&family=australia&ft:locale=en-US), [Explore subflows](https://www.servicenow.com/docs/access?context=exploring-subflows&family=australia&ft:locale=en-US), and [Explore actions](https://www.servicenow.com/docs/access?context=exploring-actions&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

