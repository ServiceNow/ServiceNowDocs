---
title: Data products release notes
description: The ServiceNow Data products application enables data stewards to create governed data interfaces and package them into discoverable, reusable data products that teams can access through the Data Catalog. Data products is a new application in the Australia release.The ServiceNow Data products application enables data stewards to create governed data interfaces and package them into discoverable, reusable data products that teams can access through the Data Catalog. Data products is a new application in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-08-25"
reading_time_minutes: 3
---

# Data products release notes

The ServiceNow® Data products application enables data stewards to create governed data interfaces and package them into discoverable, reusable data products that teams can access through the Data Catalog. Data products is a new application in the Australia release.

## About Data products

-   Create governed data interfaces from single tables, JOIN operations, or UNION operations using the Data Workbench wizard.
-   Package data interfaces into data products to provide consumers with a single, governed entry point for related data assets.
-   Publish data products to the Data Catalog so that consumers can discover, request access, and query data through stable interfaces.
-   Access data from external systems such as Snowflake, Databricks, and Oracle without moving data into ServiceNow using zero-copy connectors.
-   Protect consumers from source system changes through schema stability — published data interfaces maintain their structure even when underlying tables change.

See [Explore data products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/data-products.md) for more information.

## Activation and other requirements

**Important:** Data products is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Data products by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/build-automate-rn-landing.md)

## Australia

The ServiceNow® Data products application enables data stewards to create governed data interfaces and package them into discoverable, reusable data products that teams can access through the Data Catalog. Data products is a new application in the Australia release.

### What's new

-   **[Data interfaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/manage-data-interfaces_wdf.md)**

    Define durable, schema-based contracts that provide a consistent access layer for data consumers in analytics, workflows, and AI applications. Data interfaces support multi-source composition through UNION and JOIN operations and maintain schema stability so that downstream consumers are protected from breaking changes when underlying source systems change. Control access to data interfaces using ServiceNow role-based access control and ACLs.

-   **[Data products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/manage-data-products-wdf.md)**

    Create reusable, business-aligned data entities built on data interfaces with defined ownership, lifecycle management, and metadata. Package and govern data assets as publishable collections that consumers can discover in the Data Catalog and request access to through governed workflows. Control access to data products using ServiceNow role-based access control and ACLs.

-   **[Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/zero-copy-connectors.md)**

    Access data from external systems in place without replication using federated queries with pushdown query execution. Query sources such as Snowflake, Databricks, and native ServiceNow data in real-time or near-real time without moving data into your instance.

-   **[Catalog-First Authoring Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/data-catalog.md)**

    Discover and onboard data assets directly from the Data Catalog and create data interfaces and data products from catalog assets without switching contexts. Build on catalog-registered data sources to improve reuse and reduce duplication of data efforts across your organization.


### What's changed

-   **[Edit a published data interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/edit-data-interface-wdf.md)**

    Modify a published data interface to add columns, swap source tables, change the combination method, update column mappings, or adjust join conditions. Existing consumers continue to use the interface and must reconnect to pick up structural changes.


### Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   Data Products \(sn\_data\_product\): Enables data stewards to create data interfaces and package them into governed data products for sharing and consumption across the organization.
    -   ServiceNow Data Catalog \(sn\_dcg\_app\): Provides a self-service search and discovery interface for browsing data assets. Manages the core data model and business logic for catalog asset governance and enables automated metadata collection and integration connectivity with external data platforms.
    -   Graph Explorer \(sn\_hexplorer\): Provides visualization of data flow and business context relationships across systems with column-level lineage tracking. Enables interactive catalog navigation with upstream and downstream data flows and dependency insights.
    -   Workflow Data Fabric Connect Hub \(sn\_wdf\_connect\_hub\): Provides the central hub for configuring and managing zero-copy connectors that establish live data pathways between ServiceNow and external data sources.

