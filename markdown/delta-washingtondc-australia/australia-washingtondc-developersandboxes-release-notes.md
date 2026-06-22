---
title: Combined Developer Sandboxes release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Developer Sandboxes from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-developersandboxes-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Developer Sandboxes release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Developer Sandboxes from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Developer Sandboxes release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Developer Sandboxes to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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
</table>## New features

Between your current release family and Australia, new features were introduced for Developer Sandboxes.

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

-   **[Explore](https://www.servicenow.com/docs/access?context=exploring-sandboxes&family=zurich&ft:locale=en-US)**

View the total, available, and allocated sandboxes in your instance by using the Sandbox Management home dashboard. The dashboard also displays information about each sandbox, including the status, data utilization, owner, when the sandbox was last accessed, and when the sandbox was allocated.

-   **[Using sandbox templates](https://www.servicenow.com/docs/access?context=create-sandbox-template&family=zurich&ft:locale=en-US)**

Enable your delegated developers to reuse the data so that they can test their changes without manually inputting the data every time.

-   **[Create a Data Generation Profile](https://www.servicenow.com/docs/access?context=create-data-generation-profile&family=zurich&ft:locale=en-US)**

Enable your customers to generate the data for testing within the context of developer sandboxes, but also independently of sandboxes.

**Note:** Developer Sandboxes can't copy all the instance data. Data generation profiles enable a statistical sampling of data from selected tables with curated mappings to populate the sandbox with the data needed for building an application.

-   **[Allocate a sandbox](https://www.servicenow.com/docs/access?context=allocating-sandboxes&family=zurich&ft:locale=en-US)**

Allocate the sandboxes that were created to your development teams.

-   **[Retire sandboxes](https://www.servicenow.com/docs/access?context=retire-sandboxes&family=zurich&ft:locale=en-US)**

Retire outdated sandboxes to make room for the new sandboxes in your instance.

-   **[Automatically backed up update sets](https://www.servicenow.com/docs/access?context=dev-sbx-clone-upgrade-info&family=zurich&ft:locale=en-US)**

If you install Developer Sandboxes on an instance after Zurich Patch 5, update sets are automatically backed up when the instance is upgraded.


</td></tr><tr><td>

Australia

</td><td>

-   **[New granular roles for administration](https://www.servicenow.com/docs/access?context=dsb-installed-with&family=australia&ft:locale=en-US)**

Several new granular roles enable developers to complete administrative and configuration tasks without requiring the full admin role.

-   **[Support for separate indices for AI Search](https://www.servicenow.com/docs/access?context=exploring-sandboxes&family=australia&ft:locale=en-US)**

AI Search \(AIS\) now maintains separate indices for each sandbox environment, ensuring development activities that rely on AIS are correctly supported.

**Note:** The AIS integration with Developer Sandboxes is supported only on non-production environments.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Developer Sandboxes features.

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

-   **[Upgrade enhancements](https://www.servicenow.com/docs/access?context=dev-sbx-clone-upgrade-info&family=australia&ft:locale=en-US)**

After an upgrade, Developer Sandboxes now recreates the sandboxes on an instance and automatically backs up update sets to the base instance.

-   **[Queuing for successive sandbox creation](https://www.servicenow.com/docs/access?context=allocating-sandboxes&family=australia&ft:locale=en-US)**

To improve performance, Developer Sandboxes has implemented queuing when multiple sandboxes are created in succession.

-   **[SSO support for vanity URLs](https://www.servicenow.com/docs/access?context=dev-sbx-general-guidelines&family=australia&ft:locale=en-US)**

Instances with vanity URLs can now support Single Sign-On \(SSO\).

-   **[Schema change for shared tables isolates the table](https://www.servicenow.com/docs/access?context=dsb-installed-with&family=australia&ft:locale=en-US)**

To ensure configuration consistency, if you make a schema change, such as adding a column, to a shared table, the table now becomes an isolated table on the sandbox that initiated the schema change.

-   **[New vibe coding documentation](https://www.servicenow.com/docs/access?context=vibe-coding-landing&family=australia&ft:locale=en-US)**

Documentation is now available that introduces vibe coding, which is a natural language approach to application development in ServiceNow, including how to get started, when to use it, and how it fits within the broader suite of AI-powered development tools.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Developer Sandboxes features or functionality were removed.

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

Between your current release family and Australia, some Developer Sandboxes features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Developer Sandboxes.

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

Contact your ServiceNow account manager to install Developer Sandboxes.

</td></tr><tr><td>

Australia

</td><td>

Contact your ServiceNow account manager to install Developer Sandboxes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Developer Sandboxes we have noted them here.

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

If any specific browser requirements were introduced or changed for Developer Sandboxes we have noted them here.

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

Review details on accessibility information for Developer Sandboxes, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Developer Sandboxes we have noted them here.

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

If there are specific highlight considerations for Developer Sandboxes we have noted them here.

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

-   Enable your administrators and delegated developers to request, access, and manage the isolated development environments on top of the same underlying development instance.
-   Provide developer isolation and parallelism for customer development environments and instances.
-   View the total, available, and allocated sandboxes in your instance by using the Sandbox Management home dashboard. The dashboard also displays information about each sandbox, including the status, data utilization, owner, when it was last accessed, and when the sandbox was allocated.

 See [Developer Sandboxes](https://www.servicenow.com/docs/access?context=sandboxes-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Upgrading an instance recreates sandboxes and backs up any update sets.
-   A new plugin supports clone preservation when cloning an instance with sandboxes.

 See [Developer Sandboxes](https://www.servicenow.com/docs/access?context=sandboxes-landing&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

