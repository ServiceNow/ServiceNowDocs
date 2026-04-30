---
title: Manage Technology Management Services domain in the CSDM framework
description: The Manage Technology Management Services domain involves the tables used by IT Operations Management \(ITOM\) products such as Service Mapping and Discovery. These are deployed instances of digital products and their related and discoverable components and documentation of the services that provide and support the deployed instances.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [CSDM data domains, Explore, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage Technology Management Services domain in the CSDM framework

The Manage Technology Management Services domain involves the tables used by IT Operations Management \(ITOM\) products such as Service Mapping and Discovery. These are deployed instances of digital products and their related and discoverable components and documentation of the services that provide and support the deployed instances.

The CIs in this domain are discovered items such as installed applications, servers, and network components. The Manage Technology Management Services domain also represents the portfolio of technology management services in use. These services are operational, which means that you can select them for ITSM Incident Management, Problem Management, or Change Management.

Typical users are service instance owners \(for the application and platform\) and technology service owners \(for the infrastructure and delivery\). Technology consumers can request technical service offerings through the request catalog. Catalogs are described in detail in [Service Catalog](../../service-catalog-management/concept/service-catalog.md).

![Manage Technology Management Services domain.](../image/manage-tech-services-domain.png)

The tables in the Manage Technology Management Services domain represent the technology that your business sells or consumes in the provider view. Service Mapping and Discovery populate the tables. They also enable you to manage CIs and their relationships. Those products accelerate the process and minimize errors, but you aren’t required to use them. The domain includes the following tables:

-   Technology management service \[cmdb\_ci\_service\_technical\] table \(formerly Technical service — renamed in CSDM v5\)
-   Technical service offering \[service\_offering\] table
-   Request catalog.
-   Dynamic CI group \[cmdb\_ci\_query\_based\_service\] table. Technology management services in Event Management use the cmdb\_ci\_query\_based\_service table.
-   Mapped Application Service \[cmdb\_ci\_service\_discovered\] table \(included in the base system\)

## Technology management services

Technology management services are associated with service owners and are typically layered under one or more business services or service instances. A technology management service may have one or more technology management offerings.

Users of technology management services can view and manage the technologies that you provide to the business. Event Management enables you to monitor service performance. You can also use Event Management to identify health issues for related infrastructure CIs and service instances.

Technology management services can be managed as part of the Service Portfolio in the Sell/Consume domain \(that is, a Service Portfolio hierarchy can be referenced from a technology management service\). This allows for a more complete hierarchy and management of both technology management services and business services within the Service Portfolio Management workspace and related workspaces. You can make better decisions when you know how spend on technology management services can improve performance and reliability of your business services.

**Note:** Business services and technology management services connect to the spm\_service\_portfolio through the spm\_taxonomy\_node. See [Service Portfolio Management taxonomy](https://www.servicenow.com/docs/access?context=SPM2-taxonomy&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

## Technology management offerings

Technology consumers can request technology management offerings \(TMO\) through the request catalog. Catalogs are described in detail in [Service Catalog](../../service-catalog-management/concept/service-catalog.md). The consumer can typically select the following features and options:

-   Level of performance
-   Location or geography
-   Environment
-   Pricing
-   Availability
-   Capability
-   Support group \(for incident\)
-   Technical approval group \(for change\)
-   Packaging options \(commitments\)

Technology management offerings typically have the following components:

-   **One or more service commitments**

    A service commitment defines the service delivery obligations agreed to between the consumer and the provider. Service commitments uniquely define the level of service in terms of availability, criticality, scope, pricing, and other factors. For example, an organization may offer two levels of support for a service instance:

    -   Support for a production-level offering: Provides a high level of availability and criticality for production instances. Includes a 24/7, 5-minute response time guarantee \(24 hours per day seven days per week\).
    -   Support for a non-production-level offering: Limited availability and criticality for non-production instances. Includes a 60-minute response time guarantee between 8:00 a.m. and 5:00 p.m., Monday through Friday.
-   **A service offering subscription that records which users have access to an offering**

    A technology management offering references the **Service Categorization** attribute in service tables to denote whether a technology management offering or offering is related to a business service or to a technology management service. Technology management offerings that are mapped to the \[service\_offering\] table are classified as “technology management service" and are derived from the service. The technology management offering is based on how the parent serves a specific technical need. Every technology management service should have at least one technology management offering.

    **Important:** Each CI associated through a Dynamic CI Group can be related to only one technology management service or technology management offering. Conflicts can result when one service includes multiple offerings with different SLAs, OLAs, Support Groups, and commitments.


## Dynamic CI groups

A dynamic CI group is comprised of CIs that result from a CMDB Groups query. For example, you can create a dynamic CI group based on location: "all web servers in Detroit" or "all Oracle databases in Mumbai".

**Note:** Dynamic CI groups contain only CIs and can't contain other CI groups.

Dynamic CI groups are mapped to the \[cmdb\_ci\_query\_based\_service\] table and are classified as either service instance or technology management service, as applicable. You might want to use dynamic CI groups in the following situations:

-   **Query-based service instance**

    You don’t have Service Mapping enabled yet, but you have 12 servers and three database instances in MyAppServiceProd. You can replace your spreadsheets with a dynamic CI group as a service instance.

    See [Populate an application service using the Dynamic CI Group method](../../configuration-management/task/populate-app-service-dynamic-group.md).

-   **Managed group of Infrastructure CIs**

    The web servers in Detroit are managed by the DetroitRockCity Technical service offering. Instead of manually creating relationships from Technical service offerings to Infrastructure CIs, use a dynamic CI group. A single relationship from your Technical service offering CI \(DetroitRockCity\) to your dynamic CI Group \(web servers in Detroit\) gives you the visibility you need.

-   **A way to manage patches for your CIs**

    In Change Management, you can select the dynamic CI group for the CIs you need to update and use a business rule to auto-populate the **Affected CI** field.


## Service instances \(formerly application services\)

The Service Instance \[cmdb\_ci\_service\_auto\] table \(formerly Application Service table — renamed in CSDM v5\) supports service instances. A service instance is a set of interconnected applications and hosts that are configured to offer a service. A service instance is a logical representation of a deployed system or an application stack. Using service instances, you can view maps and change history for services. For example, the Event Management application can monitor service performance and identify health issues for service instances.

Service instances can be internal, like an organization's email system or customer-facing, like an organization's website. For example, creating financial reports through a web-based application requires a computer, web server, application server, databases, middleware, and network infrastructure. The applications and hosts are configured to offer the service of financial reporting. A service instance represents an instance of such a business application or system in the development, test, or production environment.

Service instances are the entry points for the Service Mapping feature. Service instances underpin a business or technology management service and are mapped to the CMDB Service Instance \[cmdb\_ci\_service\_auto\] table \(formerly Application Service table — renamed in CSDM v5\) for common reporting.

Service instances are key relationship entities for IT Service Management \(ITSM\), IT Operations Management \(ITOM\), Strategic Portfolio Management \(SPM\), and Customer Service Management \(CSM\).

Service instances include relationships between business applications, business services, technology management services, applications, and infrastructure CIs. You can expose a service instance by using the related business or technical service offering. For more information, see [Monitor the health of application services on the Application Services dashboard](../../configuration-management/task/app-service-dashboard.md).

The table that a service instance maps to depends on the method used to create it:

|Method used to create the service instance|Mapped to table|
|------------------------------------------|---------------|
|Top Down Discovery \(Service Mapping\)|cmdb\_ci\_service\_discovered|
|Dynamic CI Group \(Query-based\)|cmdb\_ci\_query\_based\_service|
|Tags|cmdb\_ci\_service\_tags|
|Manual entry, using the Create a Service Instance form \(formerly, the Create an Application Service form — renamed in CSDM v5\)|cmdb\_ci\_service\_discovered|

-   For more information about service instances and the methods you can use to create them, see [Application services](../../configuration-management/concept/application-services.md) and [Create an application service](../../service-mapping/task/create-it-services.md).
-   You can specify required attributes for service instances. See [Specifying attributes and relationships for service instances](csdm-module-app-service-settings.md) and [Modify the attributes and relationships required for application services](../../configuration-management/task/modify-req-fields-appservice.md).
-   You can set a relationship between a service instance and the components of other CSDM domains. See [Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

## Applications

An application is any program or module that defines behavior and performs a specific function. Applications are typically discoverable instances and provide a specific set of functions for one or more services.

-   The application table and extended tables contain uniquely discovered instances of code in use on the host.
-   Applications are considered infrastructure CIs.
-   The instance is limited to the applications on a single host. This limitation ensures that applications are uniquely identified during discovery.
-   There's a one-to-many \(and not a one-to-one\) relationship between the application and the service instance. A single installed application, such as a database instance, may support multiple service instances depending on the configuration and the use of the applications.

**Note:** The application table \[cmdb\_ci\_appl\] isn't an inventory or portfolio of your applications. Don't make the mistake of storing managed application details in the application table. Those details \(inventory or application portfolio objects\) belong in the business application table \(as documented in [Design domain in the CSDM framework](design-domain.md)\).

## Infrastructure CIs

Infrastructure CIs are managed physical and logical components. A CI can be a single module, such as a server, database, or a router or a complete system such as a web server, database, or infrastructure.

The underlying infrastructure components or CIs can be complicated. The complexity increases as data structures are layered on top of physical CIs. For that reason, you should work with a business relationship manager or enterprise architect to define your business capabilities and business applications.

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[Common Service Data Model — conceptual model](csdm-conceptual-model.md)

