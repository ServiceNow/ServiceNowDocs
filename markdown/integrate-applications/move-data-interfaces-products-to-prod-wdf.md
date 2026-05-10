---
title: Move data interfaces and data products to production
description: Use a local update set to move data interfaces and data products from a subproduction instance to production.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [Data Products, Workflow Data Fabric]
---

# Move data interfaces and data products to production

Use a local update set to move data interfaces and data products from a subproduction instance to production.

## Before you begin

Before you begin, verify the following:

-   A local update set is active in the subproduction instance with the same application scope as your data interfaces and data products.
-   All data interfaces and data products you want to move are published in the subproduction instance.
-   Zero-copy connectors for all source systems are configured in the production instance. For setup instructions, see [Zero copy connectors documentation](../../../build/zero-copy-connectors/concept/zero-copy-connectors.md).
-   Role required: Admin

## About this task

Data interfaces and data products are captured in the active update set as you create and publish them. Exporting and installing the update set in production recreates the assets, including all data interface tables and column mappings. After installation, you must verify the connections again in production because connector names and credentials differ between instances.

For detailed instructions on update sets, see [Working with update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/using-system-update-sets.md).

## Procedure

1.  In the subproduction instance, export the update set that contains your data interfaces and data products.

2.  In the production instance, retrieve and install the exported update set.

3.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Data Workbench** and open each data interface.

4.  For each source table, select **Connect and verify**, select the production connector for your source system, and select **Verify**.

    The table shows a **Verified** status when the connection to the production source is verified.


## Result

The data interfaces and data products are available in the production instance. After the metadata collector runs, the data interfaces appear in the Data Catalog where consumers can discover and request access to them.

