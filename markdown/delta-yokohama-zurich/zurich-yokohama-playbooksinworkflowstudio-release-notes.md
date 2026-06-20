---
title: Combined Playbooks in Workflow Studio release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Playbooks in Workflow Studio from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-playbooksinworkflowstudio-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Playbooks in Workflow Studio release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Playbooks in Workflow Studio from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Playbooks in Workflow Studio release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Playbooks in Workflow Studio to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

