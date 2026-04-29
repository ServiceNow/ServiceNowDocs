---
title: CSDM data domains
description: The CSDM is the data model that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB help to promote that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Explore, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CSDM data domains

The CSDM is the data model that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB help to promote that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.

## CSDM data domains

As described in [Exploring the CSDM model](csdm-content-frame-exploring.md), each domain is associated with one or more products, services, or service types, each of which you can extend as needed. Every box in the diagram \(except Catalog Item\) represents tables that hold CIs in the CMDB. Each connecting line represents a relationship between CI classes. Roles and user types appear next to their area of responsibility.

![CSDM conceptual model.](../image/csdm-model-v5.png)

![CSDM domains with standard color-coding as described in the following list.](../image/csdm-high-level-domain-desc-v5.png)

-   **Foundation domain**

    Tables in the Foundation domain contain base data that is referenced from or to objects in the other CSDM domains. Before you can use ServiceNow products, you must populate foundational data. For more information, see [Foundation domain in the CSDM model](foundation-domain.md)

-   **Ideation &amp; Strategy domain**

    The Ideation &amp; Strategy domain represents the ideas, concepts, and considerations for both the creation of new or additional services as well as improvements and enhancements to existing services. These capabilities are part of Strategic Portfolio Management \(SPM\). For more information, see [Ideation &amp; Strategy domain in the CSDM model](ideation-strategy-domain.md).

-   **Design &amp; Planning domain**

    Enterprise architects and digital product owners work on the design and planning of digital products that your organization can either buy or build. For more information, see [Design &amp; Planning domain in the CSDM model](design-domain.md).

-   **Build &amp; Integration domain**

    Development teams use the tables in the Build &amp; Integration domain during the build effort \(systems development life cycle — AGILE DEVELOPMENT\) of digital products. The tables represent the logical development details of the enterprise applications \(digital products\) to be deployed and used by your organization. These are not operational CIs. For more information, see [Build &amp; Integration domain in the CSDM model](build-domain.md).

-   **Service Delivery domain**

    The Service Delivery domain represents the overall end-to-end service delivery system that includes the infrastructure, technologies, integration patterns \(infrastructure, systems, data, processes, dependency models\), service delivery networks, and operational models. Together, these items deliver the services that conform to CSDM to internal and external users and organizations. For more information, see [Service Delivery domain in the CSDM model](manage-tech-servs-domain.md).

-   **Service Consumption domain**

    Internal or external consumers can request business services through the request catalogs in the Service Consumption domain. The business service offerings in the request catalogs are the deployed digital products in the Service Delivery domain. Business relationship managers and customer service managers might sell or even consume elements of the Service Delivery domain. For more information, see [Service Consumption domain in the CSDM model](sell-consume-domain.md).

-   **Manage Portfolio domain**

    The Manage Portfolio domain is a layer on top of the CSDM conceptual model that interacts with the other CSDM domains. The typical user, a service owner, might be responsible for services in more than one domain. For more information, see [Manage Portfolio domain in the CSDM model](manage-business-services-domain.md).


## Services and service types

A service enables you to achieve the outcomes that you want with minimal risks and without ownership of specific costs and risks. \(This definition is consistent with the base definition of “service” in ITIL v3 and IT4IT.\) Services typically have three components: the interaction, the offering, and the service system.

The ServiceNow AI Platform includes the following base-system service types that you can extend to align with the service types in your organization.

-   **Technology management service \[cmdb\_ci\_service\_technical\] table \(formerly Technical service\)**

    Technology management services are the systems associated with the admins of CIs in the Service Delivery domain. Service instance owners, Technology management service owners, and Technology service owners. Technology management services are typically lower-level leaf nodes of one or more business services or business service instances in a structured hierarchy.

    -   Technology management services are operational CIs.
    -   A Technology management service must be a one-level service and not a hierarchy of Technology management services.
    -   Technology management services are used for impact in Incident Management, Problem Management, and Change Management. Also used for approvals for Change Management.
    -   Technology management services must be provider-focused and include the technology provided for the business to consume or sell.
    For more information, see [Manage Portfolio domain in the CSDM model](manage-business-services-domain.md).

