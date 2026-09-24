---
title: Combined Developer Sandboxes release notes for upgrades from Yokohama to Brazil
description: Consolidated page of all release notes for Developer Sandboxes from Yokohama to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-brazil/brazil-yokohama-developersandboxes-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Developer Sandboxes release notes for upgrades from Yokohama to Brazil

Consolidated page of all release notes for Developer Sandboxes from Yokohama to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Developer Sandboxes release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Developer Sandboxes to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Developer Sandboxes.

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


</td></tr><tr><td>

Brazil

</td><td>

-   **[Sandbox pooling for faster provisioning](https://www.servicenow.com/docs/access?context=allocating-sandboxes&family=brazil&ft:locale=en-US)**

Allocate sandboxes faster using pre-pooled instances. When you allocate a sandbox, you claim one from a pre-created pool rather than waiting for a new instance to be provisioned. Sandbox URLs are randomly generated strings and no longer match the sandbox display name. The display name remains configurable, but you can't change the URL.

**Note:** Because pooled sandboxes are precreated, they may be out of date from the current base instance state, but are refreshed every 24 hours.

-   **[Automatic update set sources](https://www.servicenow.com/docs/access?context=dsb-update-sets&family=brazil&ft:locale=en-US)**

Transfer update sets between production and sandbox instances without manual configuration. When a sandbox is created, an update set source pointing to the sandbox is automatically created on the base instance, and an update set source pointing to production is automatically created on the sandbox. When a sandbox is retired, both update set sources are automatically removed.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Developer Sandboxes features.

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

-   **[Upgrade enhancements](https://www.servicenow.com/docs/access?context=dev-sbx-clone-upgrade-info&family=zurich&ft:locale=en-US)**

Automatic backups for upgrades are now working correctly. This issue is related to PRB2017438.


</td></tr><tr><td>

Australia

</td><td>

-   **[Upgrade enhancements](https://www.servicenow.com/docs/access?context=dev-sbx-clone-upgrade-info&family=australia&ft:locale=en-US)**

Automatic backups for upgrades are now working correctly. This issue is related to PRB2017438.


 -   **[Schema change for shared tables isolates the table](https://www.servicenow.com/docs/access?context=dsb-installed-with&family=australia&ft:locale=en-US)**

To ensure configuration consistency, if you make a schema change, such as adding a column, to a shared table, the table now becomes an isolated table on the sandbox that initiated the schema change.


 -   **[Upgrade enhancements](https://www.servicenow.com/docs/access?context=dev-sbx-clone-upgrade-info&family=australia&ft:locale=en-US)**

After an upgrade, Developer Sandboxes now recreates the sandboxes on an instance and automatically backs up update sets to the base instance.

-   **[Queuing for successive sandbox creation](https://www.servicenow.com/docs/access?context=allocating-sandboxes&family=australia&ft:locale=en-US)**

To improve performance, Developer Sandboxes has implemented queuing when multiple sandboxes are created in succession.

-   **[SSO support for vanity URLs](https://www.servicenow.com/docs/access?context=dev-sbx-general-guidelines&family=australia&ft:locale=en-US)**

Instances with vanity URLs can now support Single Sign-On \(SSO\).

-   **[New vibe coding documentation](https://www.servicenow.com/docs/access?context=vibe-coding-landing&family=australia&ft:locale=en-US)**

Documentation is now available that introduces vibe coding, which is a natural language approach to application development in ServiceNow, including how to get started, when to use it, and how it fits within the broader suite of AI-powered development tools.


 -   **[Clarified sandbox initialization status](https://www.servicenow.com/docs/access?context=allocating-sandboxes&family=australia&ft:locale=en-US)**

An error status message now appears on the instance home page when there’s an initialization error when allocating a sandbox.

-   **[Developer Sandboxes home page hidden when product is inactive](https://www.servicenow.com/docs/access?context=dev-sbx-entitlements&family=australia&ft:locale=en-US)**

The Developer Sandboxes home page is unavailable when Developer Sandboxes is inactive on an instance.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Developer Sandboxes features or functionality were removed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Developer Sandboxes features or functionality were deprecated.

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

-   All data generation metadata and non-metadata records are automatically deleted.
-   The data generation plugin is no longer discoverable.
-   All references to data generation will be removed from sandbox templates.
-   Sandbox initialization will operate independently of data generation logic.

</td></tr><tr><td>

Australia

</td><td>

-   All data generation metadata and non-metadata records are automatically deleted.
-   The data generation plugin is no longer discoverable.
-   All references to data generation will be removed from sandbox templates.
-   Sandbox initialization will operate independently of data generation logic.

</td></tr><tr><td>

Brazil

</td><td>

-   **Form changes**
    -   The **Sandbox alias** URL field has been removed from the Allocate Sandbox form. Because sandbox URLs are now randomly generated, you no longer specify a URL at allocation time.
    -   Sandbox templates have been removed from the Allocate Sandbox form.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Developer Sandboxes.

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

-   **Activation information**

Contact your ServiceNow account manager to install Developer Sandboxes.


**Important:** [Developer Sandboxes](https://www.servicenow.com/docs/access?context=sandboxes-landing&family=zurich&ft:locale=en-US) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Contact your ServiceNow account manager to install Developer Sandboxes.


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install the Developer Sandbox License Management \(`com.glide.dsb.licensing`\) plugin on your license management instance, install the sandbox plugin on your non-production instances, and use the license management UI in App Engine Management Center on the controller instance to distribute packs.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Developer Sandboxes we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Support for Build Agent in sandboxes.
-   Enable your administrators and delegated developers to request, access, and manage the isolated development environments on top of the same underlying development instance.
-   Provide developer isolation and parallelism for customer development environments and instances.
-   View the total, available, and allocated sandboxes in your instance by using the Sandbox Management home dashboard. The dashboard also displays information about each sandbox, including the status, data utilization, owner, when it was last accessed, and when the sandbox was allocated.

 See [Developer Sandboxes](https://www.servicenow.com/docs/access?context=sandboxes-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Support for Build Agent in sandboxes.
-   Upgrading an instance recreates sandboxes and backs up any update sets.
-   A new plugin supports clone preservation when cloning an instance with sandboxes.

 See [Developer Sandboxes](https://www.servicenow.com/docs/access?context=sandboxes-landing&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Work in fully isolated environments, so changes in one sandbox don't affect teammates, the baseline instance, or other sandboxes running in parallel.
-   Provision sandboxes on demand and align them to specific stories, developers, or test plans, enabling multiple workstreams to run concurrently without waiting for shared resources.
-   Integrate with source control \(Git\), reducing merge conflicts and making co-development smoother compared to shared development instances.
-   Safely test configurations, workflows, and integrations within your own sandbox before promoting changes, reducing rework and protecting system stability.

 See [Developer Sandboxes](https://www.servicenow.com/docs/access?context=sandboxes-landing&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-yokohama-brazil/rn-combined-intro.md)

