---
title: Applying CSDM guidelines to Problem Management
description: Problem Management manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Problem Management.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Problem Management product view, Applying CSDM guidelines to your product, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Applying CSDM guidelines to Problem Management

Problem Management manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Problem Management.

## CSDM tables used by Problem Management

1.  Application Service table \[cmdb\_ci\_discovered\_service\]: Application Service or any infrastructure CI
2.  Configuration Item tables \[cmdb\_ci\*\]
3.  Business Service \[cmdb\_ci\_service\_business\] table and Technical service \[cmdb\_ci\_service\_technical\] table: Use the service classification attribute to identify business services and technical services.
4.  Service Offering table \[service\_offering\]: Utilized as a choice list attribute to filter types of service offerings like Business Service, Technical Service, and Application Service.

![CSDM tables used by Problem Management.](../image/pm-used-tables-csdm4.0.png)

## Products that add value to Problem Management

When you use Problem Management with one of the following ServiceNow products, you increase the value you get from Problem Management.

-   Discovery provides details about the hardware and software CIs you are using.
-   Service Portfolio Management provides life-cycle information for a service.
-   Asset Management provides the related product model. Software Asset Management \(SAM Foundation \) and Hardware Asset Management \(HAM\) provide life-cycle data for Technology Portfolio Management.
-   Security Management provides initial information to containment, eradication, and recovery of security related problems.
-   Risk Management provides IT risk and financial risk information.

## Products that benefit from APM

-   IT Service Management \(ITSM\): Services have the context of the business and applications, along with the information and technologies layered beneath them.
-   Information Technology Operations Management \(ITOM\): Understands the business context for the application services along with the hardware and software being managed.
-   Governance, Risk, and Compliance \(GRC\): Auditors can leverage the business applications and related Information Objects. This helps auditors understand the design-time data sensitivity for scoping audits, measuring risks, and managing audit activities.
-   Asset Management: Manages the software and hardware life cycles for business applications and business services.

**Parent Topic:**[Problem Management product view](../concept/pm-use-case-product-view.md)

