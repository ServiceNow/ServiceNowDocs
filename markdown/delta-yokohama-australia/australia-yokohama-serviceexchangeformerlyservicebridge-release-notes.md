---
title: Combined Service Exchange \(formerly Service Bridge\) release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Service Exchange \(formerly Service Bridge\) from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-serviceexchangeformerlyservicebridge-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 7
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

**Important:** Do not upgrade your ServiceNow® instance to the Australia release if you rely on Service Exchange. A known RPS issue prevents Service Exchange from functioning correctly. Proceed with the upgrade only after Australia Patch 1 becomes available.

-   Service Exchange version 2.x.x, which was first released with the Xanadu release, doesn’t support migration of Service Exchange \(Legacy\) versions.

Service Exchange \(Legacy\) version: Before you upgrade to the Australia release, consult the [Service Exchange for Providers \(Legacy\) - Migration Utility \[KB1499823\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) article in the Now Support Knowledge Base to find out how to migrate your configuration data.

-   Service Exchange version 1.x.x: When upgrading, consult the [Upgrade Guide - Service Exchange for Providers and Consumers application \(v2.x.x release\) \[KB1700387\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387) article in the Now Support Knowledge Base to find out how to migrate your Service Exchange applications.
-   Service Exchange version 2.x.x: New entitlements that require the latest compatibility version cannot be activated until both consumers and providers upgrade to Service Exchange version 2.x.x. New entitlements configured with a lower compatibility version can be activated. Older active entitlements continue to work but new ones can’t be activated.
-   When using Service Exchange for Providers and Service Exchange for Consumers in a single instance, you must upgrade both applications simultaneously to the same version to maintain compatibility. If the versions diverge, a scan check will report version mismatches and the Health Dashboard will show a version mismatch issue. After upgrading, run and validate the post‑upgrade scan suite to identify and resolve any post‑upgrade issues.
-   If you have upgraded to Service Exchange version 2.0.55 before upgrading the platform to the Australia release and your instance has Sales Customer Relationship Management plug-in version 1.0.4 installed, the new Deny ACLs aren't installed. After upgrading to the Australia release, select Repair to reinstall the Service Exchange application to ensure Deny ACLs are installed.
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

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   **[Connections tab in the Service Exchange Center](https://www.servicenow.com/docs/access?context=se-connections-tab&family=australia&ft:locale=en-US)**

Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

-   **[Improved consumer registration and onboarding](https://www.servicenow.com/docs/access?context=se-provider-center-onboarding&family=australia&ft:locale=en-US)**

Onboard consumers faster with a guided, step-by-step registration experience. Consumers are automatically redirected to the new registration experience when upgrading to receive clearer progress indicators during onboarding, and receive actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

-   **[Improved FDS capabilities](https://www.servicenow.com/docs/access?context=service-bridge-v2-explore-foundation-data-sync&family=australia&ft:locale=en-US)**

Improve your connection experience, by synchronizing Knowledge Base articles between provider and consumer instances.

Reduce data inconsistencies by maintaining CMDB `sys_ids` when inserting net-new CIs through transform maps.

Preserve CI functionality on the destination instance by automatically creating CI dependency relationships or managing them manually when the source sends relationship data.

Get more referenced field data by including dot-walked fields in your outbound field configuration.

-   **[Journal Field Framework enhancements](https://www.servicenow.com/docs/access?context=service-bridge-v2-expolre-journal-field-framework&family=australia&ft:locale=en-US)**

Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.

Preserved all journal entries during synchronization by supporting journal field type `journal_input`, in addition to the existing journal field type.

-   **[Simplified persona management](https://www.servicenow.com/docs/access?context=service-bridge-v2-customer-roles&family=australia&ft:locale=en-US)**

Assign Service Exchange Remote Catalog personas to user groups or roles so that persona access is granted automatically based on group membership, reducing manual administration.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


Australia Early Availability

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

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

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

Install Service Exchange by requesting it from the ServiceNow Store. 

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

