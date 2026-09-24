---
title: Combined Case management for CSM release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Case management for CSM from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-casemanagementforcsm-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Case management for CSM release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Case management for CSM from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Case management for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Case management for CSM to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Case management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[\[Placeholder link text to key add-dependencies-between-template-item\]](https://www.servicenow.com/docs/access?context=add-dependencies-between-template-item&family=australia&ft:locale=en-US)**

Create and manage dependencies between template items using the supported dependency types. Users can apply a template at any time after the template is published. Validate dependencies using built‑in checks \(including circular dependency validation\) to help prevent invalid dependency definitions.

The following dependency types are supported:

    -   Finish to- start: the successor task starts when the predecessor task is completed.
    -   Start after start: the successor task starts when the predecessor task is started.
    -   Start together: both tasks start at the same time.
-   **[\[Placeholder link text to key share-a-task-plan-template-from-the-workspace\]](https://www.servicenow.com/docs/access?context=share-a-task-plan-template-from-the-workspace&family=australia&ft:locale=en-US)**

Provide a visual governance experience to define and manage user access enabling business process owners to configure relationships with clarity.


 -   **[Task dependencies for task plan templates](https://www.servicenow.com/docs/access?context=task-dependencies-for-task-plan-templates&family=australia&ft:locale=en-US)**

Define dependency relationships between template items in the \[sn\_task\_plan\_template\_dependency\] table, and upon applying the template, create and store the resulting task dependencies in the \[sn\_task\_dependency\_m2m\] table to ensure controlled task sequencing through predecessor–successor relationships.

-   **[Document References in Task Plan Templates](https://www.servicenow.com/docs/access?context=adding-and-managing-document-references-in-task-plan-templates&family=australia&ft:locale=en-US)**

Add documents to Task Plan Template items, storing document references in the \[sn\_task\_plan\_template\_document\] table and making them accessible through form views and related lists based on template state and user permissions, ensuring secure and controlled document access aligned with template‑level permissions


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Case management for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Manager Workspace landing page](https://www.servicenow.com/docs/access?context=csm-configurable-manager-workspace-dashboards-new&family=australia&ft:locale=en-US)**

The following UI components have been added in the Task Plan Template table:

    -   The Template Dependencies tab displays a node‑map view of dependencies between template items in saved task plan template records. Each dependency appears as a labeled edge between nodes, indicating its type \(Finish to start, Start after start\) or Start together\). Select Edge to edit or delete the dependency, based on your role.
    -   The Share Plan modal in the task plan template workspace includes three views; **Share Plan**, **Success**, and **Manage Access**, for configuring, confirming, and managing access to a task plan template, with a search bar, Select all option, and Currently shared with list in the Share Plan view.

 -   **[Granular viewer roles for Case Management](https://www.servicenow.com/docs/access?context=customer-service-management-roles&family=australia&ft:locale=en-US)**

Added new read-only roles within Case Management. These include the following:

    -   Customer Service All Case Viewer \[sn\_customerservice.all\_cases\_viewer\]
    -   Case Playbook for Complaint Viewer \[sn\_complaint.viewer\]
    -   Case Playbook for Onboarding Viewer \[sn\_onboarding.viewer\]
    -   Action Status Viewer \[sn\_action\_status.viewer\]
    -   Customer Service Document Template Viewer \[sn\_csm\_doctemplate.viewer\]
    -   Case Digest Viewer \[sn\_csm\_case\_digest.viewer\]
    -   Customer Project Management Viewer \[sn\_csm\_ppm.viewer\]
    -   Case Type Configuration Viewer \[sn\_scm\_case\_type.config\_viewer\]
    -   Case Line Viewer \[sn\_case\_line.viewer\]
-   **[Major Issue Management](https://www.servicenow.com/docs/access?context=major-issue-management&family=australia&ft:locale=en-US)**

Case Type consistency improvements: This update ensures case type consistency when creating and managing major cases and their related child cases, improving accuracy and reducing manual correction.

    -   Create major cases automatically upon approval, and major cases now inherit the same case type as the originating case.
    -   Promote the proposed case directly to a major case I-if no account or consumer or partner exists on the originating major case.
    -   Use the major case's case type and inherit the fields defined in \(sn\_customerservice.case\_fields\_to\_sync\) property or defined through extension point for child cases.
-   **[Task plan templates](https://www.servicenow.com/docs/access?context=task-plan-templates&family=australia&ft:locale=en-US)**

Add flexible task dependency management to task plan templates, and support for attachments.

    -   Schedule offsets can be defined when creating dependencies, allowing tasks to start within a specified time period \(minutes, hours, days, or weeks\).
    -   Configure and manage task dependencies directly from task dependency list and view layouts.
    -   Built‑in validations prevent circular dependencies, ensuring task plans remain accurate and reliable.
    -   Ability to attach documents to tasks or cases.
    -   Select **Apply Template** for any published task plan templates to automatically add all document references from the original template items to the newly created tasks, ensuring seamless access for task owners to all required documents.
-   **[Case type selector for creating cases](https://www.servicenow.com/docs/access?context=create-case-of-specific-case-type&family=australia&ft:locale=en-US)**

The case type selector is now activated by default when creating cases of these types:

    -   Interaction
    -   Account
    -   Contact
    -   Consumer
    -   Sold product
    -   Install base item
    -   Related lists: child case, case task
    -   List view
    -   Case task list view

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Case management for CSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Case management for CSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Case management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Case management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Case management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Case management for CSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Case management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Case management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Add dependencies between task plan template items to define predecessor–successor relationships using the supported dependency types: Finish to start, Start after start, and Start together
-   Provide a visual governance experience to define and manage user access enabling business process owners to configure relationships with clarity.
-   Major cases now have the same case type as the original case, and associated child cases also have the same case type.
-   Enhancements to task plan templates to support task dependency, and to support document attachments in task plan template items.
-   Migrating several applications from family to store.

 See [Case management](https://www.servicenow.com/docs/access?context=csm-case-management&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

