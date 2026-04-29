---
title: IBM Db2 on Windows database discovery
description: ServiceNow Discovery uses the Db2 on Windows discovery pattern to find IBM Db2 instances on Windows servers.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# IBM Db2 on Windows database discovery

ServiceNow Discovery uses the Db2 on Windows discovery pattern to find IBM Db2 instances on Windows servers.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Discovery uses this pattern to run horizontal discovery. The pattern is triggered automatically by classification using these Db2 identifiers: tcp\_port, name, installed\_dir

## Prerequisites

Ensure that the user has the permissions to run the following commands:

-   `"\"" + $installed_dir + "\bin\db2cmd\" /c /w /i db2 list database directory"`
-   `"\"" + $installed_dir + "\bin\db2cmd\" /c /w /i db2 list database directory | findstr \"Database name\" | findstr /i " + $entry_point.instance`
-   `"\"" + $installed_dir + "\bin\db2level\""`

## Data collected by Discovery during horizontal discovery

The discovered data includes the following tables and fields.

|Table and field|Description|
|---------------|-----------|
|name|Name of the Db2 instance.|
|tcp\_port|TCP port.|
|installed\_dir|The installation directory.|
|version|Db2 version.|
|db\_name|Name of the database.|
|pid|Process ID of the Db2 instance.|

The Dependency Views map shows all discovered IBM Db2 instances in your organization and the relationships between them.

![IBM Db2 Windows Dependency view](../image/IBM-Db2-Windows-dependency.png)

## CI relationships

The IBM Db2 on Windows pattern does not create any CI relationships.

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

