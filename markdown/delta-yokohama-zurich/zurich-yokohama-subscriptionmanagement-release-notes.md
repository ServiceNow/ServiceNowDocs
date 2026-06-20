---
title: Combined Subscription Management release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Subscription Management from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-subscriptionmanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Subscription Management release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Subscription Management from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Subscription Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Subscription Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Subscription Management version 4.1 is active by default on all instances of the Yokohama release. Update to Subscription Management version 6.0.2 or later to use the latest features. For more information about updating Subscription Management, see [Update an app or plugin](https://servicenow-staging.fluidtopics.net/access?context=update-application-app-mgr&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Subscription Management version 5.0 is active by default on all instances of the Zurich release. Update to Subscription Management version 6.0.2 or later to use the latest features. For more information about updating Subscription Management, see [Update an app or plugin](https://servicenow-staging.fluidtopics.net/access?context=update-application-app-mgr&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Subscription Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Subscription allocation counts according to active users](https://servicenow-staging.fluidtopics.net/access?context=subscription-details-v2&family=yokohama&ft:locale=en-US)**

View the total number of active users in a product subscription. Only active users count toward the subscription allocation totals that appear throughout Subscription Management.

-   **[Allocate subscriptions to all recommended groups](https://servicenow-staging.fluidtopics.net/access?context=allocate-subscriptions-v2&family=yokohama&ft:locale=en-US)**

Select all recommended groups when allocating subscriptions.

-   **[Support for on-premises installation](https://servicenow-staging.fluidtopics.net/access?context=configuring-subscription-management-v2&family=yokohama&ft:locale=en-US)**

Manage subscription usage using Subscription Management on-premises.

-   **[Recommended subscription reasoning](https://servicenow-staging.fluidtopics.net/access?context=addressing-issues-subscription-management-v2&family=yokohama&ft:locale=en-US)**

Determine why Subscription Management displays a subscription recommendation when mapping custom tables or custom applications.

-   **[Manage custom applications and table mapping through the platform](https://servicenow-staging.fluidtopics.net/access?context=allocating-custom-tables-subscr-apps-v2&family=yokohama&ft:locale=en-US)**

Map any missing custom applications and tables in Subscription Management to a subscription directly from the Custom Applications list or Custom Table Inventory list.

-   **[Support for domain separation](https://servicenow-staging.fluidtopics.net/access?context=domain-separation-subscription-mgmt&family=yokohama&ft:locale=en-US)**

View and filter subscribers by domain for user-based subscriptions.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Manage custom applications and table mapping through the platform](https://servicenow-staging.fluidtopics.net/access?context=allocating-custom-tables-subscr-apps-v2&family=zurich&ft:locale=en-US)**

Map any missing custom application and tables in Subscription Management to a subscription directly from the Custom Applications list or Custom Table Inventory list.

-   **[Support for domain separation](https://servicenow-staging.fluidtopics.net/access?context=domain-separation-subscription-mgmt&family=zurich&ft:locale=en-US)**

View and filter subscribers by domain for user-based subscriptionsand view Now Assist usage by domain.

-   **[Monitor Workflow Data Fabric usage](https://servicenow-staging.fluidtopics.net/access?context=monitoring-wdf-capability-use&family=zurich&ft:locale=en-US)**

Monitor and track Workflow Data Fabric capability usage and view the relative token use rate of each capability.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Subscription Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Allocation charts reflect only active users](https://servicenow-staging.fluidtopics.net/access?context=subscription-details-v2&family=yokohama&ft:locale=en-US)**

The Allocation summary and Allocation history charts on the subscription details page reflect only the subscriptions allocated to active users for each month following the upgrade.

-   **[Auditing App Engine V1 usage](https://servicenow-staging.fluidtopics.net/access?context=allocating-custom-tables-subscr-apps-v2&family=yokohama&ft:locale=en-US)**

The App Engine Usage dashboard has been restored. For details on auditing App Engine V1 usage, see the [Auditing App Engine v1 \[KB0999383\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0999383) article in the Now Support Knowledge Base.

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Now Assist usage measurement is evolving. If your instances are below Yokohama Patch 12, update Subscription Management to version 6.0.2 or later on all instances to avoid mixed measurement types. For more information, see [Now Assist Usage - Overview &amp; New Measurement Logic \[KB2704710\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Zurich

</td><td>

-   **[Assist usage excludes demo data](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Demonstration instances are excluded from the total Assist usage count to improve tracking of Assist consumption.

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Now Assist usage measurement is evolving. If your instances are below Zurich Patch 6, update Subscription Management to version 6.0.2 or later on all instances to avoid mixed measurement states. For more information, see [Now Assist Usage - Overview &amp; New Measurement Logic \[KB2704710\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Subscription Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

The Custom tables chart has been removed from the subscription details page.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Subscription Management features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Subscription Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Subscription Management is a ServiceNow AI Platform feature that is active by default. Updates for Subscription Management are available through the [https://servicenow-staging.fluidtopics.net/access?context=external.sn-app-store&amp;family=yokohama&amp;ft:locale=en-US](https://servicenow-staging.fluidtopics.net/access?context=external.sn-app-store&family=yokohama&ft:locale=en-US). For cumulative release notes information for applications available on the ServiceNow Store, see [https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&amp;family=yokohama&amp;ft:locale=en-US](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Subscription Management is a ServiceNow AI Platform feature that is active by default.Updates for Subscription Management are available through the [https://servicenow-staging.fluidtopics.net/access?context=external.sn-app-store&amp;family=zurich&amp;ft:locale=en-US](https://servicenow-staging.fluidtopics.net/access?context=external.sn-app-store&family=zurich&ft:locale=en-US). For cumulative release notes information for applications available on the ServiceNow Store, see [https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&amp;family=zurich&amp;ft:locale=en-US](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Subscription Management we have noted them here.

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
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Subscription Management we have noted them here.

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

Review details on accessibility information for Subscription Management, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Subscription Management we have noted them here.

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
</table>## Highlight information

If there are specific highlight considerations for Subscription Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   View subscription allocations according to the number of active users.
-   Select all recommended groups when allocating subscriptions.
-   Manage subscriptions in an on-premise installation.
-   Manage custom application and table mapping through the platform, and learn why specific subscriptions are recommended when mapping custom tables and applications.
-   View subscribers by domain for user-based subscriptions.

 See [Subscription Management](https://servicenow-staging.fluidtopics.net/access?context=subscription-management-landing-page-v2&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Manage custom applications and table mapping through the custom application list and custom table inventory list.
-   View and filter subscribers by domain for user-based subscriptions in domain-separated instances.
-   View and filter Now Assist usage by domain in domain-separated instances.
-   Monitor Workflow Data Fabric usage and view token use rate of each capability.

 See [Subscription Management](https://servicenow-staging.fluidtopics.net/access?context=subscription-management-landing-page-v2&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

