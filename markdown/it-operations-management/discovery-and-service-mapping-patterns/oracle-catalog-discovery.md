---
title: Oracle Catalog discovery
description: The Discovery and Service Mapping Patterns application uses the Get Catalog info pattern extension of the Oracle DB on Unix and Oracle DB on Windows patterns to find Oracle Catalog objects. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Oracle Catalog discovery

The Discovery and Service Mapping Patterns application uses the **Get Catalog info** pattern extension of the Oracle DB on Unix and Oracle DB on Windows patterns to find Oracle Catalog objects. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery uses the Oracle DB on Unix and Oracle DB on Windows patterns and the Get Catalog info pattern extension to run horizontal discovery.

You can use this pattern on the ServiceNow AI Platform® using the Madrid release or later.

For information on Oracle database discovery, see [Oracle database discovery](../../discovery/concept/c_OracleDatabaseDiscovery.md).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Provide a user with permissions to run queries on ALL\_TABLES**

    Provide a user with permissions to run queries on ALL\_TABLES.

    To view other users' tables in ALL\_TABLES, a user must have any of the following permissions:

    -   Object-level privileges, for example: SELECT.
    -   Higher-level role, for example: SELECT ANY TABLE.
-   **Configure applicative credentials**

    Configure applicative credentials for the Oracle instance \[cmdb\_ci\_db\_ora\_instance\] CI type. For more information, see Applicative credentials.

-   **Configure Windows credentials for Windows operating system \(OS\)**

    For more information, see Windows credentials.

-   **Configure UNIX credentials for UNIX OS**

    For more information, see SSH credentials.


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Get Catalog info Pattern extension.

|Table and field|Description|
|---------------|-----------|
|Oracle Catalog \[cmdb\_ci\_db\_ora\_catalog​\]|
|database\_instance|The name of the database instance​ \(SID​\).|
|name|The name of the CI in the CMDB; schema and SID​.|
|schema|The name of the catalog object.|

The following is a dependency view of the relationship between an Oracle Catalog and an Oracle instance.

![CIs and connections on a Dependency Views map](../image/oracle-catalog-discovery.png)

## CI relationships

This relationship is created to support Oracle Catalog discovery.

|CI|Relationship|CI|
|---|------------|---|
|​Oracle Catalog \[cmdb\_ci\_db\_ora\_catalog​\]|Contains::Contained by|Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

**Related topics**  


[Oracle pluggable database and container database discovery](oracle-cdb-pdb-discovery.md)

[Oracle Global License Advisory Services \(GLAS\) data collection using patterns](oracle-glas-discovery.md)

