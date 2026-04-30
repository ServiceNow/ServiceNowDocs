---
title: Sell/Consume domain in the CSDM framework
description: The Sell and Consume domain represents the portfolio of business services that may sell or consume elements of the Manage Technology Management Services domain. The Sell/Consume domain involves the tables used by Service Portfolio Management \(Service Portfolio Management\) and Customer Service Management \(CSM\). This is the portfolio and request catalog of business service offerings that depend on the deployed digital products.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [CSDM data domains, Explore, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Sell/Consume domain in the CSDM framework

The Sell and Consume domain represents the portfolio of business services that may sell or consume elements of the Manage Technology Management Services domain. The Sell/Consume domain involves the tables used by Service Portfolio Management \(Service Portfolio Management\) and Customer Service Management \(CSM\). This is the portfolio and request catalog of business service offerings that depend on the deployed digital products.

Typical users are the business relationship manager and the customer service manager. Business consumers can request business services through the request catalog. Catalogs are described in detail in [Service Catalog](../../service-catalog-management/concept/service-catalog.md). You're not required to use Service Portfolio Management or CSM to use the referenced tables, but those products enable you to manage workflows and report service-related data.

![Sell/Consume domain.](../image/sell-consume-domain.png)

The Sell/Consume domain includes the following tables:

-   Business service offering table \[service\_offering\].
-   The Business Service table \[cmdb\_ci\_service\_business\] extends the core Service table \[cmdb\_ci\_service\].

    **Note:** Before the Business Service table was added, all Business Services existed in the Service table. In the future, all Business Services might migrate from core cmdb\_ci\_service to cmdb\_ci\_service\_business. Until then, both tables operate identically.

-   Service portfolio table \[spm\_service\_portfolio\]. The Service portfolio table is not a CMDB table.

You can select the tables in the Sell/Consume domain to use with Incident Management and Change Management.

## Business service offerings

Business service offerings are the starting point for configuring Service Portfolio Management. Business service offerings inherit from Business Services. Business service offerings consist of one or more service commitments that define the level of service in terms of availability, scope, pricing, and other factors. For example, an organization might offer two levels of desktop support:

-   A silver offering of upgrades and virus protection.
-   A gold offering with the silver commitments plus a response time guarantee of 30 minutes between the hours of 8:00 a.m. and 5:00 p.m., Monday through Friday.

**Note:** Business services and technology management services connect to the spm\_service\_portfolio through the spm\_taxonomy\_node. See [Service Portfolio Management taxonomy](https://www.servicenow.com/docs/access?context=SPM2-taxonomy&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

Business service offerings have the following characteristics:

-   Business service offerings tailor the service by capability, availability, pricing, and packaging options. You can use the service offering to set different levels of performance and features for a particular service.
-   Business service offering commitments define the agreed-upon service delivery obligations.
-   Business service offering subscriptions record which users have access to an offering.
-   Business service offerings are the CMDB records that identify the specific business area and the entity where the service is delivered. Some business services and service offerings depend on the service instance.
-   Business service offerings are derived from the service and are refined depending on how the parent serves a particular business need.

**Note:** You should configure at least one service offering for each operational business service or technology management service.

You can view your business service offerings in the Digital Portfolio Management \(DPM\).

![Service Offering view in the Digital Portfolio Management (DPM).](../image/service-offering-form.png)

Business service offerings typically have different service-level agreements \(SLAs\) depending on their commitments. Without a business service offering, SLAs remain at a process level only. For example, the SLA stays at a P1 incident or a minor change, and doesn't refer to the affected service offering.

You can represent business services and business service offerings as catalog items in the service catalog to make them available for consumers.

## Business services

A business service is associated with business users and is typically layered beneath one or more business capabilities. A business service can contain one or more business service offerings.

Business consumers can use the request catalog to order business services, business service offerings, and service commitment levels. Catalogs are described in detail in [Service Catalog](../../service-catalog-management/concept/service-catalog.md). Business services are mapped to the \[cmdb\_ci\_service\_business\] table and are classified as “business services.”

## Service portfolios

A service portfolio is a hierarchical collection of business services, products, projects, or applications. A portfolio can represent a strategic business objective and enables you to manage all included items as a group \(for example, life cycles\). Items are organized into the following categories:

-   Objective \(business intent\)
-   Capability
-   Organization \(for example, enterprise resource planning \[ERP\] or financial management\)
-   Geography \(location\)

## Request catalogs

A request catalog enables consumers to order and manage business and technical products, services, service commitment options, and offerings \(for example, the Human Resources \[HR\] service catalog\). Catalogs contain catalog items and are the starting point for consumers to access available services. Catalogs are described in detail in [Service Catalog](../../service-catalog-management/concept/service-catalog.md).

**Catalog Item**

A catalog item is an item or a service that a consumer can request from the catalog. A service can contain multiple catalog items \(for example, the employee onboarding catalog\). Catalog items are listed on the service portal and are available to the users that need them \(either through subscription or job responsibility\). Each catalog item is linked to one service offering.

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[Common Service Data Model — conceptual model](csdm-conceptual-model.md)

