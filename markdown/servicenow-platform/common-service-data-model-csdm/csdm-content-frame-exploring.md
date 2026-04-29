---
title: Exploring the CSDM model
description: The CSDM is the data model that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB help to promote that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring the CSDM model

The CSDM is the data model that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB help to promote that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.

## Definitions of CSDM terms

See [CSDM terms](../reference/csdm-term-definitions.md).

## Goal of following the CSDM guidelines

Following the CSDM data model helps you to accurately and completely capture the data objects that help you to run your business.

CSDM provides guidance on where to put data in the platform. Because there are multiple ways to identify and use data, the CSDM guidelines help you to determine the best data structures for supporting your organization's services.

## Kinds of data

The CMDB holds data for several purposes.

-   Foundation \(core CMDB population and relationship integrity\)
-   Asset management \(hardware or software asset tracking, license alignment\)
-   Process enablement \(change, incident and release management\)
-   Conformance and audit \(policy adherence, audit readiness\)
-   Optimization \(capacity planning and life cycle and cost management\)
-   Security operations \(exposure mapping, policy enforcement, risk response\)

## How tables in CSDM data domains support the service life cycle

![CSDM domains support service life cycles.](../image/csdm-service-life-cycle-flow.png)

1.  When you first start working on an instance, your admins install and populate the CMDB data structures. The data is required to enable your platform features and capabilities. This kind of data is kept in tables that are considered foundational to all products on your instance. We therefore refer to this set of tables as the Foundation domain — it supports all of the other data domains.
2.  You start with an idea — an idea that implements your business model. The idea or concept is saved in data that you work on in the tables of the Ideation &amp; Strategy domain.
3.  If your research determines that the idea has merit, you can decide to commit to it and move forward into designing and planning the idea. You might design the products to implement the idea internally or buy something to integrate into your organization's offerings. The supporting data lives in tables in the Design &amp; Planning domain.
4.  After the design is complete and acceptable, you can hand it off to the teams that will build or integrate the idea. Designers and developers build the software that implements the idea. The supporting data lives in tables in the Build &amp; Integration domain. Information learned in this stage of the product life cycle is fed back into data in the domains that were involved earlier in the digital product's life cycle.
5.  Now it's time to provide infrastructure and management capabilities. The CIs and assets — service instances, applications, functions, AI, hardware, and software in the Service Delivery data domain. Information learned in this stage is also fed back.
6.  You can now release the idea. It's delivered from the infrastructure and management of the Service Delivery data domain to the catalog of service and business offerings in the Service Consumption data domain so that your customers can consume it. Customers can be internal or external. Again, information learned in this stage is fed back.

    The Manage Portfolio domain is a layer on top of the CSDM conceptual model that interacts with the other CSDM domains. The typical user, a service owner, might be responsible for services in more than one domain.


## Roles that create, maintain, and use the data

**Note:** The Application Owner, Portfolio Manager \(multiple\), and Service Owner \(multiple\) might be the same persons.

-   **Enterprise Architect and Application Owner**
    -   Identify, enter, and maintain data in Business Application records
    -   Align enterprise applications to capabilities and business strategy
    -   Manage technology portfolio life cycle
-   **Portfolio Manager and Service Owner**
    -   Own the Service or digital product
    -   Create Services and service offerings
    -   Set the SLAs
    -   Is informed of outages
    -   Request catalog items to be created for the offerings
-   **Service Desk, Incident Manager, and Change Manager**
    -   Use the Cls and related service-related data to support and maintain services and Cls
    -   Support Service Operations
    -   Review and approve changes
    -   Maintain support processes
-   **App Service Admin and Technical SMEs**
    -   Support, manage, and operate the underpinning technology that services rely on
    -   Subject matter technical experts that create change requests with data from CMDB
-   **CMDB Manager and Cl Analysts**
    -   Maintain the accuracy and integrity of the CMDB
    -   Work with various SMEs to certify that the data is accurate and aligned to the data model
    -   Create Cls and own the SACM processes

## CSDM Community

[Join the ServiceNow CSDM Community to grow your CSDM expertise.](https://www.servicenow.com/community/csdm/ct-p/common-service-data-model-csdm)

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

-   **[Products that use and benefit from CSDM guidelines](csdm-used-by-products.md)**  
Following the CSDM guidelines generates significant benefits in impact analysis, risk analysis, and business continuity.
-   **[CSDM data domains](csdm-conceptual-model.md)**  
The CSDM is the data model that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB help to promote that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.

**Parent Topic:**[Common Service Data Model](csdm-landing-page.md)

