---
title: Combined Playbooks in Workflow Studio release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Playbooks in Workflow Studio from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-playbooksinworkflowstudio-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Playbooks in Workflow Studio release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Playbooks in Workflow Studio from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Playbooks in Workflow Studio release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Playbooks in Workflow Studio to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

After you upgrade to Xanadu, update the Playbooks and Workflow Studio applications in the ServiceNow Store.

</td></tr><tr><td>

Yokohama

</td><td>

After you upgrade to Yokohama, update the Workflow Studio application in the ServiceNow Store.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Playbooks in Workflow Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Variants](https://www.servicenow.com/docs/access?context=playbook-variants&family=xanadu&ft:locale=en-US)**

Use one playbook for multiple scenarios with variants.

-   **[Playbook recommendations](https://www.servicenow.com/docs/access?context=playbook-recommendations&family=xanadu&ft:locale=en-US)**

Get suggestions on which activities to replace placeholder activities with.

-   **[Re-prompt and preview](https://www.servicenow.com/docs/access?context=generate-a-playbook-outline&family=xanadu&ft:locale=en-US)**

Preview and modify your prompt before building your playbook.

-   **[Image to playbook generation](https://www.servicenow.com/docs/access?context=generate-a-playbook-outline&family=xanadu&ft:locale=en-US)**

Generate a playbook with out-of-the-box activities from text, an image, or both.

-   **[Questionnaire activity](https://www.servicenow.com/docs/access?context=questionnaire-activity&family=xanadu&ft:locale=en-US)**

Reference flow glide variable input and output values in an activity's condition builders to collect up to 10 pieces of information from an agent or fulfiller to use later during a playbook run, without requiring an existing table or fields.

-   **[Greater access controls](https://www.servicenow.com/docs/access?context=user-access-playbooks&family=xanadu&ft:locale=en-US)**

Better manage access to your playbooks and playbook components.

-   **[Archived data enhancements](https://www.servicenow.com/docs/access?context=archive-process-executions&family=xanadu&ft:locale=en-US)**

Schedule process execution data to be archived, and view the JSON files for your archived data.

-   **[Script support for activate, restart, deactivate, and duplicate](https://servicenow.com/docs/bundle/xanadu-release-notes/page/release-notes/now-platform-app-engine/api-rn.html)**

Use a script include or business rule that calls the activate, deactivate, restart, or duplicate playbook APIs.

-   **[Washington 25.2 release](https://servicenow.com/docs/bundle/washingtondc-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html)**

See 25.2 features in the [Washington DC Playbooks release notes](https://servicenow.com/docs/bundle/washingtondc-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html):

    -   Playbook Assist

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Translate playbooks content](https://www.servicenow.com/docs/access?context=add-translations-playbooks&family=yokohama&ft:locale=en-US)**

Add custom translations for labels, descriptions, and UI Layout properties in your playbooks.

-   **[Restart playbook activities that end in error](https://www.servicenow.com/docs/access?context=restart&family=yokohama&ft:locale=en-US)**

Configure activities so that end users can restart any activity that ends in an error.

-   **[Support for Retrieval Augmented Generation \(RAG\) with playbook generation](https://www.servicenow.com/docs/access?context=playbook-assist&family=yokohama&ft:locale=en-US)**

Generate playbooks from inputs that refer to custom actions, flows, subflows, content from installed spokes, or activity definitions. Include the names of commonly used and recently published actions, subflows, flows, and activity definitions available on your instance in your playbook generation requests.

-   **[Generate playbooks with the OpenAI GPT-4o LLM](https://www.servicenow.com/docs/access?context=change-default-llm-playbook-generation&family=yokohama&ft:locale=en-US)**

Use the OpenAI GPT-4o LLM to generate a playbook from text.

-   **[Add more fields in Create Task activities](https://www.servicenow.com/docs/access?context=create-task-activity&family=yokohama&ft:locale=en-US)**

Add more fields in a more configurable Create Task activity.

-   **[Create a checklist directly in Workflow Studio](https://www.servicenow.com/docs/access?context=checklist-task-activity&family=yokohama&ft:locale=en-US)**

Create a checklist directly in the side panel without needing a checklist template.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Playbooks in Workflow Studio features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Updated Roles](https://www.servicenow.com/docs/access?context=process-automation-designer-roles&family=xanadu&ft:locale=en-US)**

The pd\_admin role is now playbook.admin.

-   **Activities trigger asynchronously**

To avoid slowing down the playbook runs, the first activities are triggered asynchronously.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Change triggers in any playbook](https://www.servicenow.com/docs/access?context=duplicate-process&family=yokohama&ft:locale=en-US)**

Edit triggers when you duplicate a playbook, in a variant, etc.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Playbooks in Workflow Studio features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Use the Questionnaire activity instead of the Collect User Data activity.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Playbooks in Workflow Studio features or functionality were deprecated.

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

-   If you have the old Create Task activity in your existing playbooks, it will continue to function. You just can't add the extra fields that are available only in the new Create Task activity.
-   If you have the old Checklist activity in your existing playbooks, it will continue to function. You just won't be able to update the checklist directly in Workflow Studio the way that you can with the new Checklist activity.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Playbooks in Workflow Studio.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The application comes with the app in the Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the ServiceNow Store, as well as related applications like the Process Automation Experience Demo application.

 To use the playbook generation feature in Workflow Studio, download the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

The application comes with the application can be downloaded for patch fixes.Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the latest Workflow Studio app in the ServiceNow Store, as well as related applications like the Process Automation Content and Process Automation Experience Demo applications. The

 To use the playbook generation feature in Workflow Studio, download the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Playbooks in Workflow Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Playbooks in Workflow Studio we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Playbooks in Workflow Studio, such as specific requirements or compliance levels.

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Playbooks in Workflow Studio we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Playbook generation with images is not available in the APAC region.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

-   Use one playbook for multiple scenarios with variants.
-   Get recommendations on which activities to replace placeholder activities with.
-   Preview and modify your text directions before generating your playbook outline with Now Assist.
-   Generate a playbook with out-of-the-box activities from text, an image or both.
-   Collect custom responses from an end user, without requiring an existing table or fields.
-   Better manage access to your playbooks and playbook components.

 See [Exploring playbooks](https://www.servicenow.com/docs/access?context=process-automation-designer&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Add custom translations for playbooks.
-   Restart playbook activities that have ended in error.
-   Create a checklist directly in the side panel without needing a checklist template.
-   Generate a playbook via API in other ServiceNow applications such as IT Operations Management \(ITOM\).
-   Generate playbooks from inputs that refer to active actions, flows, subflows, content from installed spokes, or activity definitions.

 See [Exploring playbooks](https://www.servicenow.com/docs/access?context=process-automation-designer&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

