---
title: Combined Service Exchange \(formerly Service Bridge\) release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Service Exchange \(formerly Service Bridge\) from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-serviceexchangeformerlyservicebridge-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Service Exchange \(formerly Service Bridge\) release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Service Exchange \(formerly Service Bridge\) from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Exchange \(formerly Service Bridge\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Exchange \(formerly Service Bridge\) to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

-   **Upgrade information**

**Important:** Do not upgrade your ServiceNow® instance to the Australia release if you rely on Service Exchange. A known RPS issue prevents Service Exchange from functioning correctly. Proceed with the upgrade only after Australia Patch 1 becomes available.

    -   Service Exchange version 2.x.x, which was first released with the Xanadu release, doesn’t support migration of Service Exchange \(Legacy\) versions.

Service Exchange \(Legacy\) version: Before you upgrade to the Australia release, consult the [Service Exchange for Providers \(Legacy\) - Migration Utility \[KB1499823\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) article in the Now Support Knowledge Base to find out how to migrate your configuration data.

    -   Service Exchange version 1.x.x: When upgrading, consult the [Upgrade Guide - Service Exchange for Providers and Consumers application \(v2.x.x release\) \[KB1700387\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387) article in the Now Support Knowledge Base to find out how to migrate your Service Exchange applications.
    -   Service Exchange version 2.x.x: New entitlements that require the latest compatibility version cannot be activated until both consumers and providers upgrade to Service Exchange version 2.x.x. New entitlements configured with a lower compatibility version can be activated. Older active entitlements continue to work but new ones can’t be activated.
    -   When using Service Exchange for Providers and Service Exchange for Consumers in a single instance, you must upgrade both applications simultaneously to the same version to maintain compatibility. If the versions diverge, a scan check will report version mismatches and the Health Dashboard will show a version mismatch issue. After upgrading, run and validate the post‑upgrade scan suite to identify and resolve any post‑upgrade issues.
    -   If you have upgraded to Service Exchange version 2.0.55 before upgrading the platform to the Australia release and your instance has Sales Customer Relationship Management version 1.0.4 installed, the new Deny ACLs aren't installed. After upgrading to the Australia release, select Repair to reinstall the Service Exchange application to ensure Deny ACLs are installed.
    -   If you're upgrading Service Exchange to version 2.3.x, migrate the OAuth grant type on all existing connections from authorization code to client credentials to avoid a "User Not Authenticated" error. Complete this migration on both the provider and consumer instances after the upgrade and before using the connection. For details, see [KB2944968](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2944968).
    -   When you install the Service Exchange application, the Service Exchange Global script include is automatically installed or updated on the following platform versions:
        -   Yokohama
        -   Zurich
        -   Australia

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Service Exchange \(formerly Service Bridge\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

-   **[Service Exchange Knowledge Assistant](https://www.servicenow.com/docs/access?context=now-assist-tmt-service-exchange-assistant-se&family=australia&ft:locale=en-US)**

Get answers to your Service Exchange questions directly in Now Assist, without leaving your current work. The Service Exchange Knowledge Assistant agentic workflow generates answers grounded in documentation that matches the Service Exchange version installed on your instance, and includes links to the source documentation used for every answer.


 -   **[Consumer outbound FDS](https://www.servicenow.com/docs/access?context=service-bridge-v2-explore-foundation-data-sync&family=australia&ft:locale=en-US)**

Reduce manual effort and eliminate the need to share data externally by sharing selected foundational data types with your provider on a scheduled cadence. This data transfer supports the service life cycle by providing foundational data context for operational workflows.

-   **[Service Exchange center](https://www.servicenow.com/docs/access?context=se-se-center&family=australia&ft:locale=en-US)**

Detect problems early, understand connection status, and resolve issues efficiently with the Service Exchange center, a centralized interface that provides real-time visibility into scan check issues, connection health and statuses, and access to all Service Exchange scan suites. Service Exchange admins can access their respective centers through the Provider and Consumer center links in the navigation menu.

-   **[Auto-onboarding](https://www.servicenow.com/docs/access?context=service-bridge-v2-register&family=australia&ft:locale=en-US)**

Reduce onboarding complexity for consumers with automated onboarding. This feature autonomously manages onboarding workflows, establishes secure connections, synchronizes settings, and continuously monitors for errors to ensure reliable, efficient integrations with minimal manual effort.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Service Exchange \(formerly Service Bridge\) features.

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

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


</td></tr><tr><td>

Australia

</td><td>

-   **[Now LLM service deprecation](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Service Exchange \(formerly Service Bridge\) features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Service Exchange \(formerly Service Bridge\) features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Service Exchange \(formerly Service Bridge\).

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

-   **Activation information**

Install Service Exchange by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Service Exchange \(formerly Service Bridge\) we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Service Exchange \(formerly Service Bridge\) we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Service Exchange \(formerly Service Bridge\), such as specific requirements or compliance levels.

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Service Exchange \(formerly Service Bridge\) we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Service Exchange \(formerly Service Bridge\) we have noted them here.

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

[Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US)

-   Get version-specific answers to your Service Exchange related questions with the Service Exchange Knowledge Assistant agentic workflow in Now Assist.

 [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Manage and monitor all your provider and consumer connections from a single, unified Connections tab in the Service Exchange Center.
-   Streamline the end-to-end registration and onboarding experience for consumers with an improved, guided onboarding workflow.
-   Simplify persona management with group-based assignments and persona inheritance to reduce administrative effort and align with enterprise identity and access management \(IAM\) standards.
-   Improve data synchronization across instances by synchronizing knowledge base articles, preserving CMDB sys\_ids, and replicating CI dependency relationships with expanded foundation data sync \(FDS\) capabilities.
-   Map multiple journal fields to the same target field and sync `journal` type fields alongside `journal_input` fields using the Journal Field Framework.

 Australia Early Availability

-   Service Bridge has been renamed Service Exchange.
-   Streamline data replication from consumer to provider instances with consumer outbound foundation data sync.
-   Get enhanced visibility into your instances with the Service Exchange center.
-   Reduce onboarding complexity for consumers with auto-onboarding.

 See [Service Exchange](https://www.servicenow.com/docs/access?context=tmt-service-bridge-both-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

