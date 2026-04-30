---
title: Service Consumption domain in the CSDM model
description: Internal or external consumers can request business services through the request catalogs in the Service Consumption domain. The business service offerings in the request catalogs are the deployed digital products in the Service Delivery domain. Business relationship managers and customer service managers might sell or even consume elements of the Service Delivery domain.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [CSDM data domains, Explore, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Consumption domain in the CSDM model

Internal or external consumers can request business services through the request catalogs in the Service Consumption domain. The business service offerings in the request catalogs are the deployed digital products in the Service Delivery domain. Business relationship managers and customer service managers might sell or even consume elements of the Service Delivery domain.

## Tables in the Service Consumption domain

Tables in the Service Consumption domain are used by Service Portfolio Management and Customer Service Management \(CSM\). You can select the tables in the Service Consumption domain to use with Incident Management and Change Management.

![Service Consumption domain of the CSDM framework.](../image/domain-service-consumption-tables.png)

The Service Consumption domain includes the following tables:

-   The Business Service \[cmdb\_ci\_service\_business\] table \(**Service Classification** is Business Service\) extends the core Service \[cmdb\_ci\_service\] table. For example, a service might be "Manage HR".

    **Note:** Before the Business Service table was added, all Business Services existed in the Service table. In the future, all Business Services might migrate from core cmdb\_ci\_service to cmdb\_ci\_service\_business. Until then, both tables operate identically.

-   The Business Service offering \[service\_offering\] table holds the offerings that consumers can select in the catalog. Taken together, the business service offerings make up the business service. In our HR example, offerings might be "Manage Onboarding" and "Manage Interviews". Each offering has a **Depends on::Used by** relationship with a service instance in the Service Delivery domain.
-   Service Catalog \[sc\_catalog\] table. The Service Catalog tables hold the business service offerings that consumers can select.

-   Business capability **Provided By::Provides** Business service
-   Service portfolio \(reference attribute\) Business service
-   Business service \(reference attribute\) Business service offering
-   Business service offering **Depends on::Used by** Service instance

You're not required to use Service Portfolio Management or CSM to use the referenced tables, but those products enable you to manage workflows and report service-related data.

## Tables used during the Service Consumption phase of the service life cycle

![Service Consumption tables in the service life cycle.](../image/service-lifecycle-svc-consumption.png)

## Business service offerings

Business service offerings \(**Service Classification** is Business Service\) are the starting point for configuring Service Portfolio Management. Business service offerings inherit from Business Services. Business service offerings consist of one or more service commitments that define the level of service in terms of availability, scope, pricing, and other factors. For example, an organization might offer two levels of desktop support:

-   A silver offering of upgrades and virus protection.
-   A gold offering with the silver commitments plus a response time guarantee of 30 minutes between the hours of 8:00 a.m. and 5:00 p.m., Monday through Friday.

**Note:** Business services and technology management services connect to the spm\_service\_portfolio through the spm\_taxonomy\_node. See [Service Portfolio Management taxonomy](https://www.servicenow.com/docs/access?context=SPM2-taxonomy&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

Business service offerings have the following characteristics:

-   Business service offerings tailor the service by capability, availability, pricing, and packaging options. You can use the service offering to set different levels of performance and features for a particular service.
-   Business service offering commitments define the agreed-upon service delivery obligations.
-   Business service offering subscriptions record which users have access to an offering.
-   Business service offerings are the CMDB records that identify the specific business area and the entity where the service is delivered. Some business services and service offerings depend on the service instance.
-   Business service offerings are derived from the service and are refined depending on how the parent serves a particular business need.

**Note:** You should configure at least one business service offering for each operational business service or technology management service.

You can view your business service offerings in the Digital Portfolio Management \(DPM\).

![Service Offering view in the Digital Portfolio Management (DPM).](../image/service-offering-form.png)

Business service offerings typically have different service-level agreements \(SLAs\) depending on their commitments. Without a business service offering, SLAs remain at a process level only. For example, the SLA stays at a P1 incident or a minor change, and doesn't refer to the affected business service offering.

You can represent business services and business service offerings as catalog items in the service catalog to make them available for consumers.

## Business services

A business service is associated with business users and is typically layered beneath one or more business capabilities. A business service can contain one or more business service offerings.

Business consumers can use the request catalog to order business services, business service offerings, and service commitment levels. Catalogs are described in detail in [Service Catalog](../../service-catalog-management/concept/service-catalog.md). Business services are mapped to the cmdb\_ci\_service\_business table and are classified as “business services.”

## Service portfolios

A service portfolio is a hierarchical collection of business services, products, projects, or applications. A portfolio can represent a strategic business objective and enables you to manage all included items as a group \(for example, life cycles\). Items are organized into the following categories:

-   Objective \(business intent\)
-   Capability
-   Organization \(for example, enterprise resource planning \[ERP\] or financial management\)
-   Geography \(location\)

## Catalogs

A request catalog enables consumers to order and manage business and technical products, services, service commitment options, and offerings \(for example, the Human Resources \[HR\] service catalog\). Catalogs contain catalog items and are the starting point for consumers to access available services. Catalogs are described in [Service Catalog](../../service-catalog-management/concept/service-catalog.md).

**Catalog Item**

A catalog item is an item or a service that a consumer can request from the catalog. A service can contain multiple catalog items \(for example, the employee onboarding catalog\). Catalog items are listed on the service portal and are available to the users that need them \(either through subscription or job responsibility\). Each catalog item is linked to one business service offering.

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[CSDM data domains](csdm-conceptual-model.md)

