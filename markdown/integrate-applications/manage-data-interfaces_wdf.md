---
title: Managing data interfaces
description: Create a data interface to control how source data is filtered, combined, and exposed to consumers as a stable, governed schema.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [Data Products, Workflow Data Fabric]
---

# Managing data interfaces

Create a data interface to control how source data is filtered, combined, and exposed to consumers as a stable, governed schema.

When you create a data interface, you select a combination method that determines how data from source tables is structured. The method you choose depends on where your data lives and what consumers want to query.

If you select one source table, the combination method is automatically set to Single table. If you select two or more tables, you choose between JOIN and UNION in the combination method step. The method cannot be changed after the target table is created.

-   **Single table**

    Exposes a subset of columns from one source table. Use this when all the data consumers need comes from a single table and you want to control which columns are visible.

-   **JOIN**

    Combines related data from multiple tables that share a common key, using INNER JOIN. Use this when consumer data is split across tables and you want to correlate records by a shared identifier. Only records with matching values in all joined tables are included.

-   **UNION**

    Stacks rows from multiple source tables with compatible schemas into a single view. Use this when the same type of data is distributed across systems or regions and consumers need a consolidated view. All rows from all tables are included.


-   **[Create a data interface from a single table](../task/create-data-interface-single-table-wdf.md)**  
Create a governed data interface on a single source table and publish it to the Data Catalog so consumers can access the data through a stable schema.
-   **[Create a data interface using UNION](../task/create-data-interface-union-wdf.md)**  
Create a governed data interface that consolidates rows from two or more source tables with compatible schemas using UNION. Publish it to the Data Catalog so consumers can access an aggregated view through a stable schema.
-   **[Create a data interface using JOIN](../task/create-data-interface-join-wdf.md)**  
Create a governed data interface that combines rows from two or more source tables using an INNER JOIN and publish it to the Data Catalog. Consumers can access a unified view through a stable schema.

**Parent Topic:**[Data Products](data-products.md)

