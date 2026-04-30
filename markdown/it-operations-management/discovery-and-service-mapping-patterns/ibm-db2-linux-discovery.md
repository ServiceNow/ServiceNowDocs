---
title: IBM Db2 on Linux database discovery
description: ServiceNow Discovery uses the Db2 on Linux discovery pattern to find IBM Db2 instances on Linux servers.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# IBM Db2 on Linux database discovery

ServiceNow Discovery uses the Db2 on Linux discovery pattern to find IBM Db2 instances on Linux servers.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Discovery uses this pattern to run horizontal discovery. The pattern is triggered automatically by classification using these Db2 identifiers: tcp\_port, name, installed\_dir.

## Prerequisites

Configure SSH credentials for the Linux server.

In addition, ensure that the user has the permissions to run the following commands:

-   **Identification for Db2 UDB entry point types**

    `". /" + $process.environmentVariables.HOME.value + "/sqllib/db2profile; " + $process.environmentVariables.HOME.value + "/sqllib/bin/db2level"`

    `"source " + $installed_dir + "db2profile"`

    `"db2 list database directory | grep \"Database name\" | grep -i \"" + $entry_point.instance + "\" | head -1"`

    `"db2level | grep \"DB2 v\""`

-   **Identification for Db2 UDB entry point types - NONE**

    `"cat " + $installed_dir + "/db2dump/db2diag.log | grep \"INSTANCE:\" | grep " + $entry_point.instance + " | head -1"`

    `"db2level | grep \"DB2 v\""`

-   **Identification for Db2 on z/OS**

    `"netstat -a | grep " + $entry_point.port`

    `"ls -d /*/* |grep " + $id`


## Data collected by Discovery during horizontal discovery

The **Identification for Db2 UDB entry point types** and **Identification for Db2 UDB entry point types – NONE** sections collect the following tables and fields:

|Field|Description|
|-----|-----------|
|Name \[name\]|The Db2 instance name.|
|TCP port\(s\) \[tcp\_port\]|TCP port.|
|Install Directory \[installed\_dir\]|Installation directory.|
|Version \[version\]|Db2 version.|

The Identification for Db2 on Z/OS section collects the following tables and fields:

|Table and field|Description|
|---------------|-----------|
|Name \[name\]|The Db2 instance name.|
|TCP port\(s\) \[tcp\_port\]|TCP port.|
|Install Directory \[installed\_dir\]|Installation directory.|

The Dependency Views map shows all discovered IBM Db2 instances in your organization and the relationships between them.

![IBM db2 dependency view](../image/IBM-Db2-dependency.png)

## CI relationships

The IBM Db2 on Linux pattern does not create any CI relationships.

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

