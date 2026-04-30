---
title: Common Service Data Model
description: The CSDM is the data framework that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform products, apps, and features.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2026-01-05"
reading_time_minutes: 5
breadcrumb: [Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Common Service Data Model

The CSDM is the data framework that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform products, apps, and features.

## About the CSDM

The CSDM is the data model standard for all products that use the Configuration Management Database \(CMDB\).

-   ServiceNow AI Platform products, apps, and features are “CSDM-compliant”. That is, they all share identical access to the underlying CSDM data model. This shared model significantly increases the power of your applications.
-   The CSDM guidelines ensure unified data access for ServiceNow AI Platform products.
-   The CSDM gives you clear direct prescriptive guidelines for service modeling within the CMDB.
-   CSDM terms and definitions ensure consistent and accurate service reporting.
-   The CSDM data model supports multiple configuration strategies and includes guidelines for using base-system tables and relationships.
-   You can use the CMDB query builder to create reports showing CMDB configuration items \(CIs\) and their relationships.

You will find additional information about the CSDM on the [Community Forum](https://community.servicenow.com/community). Also, see [CSDM in a nutshell](https://www.youtube.com/watch?v=EnlhMhP2FsM&list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK&index=34).

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

## Expert guidance to assess and improve your CSDM implementation — the CSDM Assessment

The CSDM Assessment provides Impact Customers with leading practices and prescriptive guidance on the CSDM and how it supports processes on the ServiceNow AI Platform. To help your organization plan for and implement CSDM, the assessment includes interactions with ServiceNow CSDM experts and personalized content. See [Common Service Data Model \(CSDM\) Assessment Accelerators](https://www.servicenow.com/docs/access?context=CSDM-assessment&version=yokohama&pubname=yokohama-impact&ft:locale=en-US).

## CSDM documentation

<table id="table_iwv_lpv_klb" class="nav-card"><tbody><tr><td>

[Explore ![](../../../common/image/icon-explore.png)](csdm-content-frame-exploring.md)See how the CSDM framework ensures that your data resides in the appropriate CMDB tables for maximum value from your ServiceNow AI Platform applications.

</td><td>

[Implement the framework![](../../../common/image/icon-set-up.png)](csdm-content-frame-using.md)Following the CSDM framework ensures that you meet your primary goal of consistent accuracy in reporting and analytics so you can effectively manage your digital environment.

</td></tr><tr><td>

[Manage the framework![](../../../common/image/icon-workspace.png)](csdm-content-frame-using.md)The CSDM is the data framework that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform products, apps, and features.

</td><td>

[Reference![](../../../reuse/icons/brand-icons/bus-learn.svg)](csdm-content-frame-reference.md)Reference topics provide detailed descriptions of tables, properties, forms, and roles that are used in the CSDM framework.

</td></tr></tbody>
</table>## Key principles that guided the design and development of the CSDM framework

The framework is intended to help you avoid errors in implementation and to ensure that your ServiceNow AI Platform products generate accurate, complete, and consistent reports. The following principles guided the development of the CSDM framework.

-   **Use simplified concepts**

    Represent concepts in a simple, distinct manner to eliminate duplicates and confusion over data sources.

-   **Design for reporting and analytics**

    A prime objective of CSDM is to support consistent analysis.

-   **Prescribe the data relationships**

    Tell users in a clear direct way which relationships and references to use to link CSDM tables.

-   **Share the data model across products**

    The CSDM identifies a data model that is shared across products to simplify concepts and collaboration. Collaborating with other product teams achieves the best shared design.

-   **Use clear definitions**

    Use agreed-upon CSDM definitions wherever a table, reference, or attribute is used.

-   **Share base-system tables**

    zBoot must provide shared base-system CSDM tables by default.

-   **Consistent data integrations**

    To ensure data integrity, use prescribed technologies when integrating external data sources

-   **Speed adoption**

    For each new release, provide automation and guidance for CSDM that accelerates upgrading and minimizes issues.

-   **Enable data governance and process**

    The presence of data within the model provides little value without governance and effective process to manage the truth and validity of the data.

-   **Provide practical user documentation**

    \(The content that you’re viewing now\) Each product team that references CSDM objects should provide documented guidance on use and/or value of the objects. Links to product guidance appear in [Applying CSDM guidelines to your product — product views](../reference/use-cases.md).


-   **[Exploring the CSDM framework](csdm-content-frame-exploring.md)**  
See how the CSDM framework ensures that your data resides in the appropriate CMDB tables for maximum value from your ServiceNow AI Platform applications.
-   **[Implementing the CSDM framework in stages](csdm-implementation-stages.md)**  
Following the CSDM framework ensures that you meet your primary goal of consistent accuracy in reporting and analytics so you can effectively manage your digital environment.
-   **[Managing the CSDM framework](csdm-content-frame-using.md)**  
The CSDM is the data framework that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform products, apps, and features.
-   **[Applying CSDM guidelines to your product — product views](../reference/use-cases.md)**  
ServiceNow products are CSDM-aware — they expect that CMDB data is organized according to CSDM guidelines and they benefit from that organization.
-   **[CSDM reference](csdm-content-frame-reference.md)**  
Reference topics provide detailed descriptions of tables, properties, forms, and roles that are used in the CSDM framework.

**Parent Topic:**[Configuration Management](../../../administer/general/concept/manage-cmdb.md)

