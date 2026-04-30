---
title: CMDB schema model
description: The Configuration Management Database \(CMDB\) schema model is a series of connected tables that contain all the assets and business services controlled by a company and its configurations.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB schema model

The Configuration Management Database \(CMDB\) schema model is a series of connected tables that contain all the assets and business services controlled by a company and its configurations.

Related ServiceNow® Store apps and reference information:

-   [CMDB tables descriptions](../reference/cmdb-tables-details.md): Descriptions of key CMDB tables in the base system.
-   [CMDB CI Class Models](cmdb-ci-class-models.md): A ServiceNow Store app that adds class models that extend the base CMDB class hierarchy. This includes class descriptions, identification rules, identifier entries, and dependent relationships if applicable. You can then use the added classes as any other CMDB base class.
-   [Populating the CMDB](c_OptionsToPopulateCMDB.md): Information about the various options for populating the CMDB.
-   [Discovery patterns](https://www.servicenow.com/docs/access?context=c_MappingPatternsCustomization&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US): A ServiceNow Store app that provides a library of Discovery patterns for discovering specific devices and applications in the industry.
-   [Getting started with Service Graph Connectors](cmdb-sgc-intro.md): ServiceNow Store apps that provide pre-defined integrations for importing and integrating common third-party data into CMDB classes. Also includes the [IntegrationHub ETL](integrationhub-etl.md) wizard for creating new ETL transform maps.

CMDB tables contain information about computers and devices on the network, software contracts and licenses, business services, and so on. The IT desk can use the CMDB to better understand their network users' equipment, and the relationships between them. The CMDB can also be referenced by other processes within the system.

Applications such as Asset Management and Contract Management, operate in conjunction with the CMDB. Asset Management and Software Asset Management link to CMDB all assets, hardware, software, assets in stock, as well as records for manufacturers and vendors. The Contract Management application contains information about contracts, including leases, service contracts, purchase orders, warranties, and software licenses. The Configuration Management Database \(CMDB\) application has a focus on operation.

For more background information about the CMDB, see the ServiceNow Community post\) at [CMDB 101- What is a configuration management database and why do you need one?](https://community.servicenow.com/community?id=community_blog&sys_id=e913125fdbd9d7404837f3231f9619de).

## Key CMDB tables

Key tables in the configuration management database \(CMDB\):

-   The Base Configuration Item \[cmdb\] table, which is the core CMDB table for non IT CIs \(descending classes are non IT CIs\).
-   The core Configuration Item \[cmdb\_ci\] table, which stores the basic attributes of all the CIs. The admin, itil, or asset user role is required to access this table \(descending classes are IT CIs\).
-   The CI Relationship \[cmdb\_rel\_ci\] table, which defines all relationships between CIs.

The Configuration Item table is extended to other tables, such as Database \[cmdb\_ci\_database\] and Computer \[cmdb\_ci\_computer\]. The Computer table is extended to the Server \[cmdb\_ci\_server\] table, which is extended to the UNIX Server \[cmdb\_ci\_unix\_server\] table, and so on.

**Note:** The Base Configuration Item \[cmdb\] table uses the table per partition extension model, which has different behaviors for replicating and deriving information than other extended tables. See [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

You can use the schema map to view more details of tables and their relationships:

1.  Navigate to **System Definition** &gt; **Tables &amp; Columns**.
2.  Select a table and click **Schema Map**.

![Table hierarchy map.](../image/SchemaMap.png "Schema Map")

**Note:** CIs not extended from the Configuration Item \[cmdb\_ci\] table, are not displayed in Dependency Views maps and in CI relation formatters.

## CI attributes

Attributes apply to all the CIs in a classification. To change attribute values for a CI, edit the appropriate CI. To add a unique attribute to a class, extend the class table and create a new classification for that CI.

The position of a CI in a classification hierarchy is determined by the attributes it shares with the CIs below it. Each time a CI has a single different attribute from its parent, the classification hierarchy branches.

For example, servers have different attributes from computers, which include workstations and laptops. Linux servers and UNIX servers have different attributes from the parent server classification and from each other, so they occupy separate branches in the hierarchy.

