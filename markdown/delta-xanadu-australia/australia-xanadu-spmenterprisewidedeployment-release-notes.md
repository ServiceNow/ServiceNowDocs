---
title: Combined SPM Enterprise-Wide Deployment release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for SPM Enterprise-Wide Deployment from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-spmenterprisewidedeployment-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined SPM Enterprise-Wide Deployment release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for SPM Enterprise-Wide Deployment from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family SPM Enterprise-Wide Deployment release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading SPM Enterprise-Wide Deployment to Australia

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

Between your current release family and Australia, new features were introduced for SPM Enterprise-Wide Deployment.

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

-   **[Partitions](https://www.servicenow.com/docs/access?context=create-partition-ewd&family=australia&ft:locale=en-US)**

Separate and control record visibility across functions using partitions.

    -   Create partitions for functions such as IT Operations, HR, and Finance using the EWD admin \(sn\_spm\_ewd.ewd\_admin\) role.
    -   Configure partition criteria using reference fields such as Department on the project, demand, program, and portfolio tables.
-   **[Supported tables and workspaces](https://www.servicenow.com/docs/access?context=supported-tables-for-partition-ewd&family=australia&ft:locale=en-US)**
    -   Partitioning is supported on the following primary tables and their related entities:

        -   Project \[pm\_project\]
        -   Demand \[dmn\_demand\]
        -   Program \[pm\_program\]
        -   Portfolio \[pm\_portfolio\]
Related entities such as cost plans, resource plans, and planning items automatically inherit the partition value from the parent record.

    -   Partition enforcement applies automatically at runtime across the following workspaces:
        -   Strategic Planning Workspace
        -   Portfolio Planning Workspace
        -   Project Workspace
        -   Resource Management Workspace
-   **[Assign PMO role for visibility across all partitions](https://www.servicenow.com/docs/access?context=assign-pmo-roles-for-visibility-across-all-partitions&family=australia&ft:locale=en-US)**

Assign the EWD PMO \(sn\_spm\_ewd.ewd\_pmo\) role to users or user groups who require visibility across all partitions, regardless of their assigned partition role. This role is intended for PMO users such as organization leads who require enterprise-wide visibility across all departments.

-   **[Update existing records with partition details scheduled job](https://www.servicenow.com/docs/access?context=update-partition-details-for-existing-records&family=australia&ft:locale=en-US)**

Populate partition details on records in the project, demand, program, portfolio, and planning item tables that were created before partition configuration was completed. Run this job only after completing partition configuration and assigning partition roles to users or user groups.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing SPM Enterprise-Wide Deployment features.

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
</table>## Removed

Between your current release family and Australia, some SPM Enterprise-Wide Deployment features or functionality were removed.

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

Between your current release family and Australia, some SPM Enterprise-Wide Deployment features or functionality were deprecated.

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

Review information on how to activate SPM Enterprise-Wide Deployment.

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

Install Enterprise-Wide Deployment by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for SPM Enterprise-Wide Deployment we have noted them here.

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

If any specific browser requirements were introduced or changed for SPM Enterprise-Wide Deployment we have noted them here.

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

Review details on accessibility information for SPM Enterprise-Wide Deployment, such as specific requirements or compliance levels.

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

If there are specific localization considerations for SPM Enterprise-Wide Deployment we have noted them here.

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

If there are specific highlight considerations for SPM Enterprise-Wide Deployment we have noted them here.

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

-   Separate and control record visibility across functions using partitions.
-   Enforce partition visibility automatically across Project Workspace, Portfolio Planning Workspace, Resource Management Workspace, and Strategic Planning Workspace.
-   Assign the EWD PMO role to users who require visibility across all partitions, such as PMO leads and portfolio managers.

 See [SPM Enterprise-Wide Deployment](https://www.servicenow.com/docs/access?context=ewd-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

