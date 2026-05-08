---
title: Multi-source service mapping
description: Multi-source service mapping combines data from multiple discovery methods to create a single, comprehensive service map that provides complete visibility into your organization's hybrid IT infrastructure.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Service Mapping, ITOM, CMDB, Configuration item, service map, unified service, Keystone, service instance, service\_mapping\_admin]
breadcrumb: [Choose method for discovering and mapping services, Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Multi-source service mapping

Multi-source service mapping combines data from multiple discovery methods to create a single, comprehensive service map that provides complete visibility into your organization's hybrid IT infrastructure.

## What is multi-source service mapping

Multi-source service mapping enables you to create unified services. You can create unified services combining mapped and unmapped services from different data sources in your CMDB. Instead of managing separate service maps created through different discovery methods, you can add them into a single composite service that represents your organization's interconnected service architecture.

This feature addresses the challenge of managing complex IT environments where a single service instance might be discovered through multiple methods, each providing partial visibility. For example, some components can be discovered through pattern-based top-down discovery, while others are more effectively identified through tag-based Service Mapping. Multi-source service mapping brings together data from all available sources to create a complete picture.

![](../image/unified-service-600px.png)

## Supported data sources

Multi-source service mapping can combine data from the following sources:

-   **Discovered maps**

    Horizontal or top-down discovery that identifies configuration items \(CI\) and their connections using Discovery and Service Mapping Patterns. These methods involves running discovery using a MID Server.

-   **Tag-based maps**

    Services mapped using cloud-native tags and metadata from your asset management system. This method is effective for cloud environments where tags are used for organization and categorization.

-   **ML-powered maps**
    -   Machine learning-based discovery that evaluates connections between application fingerprints, CIs, and processes. This method provides additional data through connections and processes discovered during monitoring.
    -   Traffic-based mapping is based on network traffic connections between devices and applications. This method helps identify communication patterns and dependencies based on actual network behavior.
-   **Manual service maps**

    Manually selecting specific CIs without automation. By converting manual services to a dynamic application services, you can synchronize the manually created CI relationships into a Service Map view. These maps are maintained by administrators and are best fit for static services. For more information, see: Convert legacy manual services to dynamic application services

-   **Dynamic CI groups**

    Based on CMDB relationships, this query-based mapping can be used for mapping technical services grouped under a specific category. For example, all Linux servers in a certain location.


## Key benefits

Multi-source service mapping offers several advantages for organizations managing complex, hybrid IT environments:

-   **Complete visibility**

    Your organization can gain broader and more detailed visibility of application dependencies across your entire infrastructure, including on-premises, cloud, and hybrid environments. Different discovery methods excel at finding different types of components, and combining them ensures that nothing is missed.

-   **Reduced duplication issues**

    Your organization can eliminate redundant service definitions by consolidating multiple partial views into a single authoritative service map. The same CIs often appear across different service maps, and unification removes this redundancy. By including unmapped services, the service maps reflect a single source of truth.

-   **Improved incident response**

    Service-level actions can improve Mean Time to Resolve \(MTTR\) and business outcomes compared to CI-level fixes, as teams work from a unified view rather than fragmented information.


## Use cases

Multi-source service mapping is valuable in the following scenarios:

-   **Incident Management**

    When a single server appears in multiple separate service maps, its failure can trigger multiple teams to work on the same issue. A unified service map provides a complete dependency picture, reducing Mean Time to Resolve \(MTTR\) and helping to prevent duplicate work across teams.

-   **Change Management**

    When a database schema change is reflected in a single service map but not another, it increases the risk of unplanned outages. Multi-source mapping can promote visibility to all dependencies, enabling accurate analysis of impact across the entire service.

-   **Reporting and Compliance**

    Organizations reporting on service uptime for Service Level Agreement \(SLA\) compliance can achieve more accurate statistics and reports with a unified view, rather than manually correlating data from multiple separate service maps.


## Multi-source service-mapping workflows

The multi-source service-mapping process follows these key phases:

-   **[Creating a unified service](../task/unified-map-create-service-instance.md)**

    Service Mapping administrators can access this flow through the Service Mapping workspace. They can search for services based on properties related to the services, such as server tag, or UR and choose the services to unify. They can choose mapped and unmapped services from various types. For example, they can unify a top-down service with a tag-based service. Unmapped services can be added to the unified service and converted to mapped services along the process. A ranking algorithm suggests the top recommendations of services to merge, according to the criteria provided.

    **Note:** The feature supports unification of 10 services maximum, by default. Service Mapping administrators can change the limit using the sn\_sm\_scoped\_app.sm.unified\_services.max\_children\_per\_service system property.

    After creating the unified service, the feature automatically transforms the selected unmapped services into non-operational service instances. This happens in order to prevent automatic discovery and impact on ITOM or ITSM processes. The Service Mapping administrator can choose to convert the services to operational using the **Mapped application services** list.

    When the process of creating the unified service is complete, the unified service map is displayed in the "Unified map" format, through the CMDB Workspace, showing the complete consolidated view.

-   **[Editing the unified service](../task/unified-map-edit-unified-service.md)**

    The Service Mapping administrator can add additional services from various types or remove a service if needed. The feature doesn't support unification of unified services, only single services.

-   **[Deleting the unified service](../task/unified-map-delete-unified-service.md)**

    The Service Mapping administrator can delete the unified service if needed. Child services remain non-operational by default.


## Getting Started

To use multi-source service mapping, your ServiceNow instance must have the following setting.

-   At least Australia family version installed.
-   Service Mapping Plus installed and updated to the latest version.
-   At least two existing services to unify, or at least two sources of data that are actively updated. If there are no existing services on your instance, choose a method to create the services. For more information, see: [Choose the right method for discovery and mapping application services](choose-mapping-method.md).

