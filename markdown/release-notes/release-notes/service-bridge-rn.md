---
title: Service Exchange \(formerly Service Bridge\) release notes
description: The ServiceNow Service Exchange application, formerly known as Service Bridge, enables providers and consumers to connect and track services directly between instances without having to configure and maintain custom integrations. Service Exchange was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# Service Exchange \(formerly Service Bridge\) release notes

The ServiceNow® Service Exchange application, formerly known as Service Bridge, enables providers and consumers to connect and track services directly between instances without having to configure and maintain custom integrations. Service Exchange was enhanced and updated in the Australia release.

## Service Exchange highlights for the Australia release

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

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

See [Service Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/tmt-service-bridge-both-landing-page.md) for more information.

**Important:** Service Exchange is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Service Exchange features

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   **[Connections tab in the Service Exchange Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/se-connections-tab.md)**

    Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

-   **[Improved consumer registration and onboarding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/se-provider-center-onboarding.md)**

    Onboard consumers faster with a guided, step-by-step registration experience. Consumers are automatically redirected to the new registration experience when upgrading to receive clearer progress indicators during onboarding, and receive actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

-   **[Improved FDS capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-explore-foundation-data-sync.md)**

    Improve your connection experience, by synchronizing Knowledge Base articles between provider and consumer instances.

    Reduce data inconsistencies by maintaining CMDB `sys_ids` when inserting net-new CIs through transform maps.

    Preserve CI functionality on the destination instance by automatically creating CI dependency relationships or managing them manually when the source sends relationship data.

    Get more referenced field data by including dot-walked fields in your outbound field configuration.

-   **[Journal Field Framework enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-expolre-journal-field-framework.md)**

    Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.

    Preserved all journal entries during synchronization by supporting journal field type `journal_input`, in addition to the existing journal field type.

-   **[Simplified persona management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-customer-roles.md)**

    Assign Service Exchange Remote Catalog personas to user groups or roles so that persona access is granted automatically based on group membership, reducing manual administration.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


Australia Early Availability

-   **[Consumer outbound FDS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-explore-foundation-data-sync.md)**

    Reduce manual effort and eliminate the need to share data externally by sharing selected foundational data types with your provider on a scheduled cadence. This data transfer supports the service life cycle by providing foundational data context for operational workflows.

-   **[Service Exchange center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/se-se-center.md)**

    Detect problems early, understand connection status, and resolve issues efficiently with the Service Exchange center, a centralized interface that provides real-time visibility into scan check issues, connection health and statuses, and access to all Service Exchange scan suites. Service Exchange admins can access their respective centers through the Provider and Consumer center links in the navigation menu.

-   **[Auto-onboarding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-register.md)**

    Reduce onboarding complexity for consumers with automated onboarding. This feature autonomously manages onboarding workflows, establishes secure connections, synchronizes settings, and continuously monitors for errors to ensure reliable, efficient integrations with minimal manual effort.


## UI changes

-   **[Health dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/se-se-center.md)**

    The Health dashboard has been relocated to the Service Exchange Center. Access a more holistic view of system health that includes a resolution center, connection health, and built-in scan suites providing centralized visibility and faster troubleshooting of integration issues.


## Important upgrade information for Service Exchange

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

## Activation information

Install Service Exchange by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-overview.md)**

    The Sales Customer Relationship Management applications enable you to manage the product sales life cycle in your organization, including pre-sales opportunities, sales quote generation, order capture, order fulfillment, and post-sales engagement.

-   **[Supporting information for HR Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery-overview.md)**

    Improve the employee service experience by automating HR interactions and providing a single platform for all HR services. Replace manual and siloed processes with cross-functional digital workflows for increased efficiency. Align business goals with employee needs, including onboarding, career growth, and other transitions.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/technology-industry-rn-landing.md)

