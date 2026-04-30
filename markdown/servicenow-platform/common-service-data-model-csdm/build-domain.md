---
title: Build domain of the CSDM framework
description: The Build domain involves the tables that are used in the build effort \(systems development life cycle — SDLC or Agile Development\) of digital products like DevOps. The tables represent the logical development details of the enterprise applications \(digital products\) to be deployed and used by the business. These are not operational CIs.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [CSDM data domains, Explore, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Build domain of the CSDM framework

The Build domain involves the tables that are used in the build effort \(systems development life cycle — SDLC or Agile Development\) of digital products like DevOps. The tables represent the logical development details of the enterprise applications \(digital products\) to be deployed and used by the business. These are not operational CIs.

SDLC component CI records in the SDLC Component table \[cmdb\_ci\_sdlc\_component\] enable the DevOps product to provide enhanced capabilities for visualizing and managing your application development pipeline. Not all organizations use this data — this is an optional table.

Records in the table are not operational and are not direct targets of the ITSM Incident Management, Problem Management, or Change Management processes. You therefore are not required to configure SDLC component records.

The tables in the build domain reference the logical development details of the enterprise applications to be deployed and used by the business. A common persona in this domain is Teams. The SDLC Component table is available through the CMDB schema version 1.33.

![Build domain includes the SDLC component table.](../image/build-domain.png)

## SDLC component

An SDLC component is a CI that represents a unique development effort of code. It represents parts of a larger business application or digital product broken down into its individually developed components. In other words, the SDLC component is a software element of a larger application or technology.

Types of SDLC components:

-   Application: An application service is a deployed instance of the SDLC application component. Examples include micro services and APIs. The build team typically builds application services on behalf of the Service Owner \(as described in [Manage Portfolio domain of the CSDM framework](manage-business-services-domain.md)\).

    See [Monitor the health of application services on the Application Services dashboard](../../configuration-management/task/app-service-dashboard.md).

-   Infrastructure: Any infrastructure CI that represents a snapshot of its configuration details is a deployed instance of the SDLC infrastructure component. Examples include database and security configurations.

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[Common Service Data Model — conceptual model](csdm-conceptual-model.md)

