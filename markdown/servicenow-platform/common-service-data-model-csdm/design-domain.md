---
title: Design domain of the CSDM framework
description: The Design domain supports the design and planning of digital products. CIs in the Design domain aren’t operational, so you can’t select them for Incident Management, Problem Management, or Change Management. Enterprise architects and application owners are the typical users of tables in this domain.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [CSDM data domains, Explore, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Design domain of the CSDM framework

The Design domain supports the design and planning of digital products. CIs in the Design domain aren’t operational, so you can’t select them for Incident Management, Problem Management, or Change Management. Enterprise architects and application owners are the typical users of tables in this domain.

## Tables used in the Design domain

The Design domain includes the tables used by Application Portfolio Management \(APM\). You use APM to rationalize and manage your business applications, but you're not required to use APM to benefit from the data in these tables.

-   Business capability table \[cmdb\_ci\_business\_capability\]
-   Business application table \[cmdb\_ci\_business\_app\]
-   Information object table \[cmdb\_ci\_information\_object\]

![Design domain of the CSDM framework.](../image/design-domain.png)

## Relationships between CIs that support decision making

An accurate service model that includes the following relationships can serve as the foundation for strategically aligned architectural decisions. The relationships enable you to determine the risks involved in using particular business capabilities. In addition, they enable you to assess services based on their relationships to business capabilities and business applications.

-   **Relationship between a business capability and its supporting business applications**

    This relationship supports visualization and reporting.

    -   A business capability is a high-level capability that supports a business model or fulfills a mission for your organization.

        A business capability typically describes a specific task that achieves one or more business outcomes. Business capabilities are often listed as verbs \(for example, manage financials or provide IT support services\). You can use business capabilities to rationalize and prioritize the cost of business applications and business services.

    -   A business application represents the software and infrastructure that provides a business function \(for example, the titles catalog\). Business applications are not strictly required, but they are strongly recommended because they increase productivity and perform other business functions such as accounts payables, accounts receivables, and general ledger. You can use APM to add any business application for which you must track costs, usage, business value, functionality, and risks.
-   **Relationship between a business application and the application services**

    The relationship connects the record of the business application that is used in planning and design with where and how it’s realized operationally, represented by application services. The relationship accounts for each use of a business application in the development, test, and production environments \(dev, test, and prod application service instances\). Often there are multiple production deployments. For example, a large retailer uses a business application that runs a cash register in each of its 1,000 stores. There are therefore 1,000 production instances of the application service — one per store — for that one business application. [See the "CSDM in a nutshell" video](https://www.youtube.com/watch?v=EnlhMhP2FsM&list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK&index=34) for additional discussion of the relationship.


## Business capabilities represented in a hierarchy

You can represent business capabilities in a hierarchy of a parent business capability and one or more lower-level \(child\) capabilities. Child capabilities \(leaf nodes\) are represented by numeric values: 1.0 for the parent and 2.0 through 6.0 for the leaf nodes. If you add, update, or delete a capability at a leaf node, be sure to update the levels of all the capabilities for the leaf nodes in that hierarchy, as applicable. If a business capability hierarchy requires more than six levels, divide the structure into multiple business capabilities.

Use the Business Capability form to create, modify, and extend business capabilities.

![Business capability form.](../image/business-capability-form.png)

To update capabilities, select the **Update Capability Level and HierarchyID** related link. Follow these guidelines when you update capabilities to ensure that the capability map reflects the change:

-   If the parent capability is updated in the hierarchy, the levels of all its leaf node capabilities are recalculated.
-   The total number of leaf node levels in a hierarchy can’t exceed six.
-   When adding a capability, the hierarchy level is automatically assigned based on the parent capability level.
-   You can delete only leaf node-level capabilities or capabilities without leaf node levels.
-   Don’t create circular relationships. For instance, when creating a parent capability, a leaf node capability can’t be its parent.

## Adding a Business application

A business application is a manually managed CI class. You must therefore manually create required relationships to CIs \(for example, with instances of the application services in use\). Creating relationships also enables you to relate business applications to infrastructure CIs such as databases and web servers. If needed, you can integrate or connect two or more business applications to establish their relationship.

A business application can span the following entities:

-   Environments \(for example, Development, Test, or Production\).
-   Geographies \(for example, the Americas, the Asia Pacific Japan\).
-   Regions \(for example, Europe, the Middle East, and Africa \[EMEA\]\).

Use either of the following methods to add a business application:

-   Import the list of applications from a spreadsheet or third-party tool. To import data, define a data source and a transform map and then run or schedule an import.

-   Use the Business Application form.

    ![Business Application form.](../image/business-application-form.png)


## Information object

-   An information object is a CI that displays and describes the information \(or type of data\) that the application receives from the database. Information objects are part of the information portfolio and are referenced by the business application.
-   Information objects are mapped to the information object table \[cmdb\_ci\_information\_object\].
-   You can use the information object table to identify the types of data that a business application uses, including highly sensitive data such as:
    -   Personally Identifiable Information \(PII\)
    -   Payment Card Industry Data Security Standard \(PCI DSS\) data
    -   Health Insurance Portability and Accountability Act \(HIPAA\) data

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[Common Service Data Model — conceptual model](csdm-conceptual-model.md)

