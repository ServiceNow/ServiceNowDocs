---
title: Domain separation and Service Mapping
description: Domain separation is supported in Service Mapping. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/domain-separation-service-mapping.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Domain separation and Service Mapping

Domain separation is supported in Service Mapping. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## How domain separation works in Service Mapping

In domain-separated environments, switch into relevant leaf domains to access actions related to mapping performed by Service Mapping. A leaf domain is a child domain of the lowest level, meaning it does not have any child domains itself.

Domain separation is handled in a slightly different way than simply configuring separate domains. Notice that you must select or specify the relevant leaf domain to perform the following mapping actions in domain-separated environments:

-   When creating an service instance, the service instance is assigned to the user's domain.
-   When manually adding a CI to an service instance, you can choose only CIs that belong to the service domain.
-   When manually adding connections to CIs to an service instance, users must belong to the same domain as the application service.
-   When transferring service definitions between instances, imported service instances and service groups are assigned to the user's domain.

## Domain separation and Automated Service Suggestions

Automated Service Suggestions supports domain separation. This means that:

-   The source and target process must reside in the same domain to create a connection.
-   The user can view only the data in the current domain.

**Note:** After installing Service Mapping Plus with domain separation support, verify that all content is in the appropriate domain. For a detailed explanation of the required steps, see the [Service mapping plus for domain separated instance \[KB1303398\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1303398) article in the Now Support Knowledge Base.

Automated Service Suggestions supports domain separation starting with version 1.9.0. No support is currently offered for on-premise instances. Reach out to product management for further information.

For more context, refer to [Discovery patterns used by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/c_MappingPatternsCustomization.md) topic and [MID Server configuration for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/configure-mid-service-mapping.md). The following topics provide operational information on how to use Service Mapping in deployments with domain separation:

-   [Enable traffic-based discovery for CI types or specific CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/t_CreateATrafficBasedDiscoveryRule.md)
-   [Map application services using tags with classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/map-service-tag.md)
-   [Create or customize patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/t_CreatePatternPatDef.md)
-   [Create entry point types for Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/t_CreateEntryPoint.md)
-   [Enhance patterns without modifying identification sections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/modify-pattern-using-extensions.md)

**Parent Topic:**[Service Mapping reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-reference.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

[bundle-psec.bp-domain-sep-recommended]

