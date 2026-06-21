---
title: Hardware life cycle
description: The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The hardware lifecycle states represent the overall life cycle of hardware assets and CIs as related to their products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-hardware.html
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [CSDM reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Hardware life cycle

The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The hardware lifecycle states represent the overall life cycle of hardware assets and CIs as related to their products.

## Life-cycle values for hardware

Hardware assets are physical items that are stocked, for example servers, monitors, and keyboards. A life-cycle value pair is the combination life cycle stage and life cycle stage status values for a CI, asset, or IBI over the life cycle of a product instance. The stages and statuses for the hardware life-cycle process are visible only in hardware-related tables in Asset Management and the CMDB.

The standard CSDM life-cycle value pair covers all phases of a product instance life cycle.

-   A **life cycle stage** is one of the broad phases that a CI moves through, from inception or procurement to retirement and end of life.
-   **life cycle stage status** is the particular status of a CI within its current life cycle stage.

For example, a hardware CI in the **Operational** stage might change status over time from **In Use** to **In Maintenance** to **End of Support**. A different hardware CI might go from **In Use** to **End of Support** without ever having been in **In Maintenance** status.

\[Omitted image "csdm-op-stage-of-hw-ci.png"\] Alt text: Allowed life-cycle values during the Operational stage of a hardware CI's life cycle

**Note:** The \[life\_cycle\_control\] table uses the type of CI \(hardware, document, logical and so on\) to determine which *life cycle stage status* values are available for each *life cycle stage*.

\[Omitted image "csdm-lifecycle-physical.png"\] Alt text: Hardware life-cycle process: pipeline, purchase, inventory, deploy, operational, defective, missing, and end of life.

For additional information on how you can benefit from implementing life-cycle value pairs for CMDB entities, see the ['Map existing status values to CSDM life-cycle value pairs' section in the 'Foundation domain' topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/foundation-domain.md).

## Holistic life cycle: CMDB hardware tables \(from cmdb\_ci\)​

|CMDB hardware tables​|CMDB hardware table name​|
|---------------------|-------------------------|
|Accessory​|cmdb\_ci\_acc​|
|Communication Device​|cmdb\_ci\_comm​|
|Computer Peripheral​|cmdb\_ci\_peripheral​|
|Computer Room AC​|cmdb\_ci\_crac​|
|Display Hardware​|cmdb\_ci\_display\_hardware​|
|Facility Hardware​|cmdb\_ci\_facility\_hardware​|
|Hardware​|cmdb\_ci\_hardware​|
|Imaging Hardware​|cmdb\_ci\_imaging\_hardware​|
|IP Device​|cmdb\_ci\_ip\_device​|
|Monitoring Equipment​|cmdb\_ci\_monitoring\_hardware​|
|Network Adaptor​|cmdb\_ci\_network\_adaptor​|
|Printing Hardware​|cmdb\_ci\_printing\_hardware​|
|Rack​|cmdb\_ci\_rack​|
|Storage Device​|cmdb\_ci\_storage\_device​|

## Example hardware classes

View attributes, identification rule, and other important schema structures for the CMDB Computer \[cmdb\_ci\_computer\] class. See [Hardware \[cmdb\_ci\_hardware\] class](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/class-hardware.md).

## How retiring an application service might affect a hardware CI

An application service is the logical representation of the underlying hardware and software CIs that work together to implement a business application or system. The application service represents an instance of the business application or system.

Hardware and software CIs are managed using the physical life-cycle value pairs. Because an application service is a logical representation, it is managed as using the logical life-cycle value pairs. The physical hardware CIs that are part of the service map under an application service have their own life cycle, but they are related through the application services as a specific set of dependencies or decomposition.

-   **Example 1: A hardware CI is not retired when the application service is retired**

    When an application service is retired, the associated hardware might not be retired. For example, the hardware might remain idle, unrelated to any application service, until it is reallocated for use by a new application service.

-   **Example 2: A hardware CI is shared by multiple application services**

    In the common scenario of a shared database, multiple application services \(each with a unique database schema\) share a single database service. The database service runs on a single physical host.

    When one of the application services is retired, the database service and host cannot be retired. All of the other application services still depend on the database service that is running on the host.


See [Monitor the health of application services on the Application Services dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/app-service-dashboard.md).

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[CSDM reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-content-frame-reference.md)

