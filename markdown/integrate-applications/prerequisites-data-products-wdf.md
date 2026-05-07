---
title: Prerequisites and setup
description: Before creating data interfaces and data products, confirm that the required plugin is activated, roles are assigned, and external data sources are connected.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-31"
reading_time_minutes: 3
breadcrumb: [Configure, Data Products, Workflow Data Fabric]
---

# Prerequisites and setup

Before creating data interfaces and data products, confirm that the required plugin is activated, roles are assigned, and external data sources are connected.

**Note:**

Build and test data interfaces and data products in a development or subproduction instance first. When you're ready for production, use a ServiceNow update set to move your assets. See [Move data interfaces and data products to production](../task/move-data-interfaces-products-to-prod-wdf.md)

## Required roles

The following roles are required to work with data products:

-   df\_data\_steward: Required to create and manage data interfaces in Data Workbench.
-   data\_product\_admin: Required to create, update, and publish data products.
-   data\_product\_user: Read-only access. Required for consumers who query published data products.

Contact your system administrator to have these roles assigned to your account.

## Zero-copy connectors for external data sources

If your data interfaces will use tables from external systems such as Snowflake, Databricks, or Oracle, a zero-copy connector for each system must be configured in Connect Hub before you begin. If your data interfaces use only ServiceNow tables, no connector is required.

A zero-copy connector establishes a live data pathway between ServiceNow and the external system. When a consumer queries a data interface built on an external table, ServiceNow uses the connector to retrieve data directly from the source. No data is copied into ServiceNow — the source system remains authoritative.

Zero-copy connectors and metadata collectors serve different purposes and are both required for external sources:

-   A zero-copy connector provides the live data pathway used when querying a data interface or verifying a connection during data interface creation.
-   A metadata collector reads schema information from the source system and publishes it to the Data Catalog. It makes source tables discoverable when building data interfaces, and makes published data products visible to consumers. It does not provide access to live data.

The zero-copy connector must be tested and verified as operational before creating data interfaces. Connection failures during data interface creation indicate that the connector is not properly configured or the external system is unavailable.

For setup instructions, see [Zero Copy Connectors](../../../build/zero-copy-connectors/concept/zero-copy-connectors.md).

## Metadata collectors and Data Catalog visibility

Metadata collectors read schema information — table names, column names, and data types — from a source system and publish it to the Data Catalog. They do not move or copy data.

Two points in the workflow depend on a metadata collector having run:

-   **Before creating a data interface:** Source tables must be discoverable in the Data Catalog before you can select them in the data interface wizard. If a table is not appearing in search, the metadata collector for that source has not run or has not been configured. Ask your administrator to run it manually from Connect Hub.
-   **After publishing a data interface or data product:** There is a delay between publishing and the asset appearing in the Data Catalog. The metadata collector must run before consumers can discover the published product. If you cannot wait for the scheduled run, ask your administrator to run the collector manually from Connect Hub.

Metadata collectors typically run on a scheduled basis, but can be triggered manually when immediate catalog updates are required. The collection process may take several minutes to complete depending on the size and complexity of the source system schema.

For setup instructions, see metadata collector documentation in the ServiceNow product documentation.

## Application scope

Data interfaces and data products are created within an application scope. Confirm that the correct scope is active in your instance before you begin. Assets created in one scope are not editable from a different scope.

**Parent Topic:**[Configure data products](configure-data-products.md)

