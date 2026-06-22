---
title: Combined Service Exchange release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Service Exchange from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-serviceexchange-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined Service Exchange release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Service Exchange from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Exchange release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Exchange to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Service Exchange version 2.x.x: Which was first released with the Xanadu release, doesn’t support migration of Service Exchange \(Legacy\) versions.

Service Exchange \(Legacy\) version: Before you upgrade to the Zurich release, follow instructions in the [Service Bridge for Providers \(Legacy\) - Migration Utility \[KB1499823\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) article in the Now Support Knowledge Base to migrate your configuration data.

-   Service Exchange version 1.x.x: When upgrading, follow the steps in the [Upgrade Guide - Service Bridge for Providers and Consumers application \(v2.x.x release\) \[KB1700387\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387) article in the Now Support Knowledge Base to migrate your Service Exchange applications.
-   Service Exchange version 2.x.x: Due to the introduction of mismatched version support, new entitlements can’t be activated until both the consumers and providers upgrade to Service Exchange version 2.x.x. Older active entitlements continue to work but new ones can’t be activated.
-   When you upgrade to Service Exchange version 2.0.55 with Sales Customer Relationship Management plug-in version 1.0.4, before upgrading the platform to the Zurich release, new Deny ACLs aren't installed. To ensure the Deny ACLs get installed, after upgrading to Zurich, select Repair to reinstall the Service Exchange application.
-   When using Service Exchange for Providers and Service Exchange for Consumers in a single instance, you must upgrade both applications simultaneously to the same version to maintain compatibility.
-   When you install the Service Exchange application, the Service Exchange Global Script Include is automatically installed or updated on the following platform versions:
    -   Washington DC patch 9
    -   Xanadu patch 4
    -   Yokohama
    -   Zurich

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Service Exchange.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Foundation data sync](https://www.servicenow.com/docs/access?context=service-bridge-v2-explore-foundation-data-sync&family=zurich&ft:locale=en-US)**

Reduce manual effort, and eliminate the need to share data externally by sharing selected foundational data types with your consumers on a scheduled cadence. This data transfer supports the service life cycle by providing foundational data context for operational workflows. The supported tables are CMDB \(CIs\), CMDB Relationship, Asset, User, Group, Location, Company, and Department.

-   **[Journal field framework](https://www.servicenow.com/docs/access?context=service-bridge-v2-expolre-journal-field-framework&family=zurich&ft:locale=en-US)**
    -   Write journal entries as a named user instead of using a generic company name to enhance authenticity and accountability.
    -   Maintain a complete historical record across instances by synchronizing previous journal entries between provider and consumer instances.
    -   Ensure that all critical operational updates remain current by mapping and synchronizing any journal-type field between provider and consumer instances.
-   **[Flow action](https://www.servicenow.com/docs/access?context=service-bridge-v2-flow-action&family=zurich&ft:locale=en-US)**

Ensure that Remote Tasks and Remote Record Producers continue to function correctly as you adopt newer revisions by maintaining flow compatibility across configuration revisions using four new Flow Actions that preserve mapped variable integrity.

-   **[Magic links](https://www.servicenow.com/docs/access?context=service-bridge-v2-explore-magic-link&family=zurich&ft:locale=en-US)**

Convert regular links sent from a provider instance into magic links that enable consumer users to directly access the linked resource in the provider instance without having to manually log in.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Service Exchange features.

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
</table>## Removed

Between your current release family and Australia, some Service Exchange features or functionality were removed.

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

Between your current release family and Australia, some Service Exchange features or functionality were deprecated.

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

Review information on how to activate Service Exchange.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Service Exchange by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Service Exchange we have noted them here.

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

If any specific browser requirements were introduced or changed for Service Exchange we have noted them here.

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

Review details on accessibility information for Service Exchange, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Service Exchange we have noted them here.

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

If there are specific highlight considerations for Service Exchange we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Streamline data replication from provider to consumer instances with foundation data sync.
-   Enable seamless collaboration between provider and consumer with enhanced journal entry support.
-   Enable consumer users to access linked resources in the provider instance using magic links.

 See [Service Exchange](https://www.servicenow.com/docs/access?context=tmt-service-bridge-both-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