-   **Service Instances — Service Instance \(called application service before CSDM v5\) \[cmdb\_ci\_service\_auto\] table**

    A service instance is a logical representation of a deployed application stack. Because service instances are logical in nature, they should use the Logical life-cycle value pairs. Service instances follow the same life-cycle guidance as any other logical CI.

    -   A service instance is an operational CI and a unique instance of an application.
    -   Used in Incident Management, Problem Management, and Change Management.
    -   Can be created for each region and each environment \(Development, QA, and Production\).
    -   Can be created via manual mapping, service mapping with entry point, and dynamic query.
    For more information about leaf nodes and structured hierarchies, see [Design &amp; Planning domain in the CSDM model](design-domain.md).

    You can monitor service instances \(called application service before CSDM v5\) on the Application Services dashboard. For more information, see [Use Service instance \(Application Services\) dashboard to monitor health](../../configuration-management/task/app-service-dashboard.md).

-   **Business services \(cmdb\_ci\_service\_business\)**

    A business service is a service type that is published to business users. A business service typically implements one or more business capabilities.

    Usually, business users order business services. Business users can select the desired offering and service commitment levels via the Service Catalog. For example, procurement, shipping, and finance.

    -   A business service is an operational CI.
    -   A business service must be a one-level service and not a hierarchy of business services.
    -   A business service can be used for impact in Incident Management, Problem Management, and Change Management and for approvals for Change.
    -   A business service must be focused on the consumer or seller.
    For more information, see [Service Consumption domain in the CSDM model](sell-consume-domain.md).


## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

-   **[Foundation domain in the CSDM model](foundation-domain.md)**  
Tables in the Foundation domain contain base data that is referenced from or to objects in the other CSDM domains. Before you can use ServiceNow products, you must populate foundational data.
-   **[Ideation &amp; Strategy domain in the CSDM model](ideation-strategy-domain.md)**  
The Ideation &amp; Strategy domain represents the ideas, concepts, and considerations for both the creation of new or additional services as well as improvements and enhancements to existing services. These capabilities are part of Strategic Portfolio Management \(SPM\).
-   **[Design &amp; Planning domain in the CSDM model](design-domain.md)**  
Enterprise architects and digital product owners work on the design and planning of digital products that your organization can either buy or build.
-   **[Build &amp; Integration domain in the CSDM model](build-domain.md)**  
Development teams use the tables in the Build &amp; Integration domain during the build effort \(systems development life cycle — AGILE DEVELOPMENT\) of digital products. The tables represent the logical development details of the enterprise applications \(digital products\) to be deployed and used by your organization. These are not operational CIs.
-   **[Service Delivery domain in the CSDM model](manage-tech-servs-domain.md)**  
The Service Delivery domain represents the overall end-to-end service delivery system that includes the infrastructure, technologies, integration patterns \(infrastructure, systems, data, processes, dependency models\), service delivery networks, and operational models. Together, these items deliver the services that conform to CSDM to internal and external users and organizations.
-   **[Service Consumption domain in the CSDM model](sell-consume-domain.md)**  
Internal or external consumers can request business services through the request catalogs in the Service Consumption domain. The business service offerings in the request catalogs are the deployed digital products in the Service Delivery domain. Business relationship managers and customer service managers might sell or even consume elements of the Service Delivery domain.
-   **[Manage Portfolio domain in the CSDM model](manage-business-services-domain.md)**  
The Manage Portfolio domain is a layer on top of the CSDM conceptual model that interacts with the other CSDM domains. The typical user, a service owner, might be responsible for services in more than one domain.

**Parent Topic:**[Exploring the CSDM model](csdm-content-frame-exploring.md)

