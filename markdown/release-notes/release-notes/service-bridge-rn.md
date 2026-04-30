---
title: Service Exchange release notes
description: ServiceNow Service Exchange will be renamed for the 2026 Australia release and will maintain the same functionality. This application enables providers and consumers to connect and track services directly between instances without having to configure and maintain custom integrations. Service Exchange was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Service Exchange release notes

ServiceNow® Service Exchange will be renamed for the 2026 Australia release and will maintain the same functionality. This application enables providers and consumers to connect and track services directly between instances without having to configure and maintain custom integrations. Service Exchange was enhanced and updated in the Zurich release.

## Service Exchange highlights for the Zurich release

-   Streamline data replication from provider to consumer instances with foundation data sync.
-   Enable seamless collaboration between provider and consumer with enhanced journal entry support.
-   Enable consumer users to access linked resources in the provider instance using magic links.

See [Service Exchange](https://www.servicenow.com/docs/access?context=tmt-service-bridge-both-landing-page&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US) for more information.

**Important:** Service Exchange is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Service Exchange to Zurich

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

## New in the Zurich release

-   **[Foundation data sync](https://www.servicenow.com/docs/access?context=service-bridge-v2-explore-foundation-data-sync&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US)**

    Reduce manual effort, and eliminate the need to share data externally by sharing selected foundational data types with your consumers on a scheduled cadence. This data transfer supports the service life cycle by providing foundational data context for operational workflows. The supported tables are CMDB \(CIs\), CMDB Relationship, Asset, User, Group, Location, Company, and Department.

-   **[Journal field framework](https://www.servicenow.com/docs/access?context=service-bridge-v2-expolre-journal-field-framework&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US)**
    -   Write journal entries as a named user instead of using a generic company name to enhance authenticity and accountability.
    -   Maintain a complete historical record across instances by synchronizing previous journal entries between provider and consumer instances.
    -   Ensure that all critical operational updates remain current by mapping and synchronizing any journal-type field between provider and consumer instances.
-   **[Flow action](https://www.servicenow.com/docs/access?context=service-bridge-v2-flow-action&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US)**

    Ensure that Remote Tasks and Remote Record Producers continue to function correctly as you adopt newer revisions by maintaining flow compatibility across configuration revisions using four new Flow Actions that preserve mapped variable integrity.

-   **[Magic links](https://www.servicenow.com/docs/access?context=service-bridge-v2-explore-magic-link&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US)**

    Convert regular links sent from a provider instance into magic links that enable consumer users to directly access the linked resource in the provider instance without having to manually log in.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Activation information

Install Service Exchange by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=order-mgt-overview&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    The Sales Customer Relationship Management applications enable you to manage the product sales life cycle in your organization, including pre-sales opportunities, sales quote generation, order capture, order fulfillment, and post-sales engagement.

-   **[Supporting information for HR Service Delivery](https://www.servicenow.com/docs/access?context=hr-service-delivery-overview&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Improve the employee service experience by automating HR interactions and providing a single platform for all HR services. Replace manual and siloed processes with cross-functional digital workflows for increased efficiency. Align business goals with employee needs, including onboarding, career growth, and other transitions.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](technology-industry-rn-landing.md)

