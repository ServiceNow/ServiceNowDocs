---
title: Combined Digital Product Release release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Digital Product Release from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-digitalproductrelease-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Digital Product Release release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Digital Product Release from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Digital Product Release release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Digital Product Release to Brazil

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

Between your current release family and Brazil, new features were introduced for Digital Product Release.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Restricted access to releases](https://www.servicenow.com/docs/access?context=dpr-product-release&family=australia&ft:locale=en-US)**

Limit who can see a release to its release team. Restricted access adds record-level control and applies to releases, release phases, release tasks, policy mappings, key dates, and release phase relationships.

Configure a product team on the Product Settings page to apply restricted access on its releases. For more information, see [Configure product-level release settings](https://www.servicenow.com/docs/access?context=dpr-config-product-release-setting&family=australia&ft:locale=en-US).

A release created for a restricted-access product inherits its setting, and the product team is set to its initial release team.

In a multi-product release, individual releases inherit access control from the main release.

-   **[On hold release state](https://www.servicenow.com/docs/access?context=dpr-hold-resume-release&family=australia&ft:locale=en-US)**

Pause a release for a business reason without cancelling it or losing its place in the release life cycle. While a release is on hold, you can't complete the current phase and automatic phase progression does not run. Resume the release after the reason for the hold is resolved, or cancel it.

-   **[Planned and actual phase dates in stage-based release](https://www.servicenow.com/docs/access?context=dpr-work-stage-release&family=australia&ft:locale=en-US)**

Track planned and actual start and end dates for stage-based release phases. You enter the planned dates; the actual dates are set automatically as the phase progresses.

-   **[System properties for the default phase association](https://www.servicenow.com/docs/access?context=digital-product-release-properties&family=australia&ft:locale=en-US)**

Control which phase is pre-selected when you associate a change or configuration item with a release. Configure **sn\_dpr.default\_phase\_for\_changes** for changes and **sn\_dpr.default\_phase\_for\_cis** for configuration items.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Restricted access to releases](https://www.servicenow.com/docs/access?context=dpr-product-release&family=brazil&ft:locale=en-US)**

Limit who can see a release to its release team. Restricted access adds record-level control and applies to releases, release phases, release tasks, policy mappings, key dates, and release phase relationships.

Configure a product team on the Product Settings page to apply restricted access on its releases. For more information, see [Configure product-level release settings](https://www.servicenow.com/docs/access?context=dpr-config-product-release-setting&family=brazil&ft:locale=en-US).

A release created for a restricted-access product inherits its setting, and the product team is set to its initial release team.

In a multi-product release, individual releases inherit access control from the main release.

-   **[On hold release state](https://www.servicenow.com/docs/access?context=dpr-hold-resume-release&family=brazil&ft:locale=en-US)**

Pause a release for a business reason without cancelling it or losing its place in the release life cycle. While a release is on hold, you can't complete the current phase and automatic phase progression does not run. Resume the release after the reason for the hold is resolved, or cancel it.

-   **[Planned and actual phase dates in stage-based release](https://www.servicenow.com/docs/access?context=dpr-work-stage-release&family=brazil&ft:locale=en-US)**

Track planned and actual start and end dates for stage-based release phases. You enter the planned dates; the actual dates are set automatically as the phase progresses.

-   **[System properties for the default phase association](https://www.servicenow.com/docs/access?context=digital-product-release-properties&family=brazil&ft:locale=en-US)**

Control which phase is pre-selected when you associate a change or configuration item with a release. Configure **sn\_dpr.default\_phase\_for\_changes** for changes and **sn\_dpr.default\_phase\_for\_cis** for configuration items.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Digital Product Release features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Charts exclude cancelled phases from the release dashboards](https://www.servicenow.com/docs/access?context=dpr-dashboard-release&family=australia&ft:locale=en-US)**

Policies, phase tasks, and task approvals attached to a cancelled or restarted release phase are excluded from chart aggregates. They are also filtered out from the lists that opens on selecting a chart segment. This applies to the Digital Product Release landing page, Release Overview, Release Bundle Details, and the multi-product release dashboard.

-   **[Digital Product Release home page widgets scoped to your releases](https://www.servicenow.com/docs/access?context=dpr-workspace&family=australia&ft:locale=en-US)**

The **My releases** chart on the Digital Product Release Workspace home page shows only releases where you're the release owner or a release team member.

-   **[Release actions on all release pages](https://www.servicenow.com/docs/access?context=dpr-manage-releases&family=australia&ft:locale=en-US)**

From any release page, perform actions such as **Start release**, **Re-target release**, **Close release**, **Complete current phase**, and **Run policies**.

-   **[Release template](https://www.servicenow.com/docs/access?context=dpr-create-release-template&family=australia&ft:locale=en-US)**

The **Manage release template** button on the Release template form is renamed **Edit release template**.

-   **[Release creation wizard](https://www.servicenow.com/docs/access?context=dpr-create-release-guided&family=australia&ft:locale=en-US)**

Additional Products fields are no longer required in the Create release flow.

-   **[Policy status aggregation](https://www.servicenow.com/docs/access?context=dpr-policy-status-aggregation&family=australia&ft:locale=en-US)**

In a multi-product release, the policy status of a product added after the release starts rolls up to the main release.

-   **[Product enhancement creation](https://www.servicenow.com/docs/access?context=dpr-add-product-enhancement-from-epic&family=australia&ft:locale=en-US)**

The **sn\_dpr\_workspace.enhancement\_work\_item\_types** system property controls which work item types auto-create product enhancements. Leave it empty to stop enhancement creation.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Charts exclude cancelled phases from the release dashboards](https://www.servicenow.com/docs/access?context=dpr-dashboard-release&family=brazil&ft:locale=en-US)**

Policies, phase tasks, and task approvals attached to a cancelled or restarted release phase are excluded from chart aggregates. They are also filtered out from the lists that opens on selecting a chart segment. This applies to the Digital Product Release landing page, Release Overview, Release Bundle Details, and the multi-product release dashboard.

-   **[Digital Product Release home page widgets scoped to your releases](https://www.servicenow.com/docs/access?context=dpr-workspace&family=brazil&ft:locale=en-US)**

The **My releases** chart on the Digital Product Release Workspace home page shows only releases where you're the release owner or a release team member.

-   **[Release actions on all release pages](https://www.servicenow.com/docs/access?context=dpr-manage-releases&family=brazil&ft:locale=en-US)**

From any release page, perform actions such as **Start release**, **Re-target release**, **Close release**, **Complete current phase**, and **Run policies**.

-   **[Release template](https://www.servicenow.com/docs/access?context=dpr-create-release-template&family=brazil&ft:locale=en-US)**

The **Manage release template** button on the Release template form is renamed **Edit release template**.

-   **[Release creation wizard](https://www.servicenow.com/docs/access?context=dpr-create-release-guided&family=brazil&ft:locale=en-US)**

Additional Products fields are no longer required in the Create release flow.

-   **[Policy status aggregation](https://www.servicenow.com/docs/access?context=dpr-policy-status-aggregation&family=brazil&ft:locale=en-US)**

In a multi-product release, the policy status of a product added after the release starts rolls up to the main release.

-   **[Product enhancement creation](https://www.servicenow.com/docs/access?context=dpr-add-product-enhancement-from-epic&family=brazil&ft:locale=en-US)**

The **sn\_dpr\_workspace.enhancement\_work\_item\_types** system property controls which work item types auto-create product enhancements. Leave it empty to stop enhancement creation.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Digital Product Release features or functionality were removed.

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

Between your current release family and Brazil, some Digital Product Release features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Auto create enhancement from primary epic system property](https://www.servicenow.com/docs/access?context=digital-product-release-properties&family=australia&ft:locale=en-US)**

The `sn_dpr_workspace.auto_create_product_enhancement_for_primary_epic` property is removed. Use `sn_dpr_workspace.enhancement_work_item_types` instead.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Auto create enhancement from primary epic system property](https://www.servicenow.com/docs/access?context=digital-product-release-properties&family=brazil&ft:locale=en-US)**

The `sn_dpr_workspace.auto_create_product_enhancement_for_primary_epic` property is removed. Use `sn_dpr_workspace.enhancement_work_item_types` instead.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Digital Product Release.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install Digital Product Release by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

For more information, see [Install Digital Product Release](https://www.servicenow.com/docs/access?context=install-digital-product-release&family=australia&ft:locale=en-US).


**Note:** Digital Product Release is available from the ServiceNow Store. See the activation information that follows.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Digital Product Release by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).

For more information, see [Install Digital Product Release](https://www.servicenow.com/docs/access?context=install-digital-product-release&family=brazil&ft:locale=en-US).


**Note:** Digital Product Release is available from the ServiceNow Store. See the activation information that follows.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Digital Product Release we have noted them here.

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

If any specific browser requirements were introduced or changed for Digital Product Release we have noted them here.

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

Review details on accessibility information for Digital Product Release, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Digital Product Release we have noted them here.

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

If there are specific highlight considerations for Digital Product Release we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Plan, validate, and track product releases in one workspace, so product teams share a single view of release readiness.
-   Gate release progression with policies that evaluate data from the AI Platform and from connected planning and CI/CD tools.
-   Restrict release visibility to the teams that own a release, and inherit that access down to release phases, phase tasks, and linked records.
-   Hand a validated release to Change Management, so change approval focuses on deployment scheduling and service impact.

 For more information, see [Digital Product Release](https://www.servicenow.com/docs/access?context=dpr-landing-page&family=australia&ft:locale=en-US).

</td></tr><tr><td>

Brazil

</td><td>

-   Plan, validate, and track product releases in one workspace, so product teams share a single view of release readiness.
-   Gate release progression with policies that evaluate data from the AI Platform and from connected planning and CI/CD tools.
-   Restrict release visibility to the teams that own a release, and inherit that access down to release phases, phase tasks, and linked records.
-   Hand a validated release to Change Management, so change approval focuses on deployment scheduling and service impact.

 For more information, see [Digital Product Release](https://www.servicenow.com/docs/access?context=dpr-landing-page&family=brazil&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

