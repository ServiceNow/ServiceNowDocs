---
title: Managing data fabric tables
description: Access data virtually from an external source or a local table on your instance using data fabric tables.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Zero Copy Connectors, Workflow Data Fabric]
---

# Managing data fabric tables

Access data virtually from an external source or a local table on your instance using data fabric tables.

## Overview of managing data fabric tables

A data fabric table is a virtual representation of data stored in another source, accessible within the ServiceNow AI Platform. It enables users to interact with data from another source as if it's stored locally, without duplicating the data.  Data stewards are responsible for creating and managing data fabric tables using the process shown in this infographic.

![The data steward selects an established connection, creates a data fabric table, maps data from an external source, and updates the mapping as needed.](../../../administer/workflow-data-fabric/image/mmasset0020812-creating-data-fabric-tables-and-mapping-data-in-workflow-data-fabric-hub-landing.png "Creating and managing data fabric tables")

## Viewing data fabric tables

View a list of all the data fabric tables that data stewards have created on the **Data fabric tables** tab.

-   Search for a data fabric table by label or name.
-   Filter the list of tables by data source and connection.
-   Filter the list of tables by creator.
-   View a list of data fabric tables from active connections in the **Active** tab.
-   View a list of data fabric tables from connections that are deactivated or not configured in the **Others** tab.

## Defining primary keys

A primary key is used to indicate uniqueness and identify records in a data fabric table. Designating a column as a primary key enables you to create references to that column from other data fabric tables. When mapping data in a new data fabric table, primary keys from the source table are automatically defined in the target data fabric table. If the source table doesn’t have a primary key, you can create one in the target table by choosing a column with unique values.

Note the following details when defining primary keys:

-   Selecting a primary key doesn't enforce primary key constraints on the data fabric table or on the remote system. You must verify that records identified by the primary key are unique.
-   Once you define a primary key, it can't be removed. If you determine that you need to change the primary key later, you must delete and recreate the data fabric table first.
-   If you decide not to define a primary key when creating a data fabric table, you can do so by editing the table later. Note that without a primary key, you can't create references to this table and searches won't work until a primary key is defined.
-   For every primary key column identified in the source table, a corresponding primary key is automatically created in the data fabric table. Once the data fabric table is created, you can't modify the primary keys that were derived from the source table.
-   You can't use a reference column as a primary key.

## Reference tables

When mapping external source columns to a data fabric table, you can add references to other tables. Establishing references between tables creates a relationship between the two tables and provides data integrity. A data fabric table can reference another data fabric table or a local table on your instance. A local table can also reference a data fabric table.

Note the following requirements when creating references between tables:

-   To reference a local table on your instance from a data fabric table, an instance administrator must create an ACL rule with the data\_fabric record operation on the local table. For example, to create a reference to the User \[sys\_user\] table, the following ACL rule is required:

    -   Type: record
    -   Operation: data\_fabric
    -   Name: User \[sys\_user\]
    For details on creating a record ACL rule, see [Configure an ACL rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/t_CreateAnACLRule.md).

-   To see values in a reference column when viewing records in the new data fabric table, you must set the Display attribute to true for the referenced column. You can manage this attribute in the referenced table's definition. See [Select a field as the table display value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_SelectTheDisplayValue.md).
-   Ensure the referenced table has at least one primary key column.
-   Ensure the primary key column in the referenced table contains unique values.
-   Ensure the primary key column matches the data type of the source column.

## Table queries

Records retrieved from a data stored and stored in a data fabric table have a finite duration, or life cycle, within the ServiceNow AI Platform.

After a data fabric table is connected to a data source, each time the data fabric table is viewed or accessed, a new query is made to the data source. The retrieved data lives in memory for as long as the list or form appears. After you close the list or form, that retrieved data is purged from memory. The next time that you use or view the retrieved data in the data fabric table, records are repopulated from the data source.

## Data fabric table limitations

-   When mapping data, ensure that the data source does not use case-sensitive table names. For example, if both MY\_TABLE and my\_table exist in the database, the schema will not load because the system cannot differentiate between the tables.
-   When creating a reference to another table, you can only select one primary key column as the reference key. You can't select a composite key as the reference key.
-   When creating a reference to another table, you can only reference a table that has one primary key defined.

For additional data fabric table limitations, see [KB2017730](https://support.servicenow.com/kb?sys_kb_id=68859e2147a0ae5448cb2920326d43fc&id=kb_article_view).

-   **[Create a data fabric table](../task/create-data-fabric-table-zcc.md)**  
Retrieve data from an internal or external source by creating a data fabric table.
-   **[Update data mapping in a data fabric table](../task/update-data-fabric-table-zcc.md)**  
Update the data mapping between a source table and a data fabric table.
-   **[Delete a data fabric table](../task/delete-data-fabric-table-zcc.md)**  
Remove a data fabric table from your instance by deleting it.
-   **[View data fabric table records](../task/view-data-fabric-table-zcc.md)**  
View the records that are currently in a data fabric table.
-   **[Change the connection in a data fabric table](../task/change-source-data-fabric-table-zcc.md)**  
Connect a data fabric table to a different data source.
-   **[Deploying a data fabric table from one instance to another](copying-data-fabric-table-zcc.md)**  
Copy a data fabric table from one instance to another through an update set.

**Parent Topic:**[Zero Copy Connectors](zero-copy-connectors.md)

