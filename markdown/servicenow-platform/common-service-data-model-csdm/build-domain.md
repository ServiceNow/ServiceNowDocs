---
title: Build &amp; Integration domain in the CSDM model
description: Development teams use the tables in the Build &amp; Integration domain during the build effort \(systems development life cycle — Agile development\) of digital products. The tables represent the logical development details of the enterprise applications \(digital products\) to be deployed and used by your organization. These are not operational CIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/common-service-data-model-csdm/build-domain.html
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [CSDM data domains, Explore, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Build &amp; Integration domain in the CSDM model

Development teams use the tables in the Build &amp; Integration domain during the build effort \(systems development life cycle — Agile development\) of digital products. The tables represent the logical development details of the enterprise applications \(digital products\) to be deployed and used by your organization. These are not operational CIs.

## Tables and relationships in the Build &amp; Integration domain

An Agile development component is a CI that represents a unique development effort of code. It represents parts of a larger business application or digital product broken down into its individually developed components. In other words, the Agile development component is a software element of a larger application or technology. Agile development component CI records in the Agile development Component \[cmdb\_ci\_sdlc\_component\] table enable the DevOps product to provide enhanced capabilities for visualizing and managing your application development pipeline.

Records in the table are not operational and are not direct targets of the ITSM Incident Management, Problem Management, or Change Management processes. You therefore are not required to configure SDLC component records. The SDLC Component table is available through the CMDB schema version 1.33.

The DevOps Change Data Model is built on a powerful data model that connects your DevOps tool chain to the work and data already in the platform. The model provides the ability to accelerate changes while ensuring effective and transparent risk management.

The Build &amp; Integration domain includes the following tables and relationships:

-   Business application \(Service Consumption domain\) **Contains::Contained By** SDLC component
-   SDLC component has a **Contains::Contained By** relationship with the Service instance table in the Service Delivery domain.

\[Omitted image "domain-build-integration-tables.png"\] Alt text: The Build &amp; Integration domain includes the SDLC component table.

## Tables used during the Build &amp; Integration phase of the service life cycle

The Al System Digital Asset represents the Software/ Application components for Al and Gen Al services. For the purposes of build, integration, and Al governance, the Al System Digital Asset \(ServiceNow asset, third-party asset, or custom asset\) represents the deployable software source, binaries, and components that feed into the Build &amp; Integration pipelines. An asset can be deployed or not currently deployed.

\[Omitted image "service-lifecycle-build-integrate.png"\] Alt text: Build &amp; Integration tables in the service life cycle.

## Types of SDLC component

-   Application: A service instance is a deployed instance of the SDLC application component. Examples include micro services and APIs. The build team typically builds service instances on behalf of the Service Owner \(as described in [Manage Portfolio domain in the CSDM model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/common-service-data-model-csdm/manage-business-services-domain.md)\).

    See [Use Application Services dashboard to monitor health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/app-service-dashboard.md).

-   Infrastructure: Any infrastructure CI that represents a snapshot of its configuration details is a deployed instance of the SDLC infrastructure component. Examples include database and security configurations.

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[CSDM data domains](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/common-service-data-model-csdm/csdm-conceptual-model.md)

