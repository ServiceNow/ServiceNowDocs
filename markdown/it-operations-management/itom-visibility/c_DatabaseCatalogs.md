---
title: Database catalog discovery
description: The database catalog lists all the catalog objects, or databases, discovered for an instance of a database.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Database discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Database catalog discovery

The database catalog lists all the catalog objects, or databases, discovered for an instance of a database.

## Databases vs. catalogs

Most database manufacturers use the term catalog to mean database, while Microsoft SQL uses the term database. Database catalogs can be imported into your instance from a third-party discovery tool, entered into the platform manually, or found by Discovery.

**Important:** Discovery does not support MySQL database catalog discovery in the base system. The Oracle DB on Unix and Oracle DB on Windows patterns discover Oracle catalog objects through the pattern extension Get Catalog info. The MSSql DB On Windows and MSSql 2000 DB patterns discover both database instances and catalogs and store them in the database instance records.

For more information about Oracle catalog discovery, see [Oracle Catalog discovery](../../service-mapping/reference/oracle-catalog-discovery.md).

For more information about Microsoft SQL database instances, see [Microsoft SQL Server and Cluster discovery](../reference/mssql-data-collected-pattern.md#).

If you discovered database catalogs using probes before migrating to patterns, you can view the probe-based database catalogs by navigating to **All** &gt; **Configuration** &gt; **Database Catalogs** and selecting a database.

**Parent Topic:**[Database discovery](database-discovery.md)

