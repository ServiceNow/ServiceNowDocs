---
title: Data products release notes
description: The ServiceNow Data products application enables data stewards to create governed data interfaces and package them into discoverable, reusable data products that teams can access through the Data Catalog. Data products is a new application in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-16"
reading_time_minutes: 3
---

# Data products release notes

The ServiceNow® Data products application enables data stewards to create governed data interfaces and package them into discoverable, reusable data products that teams can access through the Data Catalog. Data products is a new application in the Australia release.

## Data products highlights for the Australia release

-   Create governed data interfaces from single tables, JOIN operations, or UNION operations using the Data Workbench wizard.
-   Package data interfaces into data products to provide consumers with a single, governed entry point for related data assets.
-   Publish data products to the Data Catalog so that consumers can discover, request access, and query data through stable interfaces.
-   Access data from external systems such as Snowflake, Databricks, and Oracle without moving data into ServiceNow using zero-copy connectors.
-   Protect consumers from source system changes through schema stability — published data interfaces maintain their structure even when underlying tables change.

See [Explore data products](https://www.servicenow.com/docs/access?context=data-products&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) for more information.

**Important:** Data products is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Data products features

-   **[Data interfaces](https://www.servicenow.com/docs/access?context=manage-data-interfaces_wdf&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

    Define durable, schema-based contracts that provide a consistent access layer for data consumers in analytics, workflows, and AI applications. Data interfaces support multi-source composition through UNION and JOIN operations and maintain schema stability so that downstream consumers are protected from breaking changes when underlying source systems change. Control access to data interfaces using ServiceNow role-based access control and ACLs.

-   **[Data products](https://www.servicenow.com/docs/access?context=manage-data-products-wdf&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

    Create reusable, business-aligned data entities built on data interfaces with defined ownership, lifecycle management, and metadata. Package and govern data assets as publishable collections that consumers can discover in the Data Catalog and request access to through governed workflows. Control access to data products using ServiceNow role-based access control and ACLs.

-   **[Zero Copy Connectors](https://www.servicenow.com/docs/access?context=zero-copy-connectors&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

    Access data from external systems in place without replication using federated queries with pushdown query execution. Query sources such as Snowflake, Databricks, and native ServiceNow data in real time or near-real time without moving data into your instance.

-   **[Catalog-First Authoring Experience](https://www.servicenow.com/docs/access?context=data-catalog&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

    Discover and onboard data assets directly from the Data Catalog and create data interfaces and data products from catalog assets without switching contexts. Build on catalog-registered data sources to improve reuse and reduce duplication of data efforts across your organization.


## Activation information

Install Data products by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   Data Products \(sn\_data\_product\): Enables data stewards to create data interfaces and package them into governed data products for sharing and consumption across the organization.
    -   ServiceNow Data Catalog \(UI\) \(sn\_dcg\_ui\): Provides the self-service search and discovery interface for consumers to browse and access data products and data interfaces in the Data Catalog.
    -   ServiceNow Data Catalog \(Core\) \(sn\_dcg\_core\): Provides the core data model and business logic for catalog asset management, classifications, and lineage.
    -   ServiceNow Data Catalog - Metadata Collectors \(UI\) \(sn\_meta\_collectors\): Provides the interface for configuring and running metadata collectors that synchronize schema information from external data platforms to the Data Catalog.
    -   ServiceNow Data Catalog - Metadata Collectors \(Core\) \(sn\_dcg\_cc\): Provides the core connectivity services for integrating external data platforms with the Data Catalog through metadata collection.
    -   Connect Hub \(sn\_wdf\_connect\_hub\): Provides the central hub for configuring and managing zero-copy connectors that establish live data pathways between ServiceNow and external data sources.

## Related ServiceNow applications and features

-   **[Workflow data fabric](https://www.servicenow.com/docs/access?context=create-integrations-applications&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

    The ServiceNow® Workflow Data Fabric application provides the foundational platform for creating and managing data interfaces and products. Data Catalog is installed as part of the Workflow Data Fabric application and surfaces assets created and published through it.

-   **[Data catalog](https://www.servicenow.com/docs/access?context=data-catalog&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

    The ServiceNow® Data Catalog is the self-service discovery layer where consumers find published data products, review metadata and documentation, and request access. After a data product is published and the metadata collector runs, it becomes discoverable in the Data Catalog.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

