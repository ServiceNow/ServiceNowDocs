---
title: Microsoft SQL Server metadata collector
description: Provides read-only access to metadata from a Microsoft SQL Server account.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Microsoft SQL Server metadata collector

Provides read-only access to metadata from a Microsoft SQL Server account.

The collector harvests metadata from Microsoft SQL Server databases, including tables, columns, views, schemas, stored procedures, functions, and Agent jobs, making them searchable and discoverable in the data catalog. Supports both self-hosted Microsoft SQL Server instances and managed instances, such as those hosted on AWS RDS or Azure SQL.

## Metadata cataloged

The collector catalogs the following information.

**Note:** The collector harvests all versions of overloaded functions and stored procedures. Each version has its own title/name in the catalog, but a distinct identifier.

|Object|Information cataloged|
|------|---------------------|
|Agent Job|Name, Description, Version, Enabled, Category, Server Name, Created Date, Last Modified Date, Owner, Starting Job Step, Email Notification Level, Page Notification Level, Network Notification Level, Event Log Notification Level, Delete Notification Level, Email Notification Sent To, Page Notification Sent To, Network Notification Sent To|
|Agent Job Step|Name, Command, Subsystem, Flag, Additional Parameters, Server, Database, Database Username, Proxy ID, Output File, OS Run Priority, Retry Attempts, Retry Interval, Last Run Outcome, Last Run Duration, Last Run Date, Last Run Time, On Success Action, On Success Go To Step, On Failure Action, On Failure Go To Step|
|Columns|Name, JDBC type, Column Type, Is Nullable, Default Value, Key type \(Primary, foreign\), Column size, Column index Extended property: Description|
|Table|Name, Description, Primary key, Schema Extended metadata: Created date, Modified date|
|Table Index|Index Cardinality, Column name, Index Type, Index Name, is non Unique, Ordinal Position, Pages, Sort Sequence|
|Views|Name, Description, SQL definition|
|Materialized View|Name, description|
|Schema|Identifier, Name Extended metadata: Created date, Modified date|
|Database|Type, Name, Identifier, Server, Port, Environment, JDBC URL|
|Functions|Name, Description, Function Type|
|Stored Procedures|Name, Description, Stored Procedure Type Extended metadata: Definition, Created, Last modified|
|Publication|Name, Description, Status, Publication Type, Allow Push, Allow Pull, Allow Anonymous, Allow Subscription Copy, Retention, Enabled for Internet, Snapshot in Default Folder, Alternate Snapshot Folder, Pre Snapshot Script, Post Snapshot Script, Compress Snapshot, FTP Address, FTP Port, FTP Subdirectory, FTP Login, Active Directory Guid, Centralized Conflicts, Decentralized Conflicts, Conflict Retention, Backward Compatibility, Replicate DDL, Publication Sync Method, Immediate Sync, Immediate Sync Ready, Allow Queued Transaction, Allow Sync Transcation, Allow DTS, Options, Autogen Sync Procedure, Allow Initialize From Backup, Has Conflict Policy, Independent Agent, Is Filtered, Snapshot Status, Max Concurrent Merge, Allow Subscriber Initiated Snapshot, Allow Web Synchronization, Allow Sync To Alternate, Web SynchronizationUrl, Allow Partition Realignment, Generation Leveling Threshold, Automatic Reinitialization Policy|
|Article|Name, Description, Destination Object, Destination Owner, Source Object, Source Owner, Filter Clause, Creation Script, Delete Command, Insert Command, Update Command, Status, Type, Precreation command, Executes Trigger On Snapshot|
|Subscription|Description, Type, Sync Type, Status Server, Database, Queued Reinitialization, Login Name, Update Mode, Loopback Detection Send Back, No Sync Type, Subscriber Type, Datasource Type, Priority, Attempted Validate, Last Validated, Last Sync Date, Last Sync Status, Last Makegeneration Datetime, Replica Version, Cleanedup Unsent Changes|
|Synonym|Name|

