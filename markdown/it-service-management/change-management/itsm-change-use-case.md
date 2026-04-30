---
title: Change Management and CSDM tables
description: Change Management manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Change Management.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Applying CSDM guidelines to Change Management, Configure, Change Management, IT Service Management]
---

# Change Management and CSDM tables

Change Management manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Change Management.

## CSDM tables managed by Change Management

Configuration items \(CIs\) tables \[cmdb\_ci\_\*\]:

-   Application table \[cmdb\_ci\_appl\]
-   Server table \[cmdb\_ci\_server\]
-   Virtual machines table \[cmdb\_ci\_vm\_instance\]
-   Load balancer table \[cmdb\_ci\_lb\]
-   Network gear table \[cmdb\_ci\_netgear\]

The following figure highlights the CSDM tables managed by Change Management.

![CSDM elements in Change Management.](../image/change-mgmt-elements-1.png "CSDM tables managed by Change Management")

## CSDM tables used by Change Management

1.  Application Service table \[cmdb\_ci\_service\_discovered\] or any infrastructure CI.
2.  Configuration Item tables \[cmdb\_ci\*\]
3.  Business Service \[cmdb\_ci\_service\_business\] table and Technology Management Service \[cmdb\_ci\_service\_technical\] table \(formerly Technical service\): Uses the service classification attribute to identify business services, technical services, and application services as types of services.
4.  Service Offering \[service\_offering\] table: Uses the service classification attribute to identify business services, Technology Management Offerings \(formerly Technical service offerings\), and application services as types of service offerings.

![CSDM elements used by Change Management.](../image/change-mgmt-elements-2.png "Tables used by Change Management")

## Products that add value to Change Management

When you use Change Management with other ServiceNow products, you increase the value you get from Change Management. These other ServiceNow products include:

-   **Discovery**

    Discovery provides details about the hardware and software CIs you are using.

-   **Service Mapping**

    Service Mapping provides details about the application instance service in the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table, relating infrastructure and application \[cmdb\_ci\_appl\] CIs.


## Products that benefit from Change Management

-   **Service Portfolio Management \(Service Portfolio Management\)**

    Services have the context of the business and applications, along with the information and technologies that underpin them.

-   **IT Service Management \(ITSM\)**

    Incidents caused by, impacted by, or fixed by Change Management.

-   **Asset Management**

    Updates assets.

-   **Information Technology Operations Management**

    Updates CIs using a controlled process.

-   **DevOps**

    Provides Change Management governance for pipeline tool chains.


## For more information

[See the video: How Change Management leverages the CSDM](https://www.youtube.com/watch?v=3iCxTeU4ZTA&list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK&index=43)

**Parent Topic:**[Applying CSDM guidelines to Change Management](../concept/itsm-change-use-case-product-view.md)

