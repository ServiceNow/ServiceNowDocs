---
title: Combined Regulatory Change Management release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Regulatory Change Management from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-regulatorychangemanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Regulatory Change Management release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Regulatory Change Management from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Regulatory Change Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Regulatory Change Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Regulatory Change Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Now Assist for Integrated Risk Management \(IRM\)](https://www.servicenow.com/docs/access?context=now-assist-for-irm-rn&family=zurich&ft:locale=en-US)**

You can review the Now Assist for Integrated Risk Management \(IRM\) release notes for full descriptions of the Now Assist in Regulatory Change Management \(RCM\) features.

-   **[Add multiple regulatory tasks](https://www.servicenow.com/docs/access?context=regulatory-change-tasks&family=zurich&ft:locale=en-US)**

Add multiple regulatory tasks to an alert. Each task can represent a distinct area of impact or required action. By organizing work into separate change tasks, your teams can assign responsibilities, track progress, and manage dependencies more effectively.

-   **[Add multiple source document import tasks](https://www.servicenow.com/docs/access?context=source-document-import-tasks&family=zurich&ft:locale=en-US)**

Associate multiple source document import tasks with one regulatory alert to simplify the management and tracking of your regulatory content ingestion. Each import task adds the relevant documents to the regulatory library to help ensure that all source materials that are related to the alert are accurately captured and organized. You can help to improve traceability throughout the regulatory change management process.

-   **[Close a regulatory task](https://www.servicenow.com/docs/access?context=regulatory-change-tasks&family=zurich&ft:locale=en-US)**

Close a regulatory task automatically when it's approved. You can also manually close a regulatory task while it's in the Implementation state, if all the associated action tasks are completed and closed. By closing a task manually, you get flexibility in managing the regulatory changes that don’t require formal approval workflows.

-   **[Reopen action tasks](https://www.servicenow.com/docs/access?context=action-tasks&family=zurich&ft:locale=en-US)**

Reopen the action tasks for a regulatory task when it's rejected and transitions back to the Implementation state. You can review and rework the tasks to address the feedback or incorporate the updated requirements. You can also modify and resubmit the reopened action tasks so that the implementation aligns with regulatory expectations before you resubmit the change task.

-   **[Close a regulatory alert](https://www.servicenow.com/docs/access?context=list-view-of-reg-alerts&family=zurich&ft:locale=en-US)**

Close a regulatory alert manually after all the associated regulatory tasks are complete. By closing the alert, you help to ensure accurate record-keeping by signaling that a compliance life-cycle for the specific regulatory alert is complete.

-   **[Work on action tasks](https://www.servicenow.com/docs/access?context=action-tasks&family=zurich&ft:locale=en-US)**

Initiate and complete the action tasks independently without requiring prior approval from users who are assigned with the `sn_grc_reg_change.manager` role. You can execute assigned responsibilities in a timely manner and reduce unnecessary approval bottlenecks. The access to action tasks remains governed by user permissions and role-based access controls to ensure proper accountability and oversight.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Regulatory Change Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Administrator role enhancements**

After upgrading to version 21.1.x, if you have a feature admin role you can now complete tasks that were initially reserved for users with the broader administrator role.

-   **Read-only field enhancements**

Starting with version 21.1.x, the following Regulatory Change Management plugins have security enhancements for read-only fields in this release:

    -   GRC: Taxonomy management \[com.sn\_grc\_taxonomy\]
    -   GRC: Regulatory Change Management integration with RSS Feeds \[com.sn\_grc\_rcm\_rssfeed\]
    -   GRC: Regulatory Change Management \[com.sn\_grc\_reg\_change\]
    -   GRC Case Management Core \[com.sn\_grc\_case\_mgmt\]
    -   GRC integration with Thomson Reuters Regulatory Intelligence \[com.sn\_grc\_int\_tr\]
    -   Regulatory Agency Library \[com.sn\_reg\_body\_mgmt\]
-   **[Tasks widget](https://www.servicenow.com/docs/access?context=list-view-of-reg-alerts&family=zurich&ft:locale=en-US)**

The overview page of a regulatory alert includes a newly added Tasks widget that enables you to get more visibility into related activities. This widget displays the total number of associated action tasks and change tasks that are linked to the specific regulatory alert. By using this widget, you can assess the level of effort that is required for compliance.

-   **[Workflow of regulatory task](https://www.servicenow.com/docs/access?context=reg-change-task&family=zurich&ft:locale=en-US)**

A regulatory task progresses through the following states:

    -   New
    -   Work In Progress
    -   Implementation
    -   Awaiting Approval \(optional\)
    -   Completed
While in the Implementation state, requesting approval is optional. If all associated action tasks are completed, the regulatory task can be closed directly from the Implementation state without requiring additional approval.

-   **[Workflow of source document import task](https://www.servicenow.com/docs/access?context=reg-change-task&family=zurich&ft:locale=en-US)**

A source document task progresses through the following states:

    -   New
    -   Ready to Import
    -   Work In Progress
    -   Implementation
    -   Completed.
-   **[Create action tasks](https://www.servicenow.com/docs/access?context=manage-reg-action-tasks&family=zurich&ft:locale=en-US)**

You can create action tasks for a regulatory task when the task is in any of the following states:

    -   New
    -   Work in Progress
    -   Implementation
You can now break down a regulatory task into smaller, manageable components so that you can more efficiently track and execute the required activities. You can plan, assign, and monitor tasks now in a structured manner that supports your compliance objectives and regulatory requirements.


</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Regulatory Change Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Regulatory Change Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Regulatory Change Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Regulatory Change Management and Now Assist for IRM by requesting them from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Regulatory Change Management and Now Assist for IRM by requesting them from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Regulatory Change Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Regulatory Change Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Regulatory Change Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Regulatory Change Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Regulatory Change Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Add multiple regulatory tasks or source document import tasks to a regulatory alert to manage the associated compliance activities efficiently. You can help to ensure that each task aligns with the regulatory requirements to maintain structured tracking and accountability.
-   Close a regulatory task during the Implementation state after you verify that all required actions and documentation are complete. You can also confirm that no pending activities remain before you close a task.
-   Change the workflow of a regulatory task to reflect the updated compliance procedures or organizational processes.
-   Create action tasks when a regulatory task is in the New, Work in Progress, or Implementation states to drive progress. You can also assign responsibilities to help ensure that the compliance actions are executed in a timely manner.
-   Close regulatory alerts manually when all associated tasks and compliance obligations have been successfully addressed. You can verify that each related item meets the closure criteria before confirming that the alert is resolved.

 See [Regulatory Change Management](https://www.servicenow.com/docs/access?context=reg-change-mgmt-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Early availability](https://www.servicenow.com/docs/access?context=australia-all-other-fixes&family=australia&ft:locale=en-US)

 Review the updated skill family name for Regulatory change management Now Assist skills.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

 Review the updated AI experience with three licensing tiers.

 See [Regulatory Change Management](https://www.servicenow.com/docs/access?context=reg-change-mgmt-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