**Note:** All versions of overloaded functions and stored procedures are cataloged. Each version has its own title in the catalog but a distinct identifier.

When profiling and sampling parameters are enabled, the following additional column information is cataloged:

<table id="table_h3b_52f_b3c"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

Column

</td><td>

-   Average Length \(sample\)
-   Average Value \(sample\)
-   Data Distribution
-   Distinct Values
-   Estimated Distinct Values
-   Estimated Non-null Values
-   Maximum Length \(sample\)
-   Maximum Value \(sample\) sorted numerically or alphabetically \(z-a\)
-   Minimum Length \(sample\)
-   Minimum Value \(sample\) sorted numerically or alphabetically \(a-z\)
-   Non-null Values \(sample\)
-   Sample String Values \(first 5 items in a column\)

</td></tr><tr><td>

Table

</td><td>

-   Row Count
-   Sample Count \(Target sample size\)

</td></tr></tbody>
</table>## Relationship between objects

Catalog pages show relationships between the following data asset types:

|Data asset page|Relationship|
|---------------|------------|
|Agent Job|Agent Job contains Job Step|
|Job Step|Job Step command is executed in Database|
|Table|Columns, Table Indexes, Schema|
|View|Schema that contains Views, Columns that are part of Views|
|Materialized View|Schema that contains Materialized Views, Columns that are part of Materialized Views|
|Columns|Table|
|Schema|Database that contains Schema, Table that is part of Schema, View that is part of Schema, Materialized View that is part of Schema, Synonym|
|Database|Schema contained in Database|
|Publication|Contains Article, Has Parent Publication, Published by Publisher Database|
|Article|Refers Table|
|Subscription|Subscribes to Publication, Delivered To Subscriber Database, Delivery Executed By Distributor Database, Supplies Data to Table|

## Lineage and dependencies for Microsoft SQL Server

The following lineage information is collected by the Microsoft SQL Server collector. This lineage information is available only for the target server and databases specified while running the collector. Harvesting lineage from referenced objects located in another server is not supported.

<table id="table_wdy_hff_b3c"><thead><tr><th>

Object

</th><th>

Lineage available

</th></tr></thead><tbody><tr><td>

View

</td><td>

Column-level lineage showing source columns for: -   Data sourcing
-   Sorting \(ORDER BY\)
-   Filtering \(WHERE/HAVING\)
-   Aggregation \(GROUP BY\)

</td></tr><tr><td>

Stored Procedure

</td><td>

Column-level lineage showing source columns for data sourcing, sorting, filtering, and aggregation. Table-level lineage showing downstream tables updated by the procedure.

</td></tr></tbody>
</table>**Note:** The collector parses SQL to harvest lineage metadata. For Views, if SQL parsing fails, the collector uses the `dm_sql_referencing_entities` system function when available. For Stored Procedures, the collector parses INSERT, UPDATE, and SELECT statements and additionally uses the `dm_sql_referencing_entities`system function when available. Limitations:Multitable inserts are not supported.Multiple SELECT and INSERT statements must be separated by semicolon delimiters.

The collector catalogs dependencies between tables, views, and stored procedures using `sys.sql_expression_dependencies`. Dependencies are created when one entity appears by name in a persisted SQL expression of another entity. See the [Microsoft SQL Server dependencies documentation](https://learn.microsoft.com/en-us/sql/relational-databases/system-catalog-views/sys-sql-expression-dependencies-transact-sql?view=sql-server-ver16) for details.

-   **[Prepare to run the Microsoft SQL Server collector](../task/prepare-to-run-microsoft-sql-server-collector.md#)**  
Configure authentication and permissions before running the collector.
-   **[Create a Microsoft SQL Server metadata collector](../task/create-microsoft-sql-server-metadata-collector.md)**  
Create a collector to import metadata from Microsoft SQL Server.

**Parent Topic:**[Configuring metadata collectors](configure-metadata-collectors-dc.md)

