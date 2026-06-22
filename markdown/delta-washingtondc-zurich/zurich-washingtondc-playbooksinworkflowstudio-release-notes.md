---
title: Combined Playbooks in Workflow Studio release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Playbooks in Workflow Studio from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-playbooksinworkflowstudio-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Playbooks in Workflow Studio release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Playbooks in Workflow Studio from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Playbooks in Workflow Studio release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Playbooks in Workflow Studio to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

After you upgrade to Washington DC, update the Playbooks and Workflow Studio applications in the ServiceNow Store.

</td></tr><tr><td>

Xanadu

</td><td>

After you upgrade to Xanadu, update the Playbooks and Workflow Studio applications in the ServiceNow Store.

</td></tr><tr><td>

Yokohama

</td><td>

After you upgrade to Yokohama, update the Workflow Studio application in the ServiceNow Store.

</td></tr><tr><td>

Zurich

</td><td>

After you upgrade to Zurich, update the Workflow Studio application in the ServiceNow Store.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Playbooks in Workflow Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Workflow Studio](https://servicenow-staging.fluidtopics.net/access?context=workflow-studio&family=washingtondc&ft:locale=en-US)**

Build and manage playbooks, flows, subflows, actions, and decisions from a shared access point.

-   **[Restart](https://servicenow-staging.fluidtopics.net/access?context=restart&family=washingtondc&ft:locale=en-US)**

Restart your entire playbook, or restart from a specific activity or stage.

-   **[Role for canceling a process](https://servicenow-staging.fluidtopics.net/access?context=process-automation-designer-roles&family=washingtondc&ft:locale=en-US)**

Admins can grant users a new role that allows them to cancel running playbooks without the pd\_admin role or write access to the parent record.

-   **[Run activity as a specific user](https://servicenow-staging.fluidtopics.net/access?context=process-automation-designer-roles&family=washingtondc&ft:locale=en-US)**

Use the [**Run As** property](https://servicenow-staging.fluidtopics.net/access?context=flow-roles&family=washingtondc&ft:locale=en-US) to determine the role that runs an activity.

-   **[Dynamic Inputs](https://servicenow-staging.fluidtopics.net/access?context=add-dynamic-inputs-to-activity&family=washingtondc&ft:locale=en-US)**

Use dynamic inputs to return variables in your activities for use cases such as submitting a catalog request.

-   **[Automation assets](https://servicenow-staging.fluidtopics.net/access?context=automation-assets&family=washingtondc&ft:locale=en-US)**

For automation-only activities, add a subflow, flow, or action directly to your activity instead of creating an activity definition.

-   **[Form views enhancement](https://servicenow-staging.fluidtopics.net/access?context=user-form-activity&family=washingtondc&ft:locale=en-US)**

View and modify form views with Form Builder in a new Workflow Studio tab.

-   **[Playbook Assist](https://servicenow-staging.fluidtopics.net/access?context=playbook-assist-landing&family=washingtondc&ft:locale=en-US)**

Starting in release 25.2, provide text directions to generate a playbook outline with placeholder activities.

-   **Vancouver 24.2 release**

See 24.2 features in the [Vancouver Playbooks release notes](https://servicenow.com/docs/bundle/vancouver-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html):

    -   [Decision activities](https://servicenow-staging.fluidtopics.net/access?context=create-process-definition&family=washingtondc&ft:locale=en-US)
    -   [Archive processes](https://servicenow-staging.fluidtopics.net/access?context=archive-process-executions&family=washingtondc&ft:locale=en-US)
    -   [Field picker](https://servicenow-staging.fluidtopics.net/access?context=process-automation-designer-lanes-activities&family=washingtondc&ft:locale=en-US)

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Variants](https://servicenow-staging.fluidtopics.net/access?context=playbook-variants&family=xanadu&ft:locale=en-US)**

Use one playbook for multiple scenarios with variants.

-   **[Playbook recommendations](https://servicenow-staging.fluidtopics.net/access?context=playbook-recommendations&family=xanadu&ft:locale=en-US)**

Get suggestions on which activities to replace placeholder activities with.

-   **[Re-prompt and preview](https://servicenow-staging.fluidtopics.net/access?context=generate-a-playbook-outline&family=xanadu&ft:locale=en-US)**

Preview and modify your prompt before building your playbook.

-   **[Image to playbook generation](https://servicenow-staging.fluidtopics.net/access?context=generate-a-playbook-outline&family=xanadu&ft:locale=en-US)**

Generate a playbook with out-of-the-box activities from text, an image, or both.

-   **[Questionnaire activity](https://servicenow-staging.fluidtopics.net/access?context=questionnaire-activity&family=xanadu&ft:locale=en-US)**

Reference flow glide variable input and output values in an activity's condition builders to collect up to 10 pieces of information from an agent or fulfiller to use later during a playbook run, without requiring an existing table or fields.

-   **[Greater access controls](https://servicenow-staging.fluidtopics.net/access?context=user-access-playbooks&family=xanadu&ft:locale=en-US)**

Better manage access to your playbooks and playbook components.

-   **[Archived data enhancements](https://servicenow-staging.fluidtopics.net/access?context=archive-process-executions&family=xanadu&ft:locale=en-US)**

Schedule process execution data to be archived, and view the JSON files for your archived data.

-   **[Script support for activate, restart, deactivate, and duplicate](https://servicenow.com/docs/bundle/xanadu-release-notes/page/release-notes/now-platform-app-engine/api-rn.html)**

Use a script include or business rule that calls the activate, deactivate, restart, or duplicate playbook APIs.

-   **[Washington 25.2 release](https://servicenow.com/docs/bundle/washingtondc-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html)**

See 25.2 features in the [Washington DC Playbooks release notes](https://servicenow.com/docs/bundle/washingtondc-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html):

    -   Playbook Assist

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Translate playbooks content](https://servicenow-staging.fluidtopics.net/access?context=add-translations-playbooks&family=yokohama&ft:locale=en-US)**

Add custom translations for labels, descriptions, and UI Layout properties in your playbooks.

-   **[Restart playbook activities that end in error](https://servicenow-staging.fluidtopics.net/access?context=restart&family=yokohama&ft:locale=en-US)**

Configure activities so that end users can restart any activity that ends in an error.

-   **[Support for Retrieval Augmented Generation \(RAG\) with playbook generation](https://servicenow-staging.fluidtopics.net/access?context=playbook-assist&family=yokohama&ft:locale=en-US)**

Generate playbooks from inputs that refer to custom actions, flows, subflows, content from installed spokes, or activity definitions. Include the names of commonly used and recently published actions, subflows, flows, and activity definitions available on your instance in your playbook generation requests.

-   **[Generate playbooks with the OpenAI GPT-4o LLM](https://servicenow-staging.fluidtopics.net/access?context=change-default-llm-playbook-generation&family=yokohama&ft:locale=en-US)**

Use the OpenAI GPT-4o LLM to generate a playbook from text.

-   **[Add more fields in Create Task activities](https://servicenow-staging.fluidtopics.net/access?context=create-task-activity&family=yokohama&ft:locale=en-US)**

Add more fields in a more configurable Create Task activity.

-   **[Create a checklist directly in Workflow Studio](https://servicenow-staging.fluidtopics.net/access?context=checklist-task-activity&family=yokohama&ft:locale=en-US)**

Create a checklist directly in the side panel without needing a checklist template.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Set child variants to evaluate later in a playbook](https://servicenow-staging.fluidtopics.net/access?context=set-evaluation-point&family=zurich&ft:locale=en-US)**

Instead of evaluating immediately after the trigger, set a playbook's child variants to be evaluated after a specific activity in the playbook.

-   **[Agentic Playbooks](https://servicenow-staging.fluidtopics.net/access?context=agentic-playbooks&family=zurich&ft:locale=en-US)**

Enable AI agents to assist users with activities during runtime.

-   **[Add permissions for playbook authors](https://servicenow-staging.fluidtopics.net/access?context=user-access-playbooks&family=zurich&ft:locale=en-US)**

Control which playbook authors can create, edit, and view playbooks in Workflow Studio

-   **[Add permissions for runtime users](https://servicenow-staging.fluidtopics.net/access?context=create-process-definition&family=zurich&ft:locale=en-US)**

Control whether runtime users can [view a playbook](https://servicenow-staging.fluidtopics.net/access?context=create-process-definition&family=zurich&ft:locale=en-US), [add optional activities](https://servicenow-staging.fluidtopics.net/access?context=optional-activities&family=zurich&ft:locale=en-US), [restart a playbook](https://servicenow-staging.fluidtopics.net/access?context=restart&family=zurich&ft:locale=en-US), and [complete work within specific stages](https://servicenow-staging.fluidtopics.net/access?context=add-configure-stage&family=zurich&ft:locale=en-US).

-   **[Create decision branches for stages](https://servicenow-staging.fluidtopics.net/access?context=create-decision-stage&family=zurich&ft:locale=en-US)**

Add a decision node between stages to determine which stage to run next, based on runtime conditions.

-   **[Set multiple triggers](https://servicenow-staging.fluidtopics.net/access?context=process-automation-designer-triggers&family=zurich&ft:locale=en-US)**

Configure a playbook to run based on any one of multiple triggers.

-   **[Schedule when a playbook should trigger](https://servicenow-staging.fluidtopics.net/access?context=create-scheduled-trigger-definition&family=zurich&ft:locale=en-US)**

Configure a playbook to run based on a schedule.

-   **[Choose your LLM for playbook generation and recommendations](https://servicenow-staging.fluidtopics.net/access?context=change-default-llm-playbook-generation&family=zurich&ft:locale=en-US)**

Choose between NowLLM, OpenAI ChatGPT4-o, Gemini, Claude for playbook generation and recommendations.

-   **[Route users to stages based on decisions](https://servicenow-staging.fluidtopics.net/access?context=add-configure-stage&family=zurich&ft:locale=en-US)**

Send runtime users to a stage based off of the trigger record or input that users provide.

-   **[Yokohama 27.2 and 27.3 releases](https://servicenow.com/docs/bundle/yokohama-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html)**

See 27.2 and 27.3 features in the [Yokohama Playbooks release notes](https://servicenow.com/docs/bundle/yokohama-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html):

    -   [Generate a playbook with the OpenAI GPT-4o LLM](https://servicenow-staging.fluidtopics.net/access?context=generate-a-playbook-outline&family=zurich&ft:locale=en-US)
    -   [Retrieval Augmented Generation \(RAG\) for playbooks](https://servicenow-staging.fluidtopics.net/access?context=playbook-assist&family=zurich&ft:locale=en-US)

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Playbooks in Workflow Studio features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **Faster loading times**

Starting in release 25.2, playbooks are loading faster.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Updated Roles](https://servicenow-staging.fluidtopics.net/access?context=process-automation-designer-roles&family=xanadu&ft:locale=en-US)**

The pd\_admin role is now playbook.admin.

-   **Activities trigger asynchronously**

To avoid slowing down the playbook runs, the first activities are triggered asynchronously.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Change triggers in any playbook](https://servicenow-staging.fluidtopics.net/access?context=duplicate-process&family=yokohama&ft:locale=en-US)**

Edit triggers when you duplicate a playbook, in a variant, etc.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Activate playbooks without a trigger](https://servicenow-staging.fluidtopics.net/access?context=process-automation-designer-triggers&family=zurich&ft:locale=en-US)**

Configure and activate playbooks without specifying triggers, so that playbooks are only triggered programmatically.

-   **[Implement playbooks that are callable by a scriptable API](https://servicenow-staging.fluidtopics.net/access?context=process-automation-designer-triggers&family=zurich&ft:locale=en-US)**

Configure a playbook that executes with an input object instead of requiring the configuration of a trigger record reference and trigger conditions.

-   **[Decision activity enhancements](https://servicenow-staging.fluidtopics.net/access?context=create-a-decision-activity&family=zurich&ft:locale=en-US)**

User experience improvements to decision activities:

    -   In the Board view, select the branch or Start rule icon on a decision activity card to see a list of dependent activities and branches, and to navigate to them.
    -   When a decision or one of its branch nodes is selected in Diagram view, the decision and all of its branches are selected, and the side panel opens.
    -   Add parallel activities within decision branches.
-   **[Enter a combination of pills and text in an email body](https://servicenow-staging.fluidtopics.net/access?context=add-configure-activity&family=zurich&ft:locale=en-US)**

Enter a combination of text and multiple pills in any rich text / HTML editor container, such as an email body.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Playbooks in Workflow Studio features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   The trigger license requirement has been removed, allowing you to use any entitled table to trigger a playbook.

</td></tr><tr><td>

Xanadu

</td><td>

Use the Questionnaire activity instead of the Collect User Data activity.

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

Between your current release family and Zurich, some Playbooks in Workflow Studio features or functionality were deprecated.

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

-   If you have the old Create Task activity in your existing playbooks, it will continue to function. You just can't add the extra fields that are available only in the new Create Task activity.
-   If you have the old Checklist activity in your existing playbooks, it will continue to function. You just won't be able to update the checklist directly in Workflow Studio the way that you can with the new Checklist activity.

</td></tr><tr><td>

Zurich

</td><td>

-   now.assist.creator role

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Playbooks in Workflow Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

While the interface lives in app in the Workflow Studio, they are separate ServiceNow Store apps. Workflow Studio is part of the ServiceNow AI Platform® and available by default. Get the latest playbooks functionality by downloading the ServiceNow Store.

 To use the playbook generation feature in 25.2 release, and download the Workflow Studio, upgrade to the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

The application comes with the app in the Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the ServiceNow Store, as well as related applications like the Process Automation Experience Demo application.

 To use the playbook generation feature in Workflow Studio, download the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

The application comes with the application can be downloaded for patch fixes.Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the latest Workflow Studio app in the ServiceNow Store, as well as related applications like the Process Automation Content and Process Automation Experience Demo applications. The

 To use the playbook generation feature in Workflow Studio, download the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

The application comes with the application can be downloaded for patch fixes.Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the latest Workflow Studio app in the ServiceNow Store, as well as related applications like the Process Automation Content and Process Automation Experience Demo applications. The

 To use the playbook generation feature in Workflow Studio, download the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Playbooks in Workflow Studio we have noted them here.

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

The following features are part of the ServiceNow AI Platform® and are active by default:

-   Archived data enhancements
-   Script support for activate, restart, and deactivate
-   Updated roles
-   Greater access controls

 Download the app in the ServiceNow Store to access the following features:

-   Variants
-   Questionnaire activity
-   Playbook Recommendations
-   Re-prompt and preview

 For access to all app in the store.Xanadu features, download the latest

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Download the latest Workflow Studio app in the ServiceNow Store to access the newest features.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Playbooks in Workflow Studio we have noted them here.

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
</table>## Accessibility information

Review details on accessibility information for Playbooks in Workflow Studio, such as specific requirements or compliance levels.

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

-   In Diagram view, navigate between and configure stages and activities [via keyboard](https://servicenow-staging.fluidtopics.net/access?context=keyboard-navigation-in-playbook-diagram-view&family=zurich&ft:locale=en-US).
-   Set the action bar to always show in Diagram view. To learn more, see [View all buttons without hover](https://servicenow-staging.fluidtopics.net/access?context=view-all-buttons-without-hover&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Playbooks in Workflow Studio we have noted them here.

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

Playbook generation with images is not available in the APAC region.

</td></tr><tr><td>

Yokohama

</td><td>

Using OpenAI LLMs for playbook generation is not available in the APAC region.

</td></tr><tr><td>

Zurich

</td><td>

Using OpenAI LLMs for playbook generation is not available in the APAC region.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Playbooks in Workflow Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Processes are now called Playbooks in both the builder and in Playbook Experience.
-   Open the Playbooks builder in [Workflow Studio](https://servicenow-staging.fluidtopics.net/access?context=workflow-studio&family=washingtondc&ft:locale=en-US). Workflow Studio enables workflow owners to author, configure, and monitor playbooks, flows, subflows, actions, and decision tables in one place.
-   [Restart](https://servicenow-staging.fluidtopics.net/access?context=restart&family=washingtondc&ft:locale=en-US) your entire playbook, or restart from a specific activity or stage.
-   Use [dynamic inputs](https://servicenow-staging.fluidtopics.net/access?context=add-dynamic-inputs-to-activity&family=washingtondc&ft:locale=en-US) to configure your activity to show a certain set of fields based on the value of another input, such as a selected catalog item, selected decision table, or a REST API response.
-   Trigger a playbook from any entitled table. For more information, see the [Removed from this release](https://servicenow-staging.fluidtopics.net/access?context=process-automation-designer-rn&family=washingtondc&ft:locale=en-US) section.
-   As of release 25.2, use generative AI to create [playbook](https://servicenow-staging.fluidtopics.net/access?context=playbook-assist-landing&family=washingtondc&ft:locale=en-US) outlines.

 See [Exploring Process Automation Designer](https://servicenow-staging.fluidtopics.net/access?context=process-automation-designer&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Use one playbook for multiple scenarios with variants.
-   Get recommendations on which activities to replace placeholder activities with.
-   Preview and modify your text directions before generating your playbook outline with Now Assist.
-   Generate a playbook with out-of-the-box activities from text, an image or both.
-   Collect custom responses from an end user, without requiring an existing table or fields.
-   Better manage access to your playbooks and playbook components.

 See [Exploring playbooks](https://servicenow-staging.fluidtopics.net/access?context=process-automation-designer&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Add custom translations for playbooks.
-   Restart playbook activities that have ended in error.
-   Create a checklist directly in the side panel without needing a checklist template.
-   Generate a playbook via API in other ServiceNow applications such as IT Operations Management \(ITOM\).
-   Generate playbooks from inputs that refer to active actions, flows, subflows, content from installed spokes, or activity definitions.

 See [Exploring playbooks](https://servicenow-staging.fluidtopics.net/access?context=process-automation-designer&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Add permissions for playbook authors and runtime users.
-   Activate a playbook without a trigger. Set multiple potential triggers for a playbook, or trigger a playbook on a schedule.
-   Enable AI agents to complete activities without human intervention during runtime.
-   Set child variants to evaluate later in a playbook.
-   Create decision branches for stages.

 See [Playbooks](https://servicenow-staging.fluidtopics.net/access?context=process-automation-designer&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

