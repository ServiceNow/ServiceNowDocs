---
title: Combined Service Exchange release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Service Exchange from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-serviceexchange-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Service Exchange release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Service Exchange from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Exchange release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Exchange to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Service Exchange 2.x.x that is being released with the Xanadu release does not support migration of the Service Exchange \(Legacy\) versions. If you are using a Service Exchange \(Legacy\) version, before you upgrade to the Xanadu release, you must follow instructions in the [Service Exchange for Providers \(Legacy\) - Migration Utility \(KB1499823\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) article in the Now Support Knowledge Base to migrate your configuration data.
-   If you are upgrading from version 1.x.x of Service Exchange, follow the steps listed in [Upgrade Guide - Service Exchange for Providers and Consumers application \(v2.x.x release - KB1700387\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387) to migrate your Service Exchange applications.
-   Due to the introduction of mismatched version support, new entitlements cannot be activated until both the consumers and providers upgrade to the Xanadu release. Older active entitlements will continue to work but new ones cannot be activated.

</td></tr><tr><td>

Yokohama

</td><td>

-   When using Service Exchange for Providers and Service Exchange for Consumers in a single instance, you must upgrade both applications simultaneously to the same version to maintain compatibility.
-   The Service Exchange Global Script Include is automatically installed or updated when you install the Service Exchange application on the following platform versions:
    -   Washington DC Patch 9
    -   Xanadu Patch 4
    -   Yokohama
-   Service Exchange 2.x.x, which was first released with the Xanadu release, does not support migration of Service Exchange \(Legacy\) versions. If you are using a Service Exchange \(Legacy\) version, before you upgrade to the Yokohama release, you must follow instructions in the [Service Exchange for Providers \(Legacy\) - Migration Utility \[KB1499823\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) article in the Now Support Knowledge Base to migrate your configuration data.
-   If you are upgrading from Service Exchange version 1.x.x, follow the steps in [Upgrade Guide - Service Exchange for Providers and Consumers application \(v2.x.x release\) \[KB1700387\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387) to migrate your Service Exchange applications.
-   Due to the introduction of mismatched version support, new entitlements cannot be activated until both the consumers and providers upgrade to Service Exchange version 2.x.x. Older active entitlements will continue to work but new ones cannot be activated.
-   If you upgrade to Service Exchange version 2.0.55 with Sales Customer Relationship Management plug-in version 1.0.4 before upgrading the platform to the Yokohama release, the new Deny ACLs will not be installed. To ensure the Deny ACLs get installed, after upgrading to Yokohama, you must click Repair to reinstall the Service Exchange application.

</td></tr><tr><td>

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

Xanadu

</td><td>

-   **[Service Exchange mismatched version support](https://www.servicenow.com/docs/access?context=service-bridge-v2-mismatch-version&family=xanadu&ft:locale=en-US)**

Providers and consumers can run different versions of the Service Exchange applications without affecting their ability to exchange data. Providers can adopt new features without coordinating their application upgrades with their consumers.

-   **[Configuration revisions](https://www.servicenow.com/docs/access?context=service-bridge-v2-config-revision&family=xanadu&ft:locale=en-US)**

Providers can develop and deploy new versions or revisions of entitlements with updated functionality to compatible consumers without affecting consumers who have not updated their application. Consumers can therefore use older revisions of entitlements including remote task definitions, remote record producers, and foundation data sync offerings while deploying new revisions.

-   **[Consumer pre-flows](https://www.servicenow.com/docs/access?context=service-bridge-v2-conf-consumer-flow&family=xanadu&ft:locale=en-US)**

Consumers can control data synchronization with their providers by associating a flow with a Service Exchange remote record producer and run consumer-defined processes, such as approvals, before a task is synchronized to their provider.

-   **[Integration with Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=service-bridge-v2-omt-intg&family=xanadu&ft:locale=en-US)**

Providers can enable customers to quickly order entitled Sales Customer Relationship Management product offerings from their service catalog by publishing them as remote record producers on consumer instances.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Remote Catalog Item Client Scripts](https://www.servicenow.com/docs/access?context=service-bridge-v2-add-scripts-to-rrp&family=yokohama&ft:locale=en-US)**

Provider: Perform more complex tasks and gain better control over the completeness and correctness of catalog requests from the consumer by including catalog client scripts, UI Policy scripts, and other common scripts that consumers can choose to include for Remote Catalog items.

-   **[Copy From Service Catalog Item to Remote Catalog Item](https://www.servicenow.com/docs/access?context=service-bridge-v2-copy-catalog-as-rrp&family=yokohama&ft:locale=en-US)**

Providers: Eliminate the need to re-create catalog items manually in the Service Exchange remote catalog by copying single and multiple catalog items through the UI to remote record producers that can be synchronized to the consumer instance.

-   **[Transform Mapping Assist](https://www.servicenow.com/docs/access?context=now-assist-tmt-exploring&family=yokohama&ft:locale=en-US)**

Providers: Streamline the transformation mapping process and reduce errors by generating transform mappings between provider and consumer tables automatically using the Transform Mapping Assist feature that leverages the NOW large language model \(LLM\).

-   **[Consumer Variable Sets](https://www.servicenow.com/docs/access?context=service-bridge-v2-consumer-variables&family=yokohama&ft:locale=en-US)**

Consumers: Manage requested content and flow better by adding additional variables to add customization to your remote record producers.


</td></tr><tr><td>

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

Between your current release family and Australia, some Service Exchange features or functionality were removed.

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

Between your current release family and Australia, some Service Exchange features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Service Exchange \(legacy\) application is now deprecated and no longer supported or available for new activation. The Service Exchange for Consumers application provides the latest experience for this functionality.
-   Service Exchange for Providers \(legacy\) application is now deprecated and no longer supported or available for new activation. The Service Exchange for Providers application provides the latest experience for this functionality.

See [KB1499823](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) for details on migrating from the legacy version.

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

Review information on how to activate Service Exchange.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Service Exchange by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Service Exchange by requesting it from the ServiceNow Store.

</td></tr><tr><td>

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

If any specific browser requirements were introduced or changed for Service Exchange we have noted them here.

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

Review details on accessibility information for Service Exchange, such as specific requirements or compliance levels.

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

If there are specific highlight considerations for Service Exchange we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Enable providers to adopt new features and provide uninterrupted service to their consumers who have not upgraded.
-   Assess entitlements for compatibility before syncing them to consumers.
-   Enable consumers to run specific processes such as approvals before synchronizing tasks with their providers.
-   Support automated synchronization of configuration data between provider and consumer instances.

 See [Service Exchange](https://www.servicenow.com/docs/access?context=tmt-service-bridge-both-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Providers can now include client and UI policy scripts in remote record producers, which consumers can review and approve.
-   Providers can now copy local catalog items to Service Exchange as remote record producers either in bulk or individually.
-   Providers can simplify and streamline choice-based transform mapping with ServiceNow Now Assist.
-   Consumers can now add variables to remote record producers for use in consumer pre-flows.

 See [Service Exchange](https://www.servicenow.com/docs/access?context=tmt-service-bridge-both-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

