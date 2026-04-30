---
title: Common Service Data Model — conceptual model
description: The CSDM is the data framework that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform products, apps, and features.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Explore, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Common Service Data Model — conceptual model

The CSDM is the data framework that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform products, apps, and features.

## CSDM domains

Each domain is associated with one or more products, services, or service types, each of which you can extend as needed. Every box in the diagram \(except Request Catalog Item\) represents CIs in the CMDB. Roles and user types appear next to their area of responsibility.

![CSDM conceptual model.](../image/csdm-model-40.png)

![CSDM domains with standard color-coding as described in the following list.](../image/csdm-high-level-domain-desc.png)

-   **Foundation domain**

    The Foundation domain involves tables that contain base data that is referenced from or to objects in the other CSDM domains. Foundation data is required before you can use ServiceNow products or add data to the CMDB. See [Foundation domain in the CSDM framework](foundation-domain.md)

-   **Design domain**

    The Design domain supports the design and planning of digital products. CIs in the Design domain aren’t operational, so you can’t select them for Incident Management, Problem Management, or Change Management. Enterprise architects and application owners are the typical users of tables in this domain. See [Design domain in the CSDM framework](design-domain.md).

-   **Build domain**

    The Build domain involves the tables that are used in the build effort \(systems development life cycle — SDLC or Agile Development\) of digital products like DevOps. The tables represent the logical development details of the enterprise applications \(digital products\) to be deployed and used by the business. These are not operational CIs. See [Build domain in the CSDM framework](build-domain.md).

-   **Manage Technology Management Services domain**

    The Manage Technology Management Services domain involves the tables used by IT Operations Management \(ITOM\) products such as Service Mapping and Discovery. These are deployed instances of digital products and their related and discoverable components and documentation of the services that provide and support the deployed instances. See [Manage Technology Management Services domain in the CSDM framework](manage-tech-servs-domain.md).

-   **Sell / Consume domain**

    The Sell/Consume domain involves the tables used by Service Portfolio Management \(Service Portfolio Management\) and Customer Service Management \(CSM\). This is the portfolio and request catalog of business service offerings that depend on the deployed digital products. See [Sell/Consume domain in the CSDM framework](sell-consume-domain.md).

-   **Manage Portfolio domain**

    The Manage Portfolio domain is a layer on top of the CSDM conceptual model that interacts with the other CSDM domains. The typical user, a service owner, might be responsible for services in more than one domain. See [Manage Portfolio domain in the CSDM framework](manage-business-services-domain.md).


## Services and service types

A service enables you to achieve the outcomes that you want with minimal risks and without ownership of specific costs and risks. This definition is consistent with the base definition of service in ITIL v3 and IT4IT. Services typically have three components: the interaction, the offering, and the service system.

The ServiceNow AI Platform includes the following base-system service types that you can extend to align with the service types in your organization.

-   **Service Instances \[cmdb\_ci\_service\_auto\] table \(formerly Application Service table\)**

    A service instances is a logical representation of a deployed application stack. Because service instances are logical in nature, they should use the Logical life-cycle value pairs. Service instances follow the same life-cycle guidance as any other logical CI.

    -   A service instance is an operational CI and a unique instance of an application.
    -   Used in Incident Management, Problem Management, and Change Management.
    -   Can be created for each region and each environment \(Development, QA, and Production\).
    -   Can be created via manual mapping, service mapping with entry point, and dynamic query.
    For more information about leaf nodes and structured hierarchies, see [Design domain in the CSDM framework](design-domain.md).

    You can monitor service instances \(formerly application services — renamed in CSDM v5\) on the Application Services dashboard. See [Monitor the health of application services on the Application Services dashboard](../../configuration-management/task/app-service-dashboard.md).

-   **Business services \[cmdb\_ci\_service\_business\]**

    A business service is a service type that is published to business users. A business service typically implements one or more business capabilities.

    Usually, business users order business services. Business users can select the desired offering and service commitment levels via the Service Catalog. For example, procurement, shipping, and finance.

    -   A business service is an operational CI.
    -   A business service must be a one-level service and not a hierarchy of business services.
    -   A business service can be used for impact in Incident, Problem, and Change and for approvals for Change.
    -   A business service must be focused on the consumer or seller.
    See [Sell/Consume domain in the CSDM framework](sell-consume-domain.md).

-   **Technology management service \[cmdb\_ci\_service\_technical\] table \(formerly Technical service\)**

    Technology management services are the systems associated with the admins of CIs in the Manage Technology Management Services domain: Service instance owners, Technology management service owners, and Technology service owners\). Technology management services are typically lower-level leaf nodes of one or more business services or service instances in a structured hierarchy.

    -   Technology management services are operational CIs.
    -   A technology management service must be a one-level service and not a hierarchy of technology management services.
    -   Technology management services are used for impact in Incident Management, Problem Management, and Change Management. Also used for approvals for Change Management.
    -   Technology management services must be provider-focused and include the technology provided for the business to consume or sell.
    See [Manage Technology Management Services domain in the CSDM framework](manage-tech-servs-domain.md).


## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

-   **[Foundation domain in the CSDM framework](foundation-domain.md)**  
The Foundation domain involves tables that contain base data that is referenced from or to objects in the other CSDM domains. Foundation data is required before you can use ServiceNow products or add data to the CMDB.
-   **[Design domain in the CSDM framework](design-domain.md)**  
The Design domain supports the design and planning of digital products. CIs in the Design domain aren’t operational, so you can’t select them for Incident Management, Problem Management, or Change Management. Enterprise architects and application owners are the typical users of tables in this domain.
-   **[Build domain in the CSDM framework](build-domain.md)**  
The Build domain involves the tables that are used in the build effort \(systems development life cycle — SDLC or Agile Development\) of digital products like DevOps. The tables represent the logical development details of the enterprise applications \(digital products\) to be deployed and used by the business. These are not operational CIs.
-   **[Manage Technology Management Services domain in the CSDM framework](manage-tech-servs-domain.md)**  
The Manage Technology Management Services domain involves the tables used by IT Operations Management \(ITOM\) products such as Service Mapping and Discovery. These are deployed instances of digital products and their related and discoverable components and documentation of the services that provide and support the deployed instances.
-   **[Sell/Consume domain in the CSDM framework](sell-consume-domain.md)**  
The Sell and Consume domain represents the portfolio of business services that may sell or consume elements of the Manage Technology Management Services domain. The Sell/Consume domain involves the tables used by Service Portfolio Management \(Service Portfolio Management\) and Customer Service Management \(CSM\). This is the portfolio and request catalog of business service offerings that depend on the deployed digital products.
-   **[Manage Portfolio domain in the CSDM framework](manage-business-services-domain.md)**  
The Manage Portfolio domain is a layer on top of the CSDM conceptual model that interacts with the other CSDM domains. The typical user, a service owner, might be responsible for services in more than one domain.

**Parent Topic:**[Exploring the CSDM framework](csdm-content-frame-exploring.md)

