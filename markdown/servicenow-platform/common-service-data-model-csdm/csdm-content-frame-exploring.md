---
title: Exploring the CSDM model
description: The CSDM is the data model that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-08-29"
reading_time_minutes: 5
breadcrumb: [CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring the CSDM model

The CSDM is the data model that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.

## Definitions of CSDM terms

See [CSDM terms](../reference/csdm-term-definitions.md).

## Goal of CSDM

Following the CSDM data model helps you to accurately and completely capture the data objects that help you to run your business.

CSDM provides guidance on where to put data in the platform. Because there are multiple ways of identifying and using data, the CSDM guidelines help you to determine the best data structures for supporting your organization's services.

## How tables in CSDM data domains support the service life cycle

![CSDM domains support service life cycles.](../image/csdm-service-life-cycle-flow.png)

1.  When you first start working on an instance, your admins install and populate the CMDB data structures. The data is required to enable your platform features and capabilities. This kind of data is kept in tables that are considered foundational to all products on your instance. We therefore refer to this set of tables as forming the Foundation domain — it supports all of the other data domains.
2.  You start with an idea — an idea that implements your business model. The idea or concept is saved in data that you work on in the tables of the **Ideation &amp; Strategy** domain.
3.  If your research determines that the idea has merit, you can decide to commit to it and move forward into designing and planning the idea. You might design the products to implement the idea internally or buy something to integrate into your organization's offerings. The supporting data lives in tables in the **Design &amp; Planning** domain.
4.  After the design is complete and acceptable, you can hand it off to the teams that will build or integrate the idea. Designers and developers build the software that implements the idea. The supporting data lives in tables in the **Build &amp; Integration** domain. Information learned in this stage of the product life cycle is fed back into data in the domains that were involved earlier in the digital product's life cycle.
5.  You can now release the idea. It's delivered from the infrastructure and management of the **Service Delivery** domain to the catalog of business offerings in the **Service Consumption** domain so that your customers can consume it. Customers can be internal or external. Again, information learned in these stages is fed back.

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
    -   Create new Cls and own the SACM processes

## Benefits of the CSDM guidelines

<table id="table_iqz_fp4_swb"><thead><tr><th>

Benefit

</th><th>

Value and associated features

</th></tr></thead><tbody><tr><td>

Rationalization — Determine how well an enterprise application is performing

</td><td>

Identify insights from operational activities related to services \(visualize aggregated information across all your services and supporting operations\). Application Portfolio Management \(APM\) and IT Business Management \(ITBM\)

</td></tr><tr><td>

Outage reduction — Identify affected business services quickly

</td><td>

Prioritize critical events based on service-related information. IT Service Management \(ITSM\) and Event Management

</td></tr><tr><td>

Reporting — Consistent and reliable information about your services and digital products

</td><td>

Understand services, their makeups, and their accountabilities. IT Service Management \(ITSM\)

</td></tr><tr><td>

Alignment — Align business processes to reduce risk and assure compliance

</td><td>

Understand Service Health \(availability, CSAT, Performance, Vulnerabilities, IPC stats\)Governance, Risk, and Compliance \(GRC\)

</td></tr></tbody>
</table>## Importance of CSDM to the ServiceNow AI Platform

<table id="table_q1l_2vs_rfc"><thead><tr><th>

Product family

</th><th>

Benefits of a mature CMDB that follows the CSDM guidelines

</th><th>

Key metrics

</th></tr></thead><tbody><tr><td>

ITSM

</td><td>

-   Change management
-   True service-level reporting
-   Remove semantic disparity

</td><td>

-   Reduced tickets
-   Reduced MTTR

</td></tr><tr><td>

ITOM

</td><td>

-   Visibility across environments
-   System health and availability
-   Map issues to business processes for prioritization

</td><td>

-   Avoided service outages
-   Reduced MTTR

</td></tr><tr><td>

ITAM

</td><td>

-   Accurate license positions
-   Visibility across operational and financial data

</td><td>

-   Reduced software license fines
-   Reduced failed audits

</td></tr><tr><td>

Strategic Portfolio Management \(SPM\)

</td><td>

-   Map resources to business processes
-   Services based on business context
-   Planning scope and impact of investment / divestment

</td><td>

Reduced business risk and outages from outdated technologies

</td></tr><tr><td>

SecOps

</td><td>

-   Prioritization of vulnerabilities based on business criticality
-   Faster incident isolation and response
-   End-to-end risk visibility

</td><td>

Reduced time to remediate priority 1 vulnerabilities

</td></tr><tr><td>

DevOps

</td><td>

-   Automated DevOps change management
-   Link between configuration changes and impacted Cls

</td><td>

Automated change

</td></tr><tr><td>

CSM

</td><td>

-   Visibility across customer environment
-   Accurate response to incidents

</td><td>

Customer satisfaction

</td></tr><tr><td>

IRM \(GRC\)

</td><td>

-   Ensures quality data used for audit
-   Healthy, trusted data is critical for audit scoping and activities

</td><td>

-   Accurately identify audited entities
-   Reduced audit effort and time

</td></tr></tbody>
</table>## CSDM Community

[Join the ServiceNow CSDM Community to grow your CSDM expertise.](https://www.servicenow.com/community/csdm/ct-p/common-service-data-model-csdm)

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

-   **[CSDM data domains](csdm-conceptual-model.md)**  
The CSDM is the data model that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.

**Parent Topic:**[Common Service Data Model](csdm-landing-page.md)

