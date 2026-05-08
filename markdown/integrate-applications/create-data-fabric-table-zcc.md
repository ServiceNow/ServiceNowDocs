---
title: Create a data fabric table
description: Retrieve data from an internal or external source by creating a data fabric table.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage data fabric tables, Zero Copy Connectors, Workflow Data Fabric]
---

# Create a data fabric table

Retrieve data from an internal or external source by creating a data fabric table.

## About this task

Unlike a remote table, a data fabric table uses a zero copy connection to its data source, eliminating the need for a script to populate the table. This connection allows you to access the data source directly, map the data you need, and create a data fabric table for data consumers on the ServiceNow AI Platform.

With a data fabric table, you can retrieve data from either an internal or external data source.

-   Connect the data fabric table to your local database to reuse data from a physical table on your instance.
-   Connect the data fabric table to an outside data source, such as a data lake or third-party database, to retrieve data that resides outside of your instance.

## Before you begin

Role required: One of the following role combinations or admin.

-   delegated\_developer with sn\_dd\_&lt;application\_scope\_name&gt;\_tablesforms OR sn\_dd\_&lt;application\_scope\_name&gt;\_delegatedadmin, and a role containing the df\_data\_steward role
-   delegated\_developer with sn\_dd\_&lt;application\_scope\_name&gt;\_tablesforms OR sn\_dd\_&lt;application\_scope\_name&gt;\_delegatedadmin, and df\_connection\_admin

Read access to table records is automatically added to users with either of the delegated developer roles.

Note the following restrictions:

-   Only a user with the admin role can create a data fabric table in the global scope.
-   A data steward with the delegated\_developer and the sn\_dd\_&lt;application\_scope\_name&gt;\_tablesforms roles can create data fabric tables in the permitted application scope. These roles enable a data steward to create data fabric tables in an application scope if they have permissions for that application, but not in the global scope.

## Procedure

1.  Navigate to the **Established connections** tab in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
2.  Select the established connection that you want to use.

3.  On the connection page, select the **Data assets** tab.

4.  In the list of data assets, select the source table that you want to pull data from.

5.  Select **Create data fabric table**.

6.  Enter a label for the data fabric table and select **Continue**.

7.  Map one or more columns from the source table to the data fabric table.

    Each column that you select is automatically created in the data fabric table with the same name and data type.

8.  Allow other tables to reference this table by defining a primary key using the Primary Key toggle switch.

    **Note:** Primary key columns detected in the source table are automatically selected as primary keys in the target table. If a primary key isn't detected in the source table automatically, you can select a column with unique values that you want to use as the primary key.

    -   Selecting a primary key doesn't enforce primary key constraints on the data fabric table or on the remote system. You must verify that records identified by the primary key are unique.
    -   Once you define a primary key, it can't be removed. If you determine that you need to change the primary key later, you must delete and recreate the data fabric table first.
    -   If you decide not to define a primary key when creating a data fabric table, you can do so by editing the table later. Note that without a primary key, you can't create references to this table and searches won't work until a primary key is defined.
    -   For every primary key column identified in the source table, a corresponding primary key is automatically created in the data fabric table. Once the data fabric table is created, you can't modify the primary keys that were derived from the source table.
    -   You can't use a reference column as a primary key.
9.  Link data between tables by creating a reference to another table.

    -   To reference a local table on your instance from a data fabric table, an instance administrator must create an ACL rule with the data\_fabric record operation on the local table. For example, to create a reference to the User \[sys\_user\] table, the following ACL rule is required:

        -   Type: record
        -   Operation: data\_fabric
        -   Name: User \[sys\_user\]
        For details on creating a record ACL rule, see Configure an ACL rule.

    -   To see values in a reference column when viewing records in the new data fabric table, you must set the Display attribute to true for the referenced column. You can manage this attribute in the referenced table's definition. See Select a field as the table display value.
    1.  Identify the column that represents the same records in both tables.

    2.  In the Type column, change the column type to **Reference**.

    3.  Select **Set reference**.

    4.  In the Set Reference Label dialog box, enter the name of the table that you want to reference in the Table field.

        **Note:** Only tables with a single primary key appear in the list.

    5.  In the Set Reference Label dialog box, select the primary key column that you want to use in the Reference key field.

    6.  Finish configuring the reference by selecting **Set reference**.

10. Select **Finish**.


## Result

The data fabric table is created and connected to a data source. Data consumers can access the data fabric table and its data just like any physical table on the instance.

**Parent Topic:**[Managing data fabric tables](../concept/managing-data-fabric-tables-zcc.md)

