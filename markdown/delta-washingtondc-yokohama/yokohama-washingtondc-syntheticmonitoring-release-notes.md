---
title: Combined Synthetic monitoring release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for Synthetic monitoring from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-syntheticmonitoring-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined Synthetic monitoring release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for Synthetic monitoring from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Synthetic monitoring release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Synthetic monitoring to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Synthetic monitoring.

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

-   **[Create and edit a synthetic monitor](https://www.servicenow.com/docs/access?context=create-synthetic-monitor&family=yokohama&ft:locale=en-US)**

Create and manage synthetic tests to replicate end-user transactions for critical service endpoints. Configure an alert to activate when a test fails, enabling you to address issues before they impact users.

As of version 1.2, you can:

    -   Test for response code: Confirm that your endpoints are returning success codes and know when they aren’t.
    -   Test for response time: Confirm that your services are meeting performance expectations by setting thresholds for response times.
    -   Test for response text: Validate whether specific content exists in the response body, enabling accurate end-to-end checks.
    -   Run tests from your local Glide instance: Enable closer integration with your instance and reduce the need for external test runners.
    -   Run tests from multiple locations.
-   **[Identifying system issues with synthetic monitoring](https://www.servicenow.com/docs/access?context=identifying-system-issues&family=yokohama&ft:locale=en-US)**

View the Overview page for a monitor where you can:

    -   View the status of the monitor.
    -   View charts that display test failures and response times.
    -   Visit related configuration items \(CIs\) that might be the start to investigating failed tests.
    -   View a historical log of synthetic test runs, including details and the response body text.
    -   Share results by exporting a list of tests for a monitor.

</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Synthetic monitoring features.

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

</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Synthetic monitoring features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Synthetic monitoring features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Synthetic monitoring.

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

Install synthetic monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Synthetic monitoring we have noted them here.

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

You must do the following before you can use synthetic monitoring:

-   If you have version 1.0, configure at least one proxy agent on the Agent Client Collector. These agents should be the ones you use to monitor the health and performance of the services to be monitored. For more information about proxy agents, see [Using proxy agents in Agent Client Collector](https://www.servicenow.com/docs/access?context=proxy-agent&family=yokohama&ft:locale=en-US).

Starting with version 1.2, you can run tests from your local Glide instance instead of a proxy agent.

-   Add CIs in the CMDB for the endpoints that you want to monitor.
-   If your endpoints require authentication, configure credentials in the Credentials \[discovery\_credentials\] table.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Synthetic monitoring we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Synthetic monitoring, such as specific requirements or compliance levels.

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Synthetic monitoring we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Synthetic monitoring we have noted them here.

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

-   View real-world performance data from your services without needing actual users, catching issues before they're released to production.
-   Get real-time notifications for performance degradations or outages before they impact users.
-   Visualize synthetic test results and share insights with stakeholders.

 See [Synthetic monitoring](https://www.servicenow.com/docs/access?context=synthetic-monitoring-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)

