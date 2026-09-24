---
title: Service Catalog release notes
description: The ServiceNow Service Catalog application provides a requester view of available services and products offered by departments within your organization. See the following sections for release notes by version.The Brazil release adds configurable subscription access enforcement for catalog items and lets migrate Core UI to an Angular portal using a plugin only on upgrades.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/service-catalog-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform capabilities release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Service Catalog release notes

The ServiceNow® Service Catalog application provides a requester view of available services and products offered by departments within your organization. See the following sections for release notes by version.

## About Service Catalog

-   Develop comprehensive service catalogs to empower users with self-service capabilities.
-   Tailor portals to let users request a range of catalog items, including services and product offerings.
-   Standardize request fulfillment processes to verify the accuracy and availability of items within the catalogs.

See [Service Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-catalog.md) for more information.

## Activation and other requirements

-   **Activation information**

    Service Catalog is a ServiceNow AI Platform feature that is active by default.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/now-platform-capabilities-rn-landing.md)

## Brazil Early Availability

The Brazil release adds configurable subscription access enforcement for catalog items and lets migrate Core UI to an Angular portal using a plugin only on upgrades.

### What's new

-   **[Configurable subscription access enforcement for catalog items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/r_ServiceCatalogProperties.md)**

    Control whether service subscriptions can bypass "Available for" user criteria on catalog items using the `glide.sc.catalog_item.subscription_enforcement` property. This setting verifies that only users meeting specific criteria can access items, even with a parent service subscription.

    The property controls this behavior with the following two modes:

    -   require\_criteria: Prevents access to users who don't meet the item's criteria, even if they are subscribed to the parent service offering.
    -   allow\_bypass: Preserves existing behavior that means users gain access through the "Available for" user criteria. "allow\_bypass" is a default value.
-   **[Migration from Core UI to Angular portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/migrate-core-ui-to-angular-catalog-exp.md)**

    Migrate from the Core UI catalog experience to the Angular portal using the `com.glideapp.servicecatalog.ui16_portal` plugin, but only for upgraded instances.

    Administrators on upgraded instances must install the`com.glideapp.servicecatalog.ui16_portal` plugin to move from the Core UI catalog experience to the Angular portal. On new instances, the plugin is active by default. Requesters view the Angular portal instead of Core UI while requesting a catalog item.


### What's deprecated or removed

-   **Removal of Catalog Roles from request management ACLs**

    ACL records on request management tables and fields no longer grant access based on the catalog role or the catalog admin role. ACL records for tables owned by request management, such as Request \[sc\_request\] and Requested Item \[sc\_req\_item\], no longer include catalog-related roles in the list of required roles. Each ACL record retains at least one request management role, so the list is never empty. Users who have only a catalog-related role and no request management role can no longer use these ACL records to access request management tables or features. Another ACL record on the same table might still grant access through a different role. This change affects only the ACL records that the catalog team owns.


