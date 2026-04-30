---
title: Enterprise Architecture \(formerly Application Portfolio Management\) and CSDM tables - Legacy
description: Enterprise Architecture manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Enterprise Architecture.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Enterprise Architecture and CSDM framework - Legacy, Configure - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Enterprise Architecture \(formerly Application Portfolio Management\) and CSDM tables - Legacy

Enterprise Architecture manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Enterprise Architecture.

## CSDM tables managed by Enterprise Architecture

1.  Business Capability table \[cmdb\_ci\_business\_capability\]
2.  Business Application table \[cmdb\_ci\_business\_app\].

    **Note:**

    Enterprise Architecture uses the **Platform** and **Platform App** fields on the Business Application table to establish the relationship between a business application and the underlying application service. Enterprise Architecture manages the Platform Host / Platform App relationship using a reference on the Enterprise Architecture form, not through a CI relationship.

    The relationship connects the record of the business application that is used in planning and design with where and how it’s realized operationally, represented by application services. The relationship accounts for each use of a business application in the development, test, and production environments \(dev, test, and prod application service instances\). Often there are multiple production deployments. For example, a large retailer uses a business application that runs a cash register in each of its 1,000 stores. There are therefore 1,000 production instances of the application service — one per store — for that one business application. [See the "CSDM in a nutshell" video](https://www.youtube.com/watch?v=EnlhMhP2FsM&list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK&index=34) for additional discussion of the relationship.

3.  Information Object table \[cmdb\_ci\_information\_object\]





## Products that add value to Enterprise Architecture

When you use Enterprise Architecture with any of the following ServiceNow products, you increase the value you get from Enterprise Architecture:

-   Discovery provides details about the hardware and software CIs you are using.
-   Service Mapping provides details about the application instance service in the \[cmdb\_ci\_service\_discovered\] table, relating infrastructure and application \[cmdb\_ci\_appl\] CIs.
-   Asset Management provides the related product model. Software Asset Management \(SAM Foundation\) and Hardware Asset Management \(HAM\) provide life-cycle data for Technology Portfolio Management.
-   Project Portfolio Management views the business application roadmaps. Includes demands, projects, sprints and epics.
-   Agile Development views the backlog stories and epics of each business application in the application roadmap.

## Products that benefit from Enterprise Architecture

The following ServiceNow products gain value from Enterprise Architecture:

-   IT Service Management \(ITSM\): Services have the context of the business and applications, along with the information and technologies layered beneath them.
-   Information Technology Operations Management \(ITOM\): Understands the business context for the application services along with the hardware and software being managed.
-   Governance, Risk, and Compliance \(GRC\): Auditors can leverage the business applications and related information objects. This helps auditors understand the design-time data sensitivity for scoping audits, measuring risks, and managing audit activities.
-   Asset Management: Manages the software and hardware life cycles for business applications and business services.

**Parent Topic:**[Enterprise Architecture \(EA\) \(formerly Application Portfolio Management\) and the CSDM framework - Legacy](../concept/apm-use-case-product-view.md)

**Related topics**  


[Exploring the CSDM model](https://www.servicenow.com/docs/access?context=csdm-content-frame-exploring&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

