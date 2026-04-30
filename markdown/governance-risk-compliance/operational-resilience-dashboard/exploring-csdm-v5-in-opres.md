---
title: Common Service Data Model for Operational Resilience
description: Starting with Release 20.1.x, the Operational Resilience application supports the latest Common Service Data Model \(CSDM\). CSDM is the data framework that administrators use when configuring ServiceNow products and applications. It ensures that configuration items \(CIs\) and their relationships are properly defined and stored in the relevant Configuration Management Database \(CMDB\) tables.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Operational Resilience, Governance, Risk, and Compliance]
---

# Common Service Data Model for Operational Resilience

Starting with Release 20.1.x, the Operational Resilience application supports the latest Common Service Data Model \(CSDM\). CSDM is the data framework that administrators use when configuring ServiceNow® products and applications. It ensures that configuration items \(CIs\) and their relationships are properly defined and stored in the relevant Configuration Management Database \(CMDB\) tables.

## About Common Service Data Model \(CSDM\)

The Common Service Data Model \(CSDM\) offers a robust framework for defining and managing services and business services related data in Operational Resilience reporting. Implementing this model helps organizations achieve the following objectives.

-   Define and manage services, business services, and interfaces.
-   Identify and manage risks, controls, and incidents.
-   Develop and maintain business continuity plans.
-   Support operational resilience and control environment management.
-   Enable informed decision-making and service optimization.

This data model ensures that services are of high quality and align with the overall business goals.

## Benefits of CSDM

The CSDM offers several key benefits for organizations.

1.  Improved service management: By defining and managing services, business services, and interfaces, organizations can ensure efficient and effective service/business service delivery.
2.  Enhanced Operational Resilience: The CSDM model enhances organizational resilience by identifying and managing risks, controls, and incidents, which enables a quick response and recovery from disruptions.
3.  Informed decision-making: By providing a comprehensive view of business services, risks, and controls, the CSDM model facilitates informed decision-making and service optimization.

These benefits help organizations achieve their strategic objectives, enhance customer satisfaction, and maintain a competitive edge in a dynamic business environment.

## About the Common Service Data Model

The Common Service Data Model is the standard data model for all products that use the Configuration Management Database \(CMDB\).

ServiceNow AI Platform® products, applications, and features are CSDM compliant, meaning they all have identical access to the underlying CSDM data model. This shared access greatly enhances the capabilities of your applications.

Additional information about the CSDM can be found in the [CSDM in a nutshell](https://www.youtube.com/watch?v=EnlhMhP2FsM&list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK&index=34) and [Community Forum](https://community.servicenow.com/community).

For the playlist of all the videos, see [Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK).

## Highlights of CSDM for Operational Resilience

The previously integrated data model did not support service offerings and application services. The latest CSDM model now includes support for both service offerings and application services.

## Staging tables and pillars

The Operational Resilience application uses the Entity Hierarchy table, \[sn\_grc\_m2m\_profile\_profile\], to save hierarchical relationships. For example, if a record has `upstream_profile` as a business service \(BS\) and `downstream_profile` as a service offering \(SO\), it indicates that the business service \(BS\) directly connects to the service offering \(SO\) in the CSDM data model.

The Service Process pillar is the parent table for all staging tables in Operational Resilience. Other staging tables inherit the profile field from it.

References for business services \(BS\), service offerings \(SO\), business processes \(BP\), and application services \(AS\) are added to the \[sn\_oper\_res\_profile\] table.

For more information on the tables that are relevant to the CSDM data model, see [Tables relevant to CSDM](../reference/csdm-v5-ref.md). For information on the pillars, see [Pillars overview tab](../../grc-operational-res-ws/concept/pillars-ov.md).

