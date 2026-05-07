---
title: Explore data products
description: Data products package data interfaces with metadata and governance to provide reusable, discoverable data for workflows, AI agents, and analytics.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 4
breadcrumb: [Data Products, Workflow Data Fabric]
---

# Explore data products

Data products package data interfaces with metadata and governance to provide reusable, discoverable data for workflows, AI agents, and analytics.

A data product is a governed collection of data interfaces that represents a business concept or use case. Data products combine one or more data interfaces. Teams discover data products and data interfaces in the Data Catalog, request access through governance workflows, and query data through stable interfaces.

## Data product components

Data interfaces define the schema, field names, and data types that consumers use to access data. A data product can include multiple interfaces that provide different views of related business entities. Interfaces act as stable contracts between data providers and consumers.

Metadata makes data products discoverable and understandable. This includes business descriptions, tags, ownership information, usage guidelines, and documentation that help consumers evaluate whether the data product meets their requirements.

Governance controls provide data quality and managed access. Each data product has defined ownership, access controls through role-based permissions, and lifecycle management through draft and published states. ![Sample data product](../image/wdf-data-product-overview.png)

## How data products work

Data products expose business entities exclusively through data interfaces. When you create a data product, you select existing data interfaces and package them with metadata and access controls.

The data interfaces enable to read data from source systems, whether ServiceNow tables or external systems, for example, Snowflake, Databricks, Oracle, and other supported data sources. Consumers query the data interfaces without requiring knowledge about underlying source systems, connection details, or data mapping logic.

When source systems change, the data interface schema remains stable. Dashboards, workflows, and applications built on data products continue working when source tables are upgraded, fields are renamed, or data sources are replaced.

## Data product users

|User|Description|
|----|-----------|
|Data Steward|Creates and maintains data interfaces. Packages data interfaces into data products with metadata and documentation. Configures access controls and publishes data products to the Data Catalog. Manages data product lifecycle.|
|Security Administrator|Reviews and approves access control configurations for data products. Manages parent data product roles and validates appropriate reader role assignments to underlying data interfaces.|
|Data Consumer|Discovers data products in the Data Catalog. Reviews metadata and documentation to understand available data. Requests access with business justification. Queries data through data interfaces using Flow Designer, Dashboard Builder, APIs.|

## Data product workflow

This workflow shows the lifecycle from creation to consumption:

1.  Build: A Data Steward creates data interfaces in Data Workbench, using zero-copy connectors configured in Connect Hub to connect to external source tables. Data Stewards create data interfaces by entering basic details, selecting source tables, defining table structure, verifying source connections, and setting permissions.
2.  Package: Data Stewards select data interfaces and combine them into a data product with metadata, documentation, and usage guidelines.
3.  Secure: Data Stewards work with Security Administrators to configure parent data product roles and validate access controls.
4.  Publish: Data Stewards publish the data product and data interfaces. After the metadata collector runs, the data product and data interfaces appears in the Data Catalog.
5.  Discover: Data Consumers search the Data Catalog to find data products and data interfaces that meet their requirements. They review metadata, documentation, and sample data.
6.  Access: Data Consumers request access to data products. After Security Administrator approval, they receive role assignments granting access to all product data interfaces.
7.  Consume: Data Consumers query data through data interfaces in workflows, dashboards, APIs, or AI applications.

## Data products and external data

Data products can expose data from external systems without moving data into ServiceNow. Supported external sources include Snowflake, Databricks, Oracle, PostgreSQL, MySQL, MongoDB, Redshift, BigQuery, SAP HANA, and Teradata. Data interfaces built on external sources can be packaged into data products, providing governed access through the same contract model used for ServiceNow data.

## Data product lifecycle

Data products support two lifecycle states.

-   Draft state is for authoring and testing. Draft products are not visible to consumers in the Data Catalog. Data Stewards build data interfaces, package them into products, and validate functionality.
-   Published state makes data products visible in the Data Catalog where teams can discover and request access. Published products have completed governance review.

## Access control model

Data products use a parent-child role model. The data product has a parent role that grants access to all included data interfaces. Each data interface has its own reader role controlling access to underlying data.

When consumers request access to a data product, they receive the parent role. This automatically grants access to all data interface reader roles included in the product. Consumers don't request access to individual data interfaces.

Security Administrators validate that parent role configuration includes appropriate data interface roles before approving data product publication.

## What to explore next

To learn more about data products, see:

-   [Data products use cases](data-products-use-cases.md)
-   [Managing data products](manage-data-products-wdf.md)
-   [Data interfaces](data-interfaces.md)

