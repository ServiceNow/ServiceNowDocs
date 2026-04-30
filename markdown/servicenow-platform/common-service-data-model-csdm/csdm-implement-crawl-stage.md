---
title: CSDM implementation stages — Crawl
description: In the Crawl stage, you work on base-system CMDB tables that are associated with IT Service Management \(ITSM\).
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Implement, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CSDM implementation stages — Crawl

In the Crawl stage, you work on base-system CMDB tables that are associated with IT Service Management \(ITSM\).

## Benefits of the operations that you perform in the Crawl stage

-   The operations provide the minimum CMDB support requirements for Incident Management and Change Management.
-   Setting up APM is faster because your business application data is in the right place in the CMDB.
-   The operations build the foundation for using DevOps because your SDLC component data is populated and ready to relate to your applications.
-   Service Mapping is ready to use for mapping entry points because your service instance data is populated.
-   The operations build the foundation for using TPM risk details, a capability of APM.

    The operations prepare you to manage and monitor the life cycles and versions of the underlying technologies of the business applications in your enterprise.

    The data enables you to identify outdated or at-risk software using APM, Service Mapping and Software Asset Management \(SAM\) Professional.


## Tables that you work on during the Crawl stage

**Important:** Future products and product enhancements depend on the data that you prepare in each of the tables.

During this stage, you work on the following base-system CMDB tables:

-   Business Application table \[cmdb\_ci\_business\_app\]
-   Mapped Application Service table \[cmdb\_ci\_service\_discovered\].
-   Application table \[cmdb\_ci\_appl\] \(discoverable\)
-   Server/host \(discoverable\)

**Note:** Some of the classes that you implement in this stage are logical CIs. Logical CIs aren’t created through Discovery, so their **Model ID** values might not refer to product model \(application model, service model, or software model\) records. To help you to migrate to a product-centric management paradigm, each instance of a logical CI should be associated with a product model. See [Auto-generate product models for logical CIs](../task/csdm-auto-create-prod-model-for-ci.md).

![Tables that you work on during the Crawl stage.](../image/crawl-stage.png)

Start by focusing on applications and the application-related data in these areas and tables:

-   **Business Application table \[cmdb\_ci\_business\_app\]**

    A business application is a base-system CMDB table that stores your inventory, application portfolio, and their metadata.

    **Note:** Because this table holds conceptual data, not operational CIs, it is not used by ITSM Incident Management, Problem Management, or Change Management processes.

-   **SDLC Component table \[cmdb\_ci\_sdlc\_component\]**

    SDLC component CI records in the SDLC Component table \[cmdb\_ci\_sdlc\_component\] enable the DevOps product to provide enhanced capabilities for visualizing and managing your application development pipeline. Not all organizations use this data — this is an optional table.

    This table represents the software part or element of a larger whole for applications and infrastructure. Related material may serve as representative of developmental details. It can be used if you need to identify the stratification of a business application or digital product.

    **Note:** Because this table holds logical data, not operational CIs, it is not used by ITSM Incident Management, Problem Management, or Change Management processes.

-   **Service Instance \[cmdb\_ci\_service\_auto\] table \(formerly Application Service table — renamed in CSDM v5\)**

    The service instance is typically the system that a caller identifies when they report an issue with an application.

    A mapped service instance is a base-system CMDB table that identifies the related business application in use. The service instance ties all the elements of the CSDM together where applications are present.

    You might have several service instances representing each deployment based on the environment \(development, QA, production\) and location or geography \(North America, Asia Pacific\).

    Because service instances are logical in nature, they should use the Logical life-cycle value pairs. Service instances follow the same life-cycle guidance as any other logical CI.

    See [Monitor the health of application services on the Application Services dashboard](../../configuration-management/task/app-service-dashboard.md).

-   **Application table \[cmdb\_ci\_appl\]**

    An application is a base-system CMDB table that represents the discoverable instance of an application: code related to a process in use on a host. This table isn't an inventory of your applications. Because of the high level of complexity involved, don't try to manually populate the application table. Discovery creates and maintains this table.

    **Important:** The application table \[cmdb\_ci\_appl\] isn't an inventory or portfolio of your applications. Don't make the mistake of storing managed application details in the application table. Those details \(inventory or application portfolio objects\) belong in the business application table \(as documented in [Design domain in the CSDM framework](design-domain.md)\).

    The application might be identified as the root cause of an incident. However, if you're not using Event Management, the application might not be the initial cause.

    If you're using Discovery, applications are automatically related to their host, which provides an impact hierarchy from server-to-host applications.


**Parent Topic:**[Implementing the CSDM framework in stages](csdm-implementation-stages.md)

