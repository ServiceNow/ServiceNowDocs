---
title: Service Delivery domain in the CSDM model
description: The Service Delivery domain represents the overall end-to-end service delivery system that includes the infrastructure, technologies, integration patterns \(infrastructure, systems, data, processes, dependency models\), service delivery networks, and operational models. Together, these items deliver the CSDM-compliant services to internal and external users and/or organizations.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [CSDM data domains, Explore, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Delivery domain in the CSDM model

The Service Delivery domain represents the overall end-to-end service delivery system that includes the infrastructure, technologies, integration patterns \(infrastructure, systems, data, processes, dependency models\), service delivery networks, and operational models. Together, these items deliver the CSDM-compliant services to internal and external users and/or organizations.

## Tables in the Service Delivery domain

Users of tables in the Service Delivery domain provide and manage the operational environments and infrastructure that support your organization’s business applications \(as developed in the Build &amp; Integration domain\). Typical users are service instance owners \(for application and platform\) and service delivery owners or service providers \(for infrastructure and delivery\).

The tables in the Service Delivery domain represent the technology that your business sells or consumes in the provider view. Service Mapping and Discovery populate the tables. The tables in the domain also enable you to manage CIs and their relationships. The domain includes the following tables:

-   Technology management service \(formerly Technical service\) \[cmdb\_ci\_service\_technical\] table. The **Service Classification** is Technical Service.
-   Technology management offering \(formerly Technical service offering\) \[service\_offering\] table. The **Service Classification** is Technical Service.
-   Request catalog. Technology consumers can request technology management offerings through a request catalog. Catalogs are described in detail in [Service Catalog](../../service-catalog-management/concept/service-catalog.md).
-   Dynamic CI group \[cmdb\_ci\_query\_based\_service\] table. **Service Classification** is Technical Service. Technology management services in Event Management use the cmdb\_ci\_query\_based\_service table.
-   Service instance \(called application service before CSDM v5\) \[cmdb\_ci\_service\_auto\] tables. The **Service Classification** is Application Service.
    -   For manually-created and Service Mapping: Mapped Application Service \[cmdb\_ci\_service\_discovered\] table \(included in the base system\).
    -   When query-based: \[cmdb\_ci\_query\_based\_service\].
    -   When tag-based: \[cmdb\_ci\_service\_by\_tags\].

The CIs in this domain are deployed instances of digital products and their related and discoverable components \(such as installed applications, servers, and network components\) plus documentation of the services that provide and support the deployed instances. The domain also represents the portfolio of technology management services in use. For more information on life cycles, see [Definitions of life-cycle values for tangible/physical CIs](../reference/csdm-lifecycle-df-tangible-physical.md).

The services are operational, which means that you can select them for ITSM Incident Management, Problem Management, or Change Management.

![Service Delivery domain of the CSDM framework.](../image/domain-service-delivery-tables.png)

## Relationships between Service Delivery tables

-   SDLC component **Contains::Contained by** Service instance \(optional to use this item\).
-   Business application **Consumes::Consumed** by Service instance.
-   Service instance \(a logical representation of a deployed system or application stack\)**Depends on::Used by** /**Sends Data To::** Service instance.
-   Service instance **Depends on::Used by** Application.
-   Application **Runs on::Runs** Infrastructure CIs.
-   Technology management service uses a reference attribute to specify the relationship with Infrastructure Technology management offering. Published to service owners and typically underpins one or more business services. A Technology management service may have an operational view made up of one or more Technology management offerings.
-   Technology management offering **Contains::Contained by** Service instance. Stratification of the Technical Service into options, including localization/geography, environment, pricing, availability, capability, support group \(INCIDENT\), technical approval group \(CHANGE\) and packaging options.
-   Technology management offering **Contains::Contained by** Dynamic CI Group.
-   Dynamic CI Group \(a dynamic grouping of CIs, based on results of CMDB Groups queries\) uses a related list to specify the relationship with Infrastructure CIs.
-   Business Service Offering **Depends on::Used by** Service instance.

**Note:** Business services and technology management services connect to the spm\_service\_portfolio through the spm\_taxonomy\_node. See [Service Portfolio Management taxonomy](https://www.servicenow.com/docs/access?context=SPM2-taxonomy&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

## Tables used during the Service Delivery phase of the service life cycle

![Service Delivery tables in the service life cycle.](../image/service-lifecycle-service-delivery.png)

## Tables used during the Service Delivery phase of the service life cycle

![Service Delivery tables in the service life cycle.](../image/service-lifecycle-svc-deliv-srv-inst.png)

## AI component tables used during the Service Delivery phase of the service life cycle

![AI component tables in the Service Delivery phase.](../image/service-lifecycle-tech-net-tables.png)

API: The API data model is made available within the CMDB to assist in managing your API data. As part of API Insights, you can centralize your management of APls including, but not limited to, viewing API details, comparing APls, identify and resolve data gaps, and manage service relationships. API Function: from a virtual perspective. API Application: From an on-premises perspective.

Al Function: Al SaaS applications deployed on public cloud platforms that offer scalable, on-demand services for machine learning, data processing, and Al-driven tasks. The applications provide flexible solutions without the need for on-premises infrastructure management.

Al Application: Al software applications that can run on various platforms such as Linux, Windows, Docker containers, or Kubernetes \(K8\) clusters. The platforms support diverse Al workloads, including machine learning models, data analytics, and intelligent services or Al- enabled applications.

## Technology management services

Technology management services are associated with service owners and are typically layered under one or more business services or service instances. A technology management service may have one or more technology management offerings.

Users of technology management services can view and manage the technologies that you provide to the business. Event Management enables you to monitor service performance. You can also use Event Management to identify health issues for related infrastructure CIs and service instances.

Technology management services can be managed as part of the Service Portfolio in the Service Consumption domain \(that is, a Service Portfolio hierarchy can be referenced from a technology management service\). This allows for a more complete hierarchy and management of both technology management services and business services within the Service Portfolio Management workspace and related workspaces. You can make better decisions when you know how spend on technology management services can improve performance and reliability of your business services.

**Note:** Business services and technology management services connect to the spm\_service\_portfolio through the spm\_taxonomy\_node. See [Service Portfolio Management taxonomy](https://www.servicenow.com/docs/access?context=SPM2-taxonomy&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

## Technology management offerings

Technology consumers can request technology management offerings \(TMO\) through the request catalog. Catalogs are described in [Service Catalog](../../service-catalog-management/concept/service-catalog.md). The consumer can typically select the following features and options:

-   Level of performance
-   Location or geography
-   Environment
-   Pricing
-   Availability
-   Capability
-   Support group \(for incident\)
-   Technical approval group \(for change\)
-   Packaging options \(commitments\)

**Tip:** Use dynamic CI groups to significantly improve management. For more information, see [Synchronize user groups for a technology management offering](../task/csdm-enable-tso.md).

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

    See [Use the Dynamic CI Group method to populate application services](../../configuration-management/task/populate-app-service-dynamic-group.md).

-   **Managed group of Infrastructure CIs**

    The web servers in Detroit are managed by the DetroitRockCity technology management offering. Instead of manually creating relationships from technology management offerings to Infrastructure CIs, use a dynamic CI group. A single relationship from your technology management offering CI \(DetroitRockCity\) to your dynamic CI Group \(web servers in Detroit\) gives you the visibility you need.

-   **A way to manage patches for your CIs**

    In Change Management, you can select the dynamic CI group for the CIs you need to update and use a business rule to auto-populate the **Affected CI** field.


## Service instances \(called application services before CSDM v5\)

Service instance a relabel of \[cmdb\_ci\_service\_auto\], which previously was called application service.

Application services still exist. They were always there as extended tables depending on how you managed that application service.

For manual creation or service mapping, you go into the mapped application service.

For tag-based, it would live in the tag-based application service table. The tables still exist and they are still application services and you are still gonna go to the application service wizard to create application services.

New types of service instances are extensions of \[cmdb\_ci\_service\_auto\]:

-   Data service instance \[cmdb\_ci\_data\_service\_instance\]
-   Network service instance \[cmdb\_ci\_network\_service\_instance\]
-   Operational Process service instance \[cmdb\_ci\_operational\_process\_service\_instance\]
-   Connection service instance \[cmdb\_ci\_connection\_service\_instance\]
-   Facility service instance \[cmdb\_ci\_facility\_service\_instance\]

The Service Instance \(called application service before CSDM v5\) \[cmdb\_ci\_service\_auto\] table supports service instances. A service instance is a set of interconnected applications and hosts that are configured to offer a service. A service instance is a logical representation of a deployed system or an application stack. Using service instances, you can view maps and change history for services. For example, the Event Management application can monitor service performance and identify health issues for service instances.

Service instances can be internal, like an organization's email system or customer-facing, like an organization's website. For example, creating financial reports through a web-based application requires a computer, web server, application server, databases, middleware, and network infrastructure. The applications and hosts are configured to offer the service of financial reporting. A service instance represents an instance of such a business application or system in the development, test, or production environment.

Service instances are the entry points for the Service Mapping feature. Service instances underpin a business or technology management service and are mapped to the CMDB Service Instance \(called application service before CSDM v5\) \[cmdb\_ci\_service\_auto\] table for common reporting.

Service instances are key relationship entities for IT Service Management \(ITSM\), IT Operations Management \(ITOM\), Strategic Portfolio Management \(SPM\), and Customer Service Management \(CSM\).

Service instances include relationships between business applications, business services, technology management services, applications, and infrastructure CIs. You can expose a service instance by using the related business or technology management offering. For more information, see [Use Application Services dashboard to monitor health](../../configuration-management/task/app-service-dashboard.md).

Types of service instance in the Service Instance data model:

-   Data service instance
-   Network service instance
-   Operational Process service instance
-   Connection service instance
-   Facility service instance

The table that a service instance maps to depends on the method used to create it:

|Method used to create the service instance|Mapped to table|
|------------------------------------------|---------------|
|Top Down Discovery \(Service Mapping\)|cmdb\_ci\_service\_discovered|
|Dynamic CI Group \(Query-based\)|cmdb\_ci\_query\_based\_service|
|Tags|cmdb\_ci\_service\_tags|
|Manual entry, using the Create a Service Instance form \(formerly, the Create an Application Service form\)|cmdb\_ci\_service\_discovered|

-   For more information about service instances and the methods you can use to create them, see [Application services](../../configuration-management/concept/application-services.md) and [Create an application service](../../service-mapping/task/create-it-services.md).
-   You can specify required attributes for service instances. For more information, see [Modify the attributes and relationships required for application services](../../configuration-management/task/modify-req-fields-appservice.md).
-   You can set a relationship between a service instance and the components of other CSDM domains. See [Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

## Applications

An application is any program or module that defines behavior and performs a specific function. Applications are typically discoverable instances and provide a specific set of functions for one or more services.

-   The application table and extended tables contain uniquely discovered instances of code in use on the host.
-   Applications are considered infrastructure CIs.
-   The instance is limited to the applications on a single host. This limitation ensures that applications are uniquely identified during discovery.
-   There's a one-to-many \(and not a one-to-one\) relationship between the application and the service instance. A single installed application, such as a database instance, may support multiple service instances depending on the configuration and the use of the applications.

**Note:** The application table \[cmdb\_ci\_appl\] isn't an inventory or portfolio of your applications. Don't make the mistake of storing managed application details in the application table. Those details \(inventory or application portfolio objects\) belong in the business application table \(as documented in [Design &amp; Planning domain in the CSDM model](design-domain.md)\).

## Infrastructure CIs

Infrastructure CIs are managed physical and logical components. A CI can be a single module, such as a server, database, or a router or a complete system such as a web server, database, or infrastructure.

The underlying infrastructure components or CIs can be complicated. The complexity increases as data structures are layered on top of physical CIs. For that reason, you should work with a business relationship manager or enterprise architect to define your business capabilities and business applications.

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[CSDM data domains](csdm-conceptual-model.md)

**Related topics**  


[Synchronize user groups for a technology management offering](../task/csdm-enable-tso.md)

