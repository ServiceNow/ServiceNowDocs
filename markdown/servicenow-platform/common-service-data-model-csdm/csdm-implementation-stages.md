---
title: Implementing the CSDM framework in stages
description: Following the CSDM framework ensures that you meet your primary goal of consistent accuracy in reporting and analytics so you can effectively manage your digital environment.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Implementing the CSDM framework in stages

Following the CSDM framework ensures that you meet your primary goal of consistent accuracy in reporting and analytics so you can effectively manage your digital environment.

## The CSDM data framework

The CSDM is the data model that admins should follow when they set up ServiceNow products and applications. The standards for defining configuration items \(CIs\) and relationships between CIs in the CMDB ensure that your data resides in the appropriate CMDB tables. The result is maximum value from ServiceNow AI Platform applications.

## Activating CSDM

-   **[Activate the CSDM plugin](../task/csdm-enable.md)**

    Activate the CSDM plugin so you can begin implementing the CSDM data model.

-   **[Enabling life-cycle sync from legacy-to-asset](../../configuration-management/concept/csdm-life-cycle-standard-values.md#)**

    You can align life-cycle values for each product instance on the asset, CI, and IBI tables. A one-time process moves legacy status values for asset and CI across the platform to standard CSDM life-cycle value pairs \(*life cycle stage* and *life cycle stage status*\). Business rules then run regularly to ensure identical IBI, asset, and CI life-cycle data for each product instance.

-   **[Migrate and sync existing data to the CSDM framework](../task/migrate.md)**

    You complete several tasks to ensure that your existing application data migrates successfully to the required tables in the CMDB.


## Implementing the CSDM framework

It's best to use a staged approach when you implement the CSDM framework. Each implementation stage involves particular information types and provides specific benefits. Because each stage builds on the preceding stage, we use an analogy to the way a person develops: foundation, crawl, walk, run, and, eventually, fly.

![CSDM stages: foundation, crawl, walk, run, and fly.](../image/csdm-phases.png)

**Note:** Business applications reference information objects in the information portfolio. You might need to implement the Information Object \[cmdb\_ci\_information\_object\] table earlier than the Fly stage. Your business requirements determine the right stage for implementing the table.

-   **[CSDM implementation stage — Foundation](csdm-implement-foundation-stage.md)**

    In the Foundation stage of implementing the CSDM framework, you prepare the referential data that enables accurate reporting to support good business decisions. Use the base-system tables when you begin implementing the CSDM to derive the highest value from your ServiceNow products and the ServiceNow AI Platform.

-   **[CSDM implementation stage — Crawl](csdm-implement-crawl-stage.md)**

    In the Crawl stage, you work on base-system CMDB tables that are associated with IT Service Management \(ITSM\).

-   **[CSDM implementation stage — Walk](csdm-implement-walk-stage.md)**

    In the Walk stage, you identify and populate the network infrastructure CIs and applications that your organization's technical teams support.

-   **[CSDM implementation stage — Run](csdm-implement-run-stage.md)**

    In the Run stage, you set up the relationship between a technology and the business that sells and/or consumes the technology.

-   **[CSDM implementation stage — Fly](csdm-implement-fly-stage.md)**

    When you reach the Fly stage, you've accomplished all or most of the process of implementing the CSDM framework. The fly stage completes the process.


## Key guidelines for you to follow

-   When linking CSDM tables, use only the relationships that are designed in the model.
-   Collaborate on the shared data model with other product teams. Also, when you extend CSDM and related functionality, be sure to follow the provided guidance. Following the guidance and collaborating with other product teams helps you achieve the best design.
-   Use agreed-upon CSDM definitions whenever you use a table, reference, or attribute.
-   Use the provided CSDM base tables.
-   Use the recommended technologies when you integrate external data sources. The specified process ensures data integrity and integration consistency.
-   Follow the provided guidance for setting up and using ServiceNow AI Platform products.

## Improve your CSDM implementation

The CSDM Assessment provides Impact Customers with leading practices and prescriptive guidance on the CSDM and how it supports processes on the ServiceNow AI Platform. To help your organization plan for and implement CSDM, the assessment includes interactions with ServiceNow CSDM experts and personalized content. See [Common Service Data Model \(CSDM\) Assessment Accelerators](https://www.servicenow.com/docs/access?context=CSDM-assessment&version=zurich&pubname=zurich-impact&ft:locale=en-US).

-   **[Enabling life-cycle sync from legacy-to-asset](../../configuration-management/concept/csdm-life-cycle-standard-values.md#)**  
You can align life-cycle values for each product instance on the asset, CI, and IBI tables. A one-time process moves legacy status values for asset and CI across the platform to standard CSDM life-cycle value pairs \(*life cycle stage* and *life cycle stage status*\). Business rules then run regularly to ensure identical IBI, asset, and CI life-cycle data for each product instance.
-   **[Matching the usage of dynamic CI groups to service type](csdm-dynamic-ci-groups-by-service.md)**  
The type of service determines how you use dynamic CI groups.
-   **[CSDM implementation stage — Foundation](csdm-implement-foundation-stage.md)**  
In the Foundation stage of implementing the CSDM framework, you prepare the referential data that enables accurate reporting to support good business decisions. Use the base-system tables when you begin implementing the CSDM to derive the highest value from your ServiceNow products and the ServiceNow AI Platform.
-   **[CSDM implementation stage — Crawl](csdm-implement-crawl-stage.md)**  
In the Crawl stage, you work on base-system CMDB tables that are associated with IT Service Management \(ITSM\).
-   **[CSDM implementation stage — Walk](csdm-implement-walk-stage.md)**  
In the Walk stage, you identify and populate the network infrastructure CIs and applications that your organization's technical teams support.
-   **[CSDM implementation stage — Run](csdm-implement-run-stage.md)**  
In the Run stage, you set up the relationship between a technology and the business that sells and/or consumes the technology.
-   **[CSDM implementation stage — Fly](csdm-implement-fly-stage.md)**  
When you reach the Fly stage, you've accomplished all or most of the process of implementing the CSDM framework. The fly stage completes the process.

**Parent Topic:**[Common Service Data Model](csdm-landing-page.md)

