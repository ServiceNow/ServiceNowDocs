---
title: Update data mapping in a data fabric table
description: Update the data mapping between a source table and a data fabric table.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage data fabric tables, Zero Copy Connectors, Workflow Data Fabric]
---

# Update data mapping in a data fabric table

Update the data mapping between a source table and a data fabric table.

## Before you begin

Role required: One of the following role combinations or admin.

-   delegated\_developer with sn\_dd\_&lt;application\_scope\_name&gt;\_tablesforms OR sn\_dd\_&lt;application\_scope\_name&gt;\_delegatedadmin, and a role containing the df\_data\_steward role
-   delegated\_developer with sn\_dd\_&lt;application\_scope\_name&gt;\_tablesforms OR sn\_dd\_&lt;application\_scope\_name&gt;\_delegatedadmin, and df\_connection\_admin

## About this task

A data steward might need to update the field mapping for a data fabric table in the following scenarios:

-   The data source administrator notifies the connection admin or data steward about a schema change in the external data source.
-   A field in the data fabric table isn't named correctly.
-   The data steward wants to create a relationship with another data fabric table by adding a reference column.
-   A data steward wants to create a reference to the current data fabric table from another table but needs to designate a primary key in the current table first.

## Procedure

1.  Navigate to the **Data fabric tables** tab in the Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Data fabric tables**
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Data fabric tables**.
2.  Find the data fabric table that you want to update and select **Edit**.

3.  Add or remove mapped columns from the external source.

    -   In the list of source columns, select the check box for each column that you want to add to the data fabric table. Each column that you select is automatically created in the data fabric table with the same name and data type.
    -   In the list of source columns, clear the check box for each column that you want to remove from the data fabric table.
4.  Update a field's display name by changing the column label.

    You can only change the label and not the column name.

5.  Add or remove references to other tables.

    -   To reference a local table on your instance from a data fabric table, an instance administrator must create an ACL rule with the data\_fabric record operation on the local table. For example, to create a reference to the User \[sys\_user\] table, the following ACL rule is required:

        -   Type: record
        -   Operation: data\_fabric
        -   Name: User \[sys\_user\]
        For details on creating a record ACL rule, see [Configure an ACL rule](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&version=australia&pubname=australia-platform-security&ft:locale=en-US).

    -   To see values in a reference column when viewing records in the new data fabric table, you must set the Display attribute to true for the referenced column. You can manage this attribute in the referenced table's definition. See [Select a field as the table display value](https://www.servicenow.com/docs/access?context=t_SelectTheDisplayValue&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
<table id="choicetable_mqw_2tf_w2c"><tbody><tr><td id="d658239e197">

**Add a reference**

</td><td>

1.  In the Type column, change the column type to **Reference**.
2.  Select **Set reference**.
3.  In the Set Reference Label dialog box, enter the name of the table that you want to reference.
4.  In the Set Reference Label dialog box, select a primary key in the Reference key field.
5.  Select **Set reference**.


</td></tr><tr><td id="d658239e233">

**Remove a reference**

</td><td>

In the Type column, change the column type from **Reference** back to the data type that matches the source column.

</td></tr></tbody>
</table>6.  Add or remove a primary key from the data fabric table using the Primary Key toggle switch.

    If the current table will be referenced by another data fabric table, you must select a primary key to use as the reference.

7.  Select **Finish**.


**Parent Topic:**[Managing data fabric tables](../concept/managing-data-fabric-tables-zcc.md)

