---
title: Incident Management and CSDM tables
description: Incident Management manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Incident Management.
locale: en-US
release: yokohama
product: Incident Management
classification: incident-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Applying CSDM guidelines to Incident Management, Configure, Incident Management, IT Service Management]
---

# Incident Management and CSDM tables

Incident Management manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Incident Management.

## CSDM tables used by Incident Management

The Incident form references the following CSDM tables:

1.  Application Service \[cmdb\_ci\_service\_discovered\] table or any infrastructure CI.
2.  Configuration Item tables \[cmdb\_ci\*\]
3.  Business Service \[cmdb\_ci\_service\_business\] table and Technical service \(Technology Management Service \[cmdb\_ci\_service\_technical\] table\): Use the service classification attribute to identify business services, technical services, and application services as types of services.
4.  Service Offering \[service\_offering\] table: Uses the service classification attribute to identify business services, technical services, and application services as types of service offerings.

    See the Incident Management documentation for information about service commitments on a service offering \(for example, resolution time for incident\).


![CSDM tables used by Incident Management.](../image/incident-elements-4.png "Tables used by Incident Management")

## Products that add value to Incident Management

When you use Incident Management with other ServiceNow products, you increase the value you get from Incident Management. These other ServiceNow products include:

-   **Discovery**

    Discovery provides details about the hardware and software CIs you are using.

-   **Service Portfolio Management \(Service Portfolio Management\)**

    Provides life-cycle information for a service.

-   **Asset Management**

    Provides the related product model. Software Asset Management \(SAM Foundation \) and Hardware Asset Management \(HAM\) provide lifecycle data for Incident Management.

-   **Security Management**

    Provide initial information that helps in containing, eradicating, and recovery of security related incidents.

-   **Risk Management**

    Provides IT risk and financial risk information.


## Products that benefit from Incident Management

-   **IT Service Management \(ITSM\)**

    Services have the context of the business and applications, along with the information and technologies layered beneath them.

-   **Information Technology Operations Management \(ITOM\)**

    Understands the business context for the application services along with the hardware and software being managed.

-   **Governance, Risk, and Compliance \(GRC\)**

    Auditors can leverage the business applications and related Information Objects. This helps auditors understand the design-time data sensitivity for scoping audits, measuring risks, and managing audit activities.

-   **Asset Management**

    Manages the software and hardware life cycles for business applications and business services.

-   **Customer Service Management \(CSM\)**

**Parent Topic:**[Applying CSDM guidelines to Incident Management](../concept/itsm-incident-use-case-product-view.md)

