---
title: Business Continuity Management and ServiceNow Store
description: Business Continuity Management applications are available from the ServiceNow Store, enabling you to obtain new and updated features more rapidly. Before you can use the Business Continuity Management applications, you must verify that you have an entitlement to use them.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Business Continuity Management and ServiceNow Store

Business Continuity Management applications are available from the ServiceNow Store, enabling you to obtain new and updated features more rapidly. Before you can use the Business Continuity Management applications, you must verify that you have an entitlement to use them.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

The list of BCM applications available on ServiceNow Store is:

|Application|Description|
|-----------|-----------|
|GRC: Business Impact Analysis|Provides structured workflows for business continuity management teams to assess the impact of a disruption for critical resources such as business processes, applications, and locations.|
|GRC: Business Continuity Planning|Provides capabilities for business continuity management teams to create, review, and approve business continuity and disaster recovery plans.|
|GRC: Crisis Management|Provides capabilities for business continuity management teams to activate business continuity plans during plan exercises and actual crisis events.|
|GRC: Crisis Management integration with Everbridge Notifications \(com.snc.bcm.app\_crisis\_ebn\_intg\)|Provides integration with Everbridge to create and send notification, and track responses.|
|GRC: Crisis Map \(com.snc.app\_bcm\_crisis\_map\)|Provides the ability to integrate with the Feeds and Alert Management application to view the threat alerts and assets at risk on the BCM crisis map. Also, take appropriate action by triggering the Crisis Management event and notification workflows.|
|GRC: Approver Configurator \(sn\_grc\_appr\)|Provides capabilities to define multiple levels of approvals based on approval rule definitions.|

**Note:** Installing GRC: Business Impact Analysis, GRC: Business Continuity Planning, or GRC: Crisis Management automatically installs GRC: Business Continuity Management – Core, GRC: Business Continuity Management – Components, and GRC: Approver Configurator.

GRC: Business Continuity Management – Core provides capabilities to configure data that are required for the business continuity management applications. This application also installs GRC: Business Continuity Management – Components: Now Design System components for Business Continuity Management application.

-   **[Get entitlement for the BCM application](../task/entitle-bcm-product.md)**  
The first step in installing an application is to verify that the application or the product and its associated applications have valid ServiceNow entitlements.
-   **[Install Business Continuity Management from ServiceNow Store](../task/install-business-continuity-management.md)**  
You can install the Business Continuity Management application if you have the admin role. This application includes demo data and installs the related store applications if they are not already installed.
-   **[BCM lite operators](bcm-lite-operators.md)**  
The Business Continuity Management application provides flexible user licensing terms. The terms are based on whether your operator has read-only access or can complete certain types of tasks.

**Parent Topic:**[Configuring Business Continuity Management](configuring-business-continuity-management.md)

