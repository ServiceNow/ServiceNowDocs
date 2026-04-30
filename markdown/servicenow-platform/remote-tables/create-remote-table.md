---
title: Create a remote table
description: Create a remote table using data retrieved from an external source.
locale: en-US
release: yokohama
product: Remote Tables
classification: remote-tables
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a remote table

Create a remote table using data retrieved from an external source.

## Before you begin

Role required: delegated\_developer or admin

## About this task

When you designate a table as a remote table, keep the following points in mind:

-   Before you create a remote table, you must have a good understanding of external data sources. For example, if you want to retrieve CRM data for use in Customer Service Management, you must understand how the data is structured in the external CRM source.
-   A remote table needs an external primary key to relate its temporary data to the data that is stored in the external source. When you designate a table as remote, only a sys\_id field is auto-generated and appears in the Columns section, which it uses as its primary key for use in Glide records. All external table primary key values are converted to string values.
-   Unlike standard internal tables, you can't extend a remote table from another table.

## Procedure

1.  Navigate to **System Definition** &gt; **Remote Tables** &gt; **Tables**.

    **Tip:** You can also create a remote table using the standard form for tables from **System Definition** &gt; **Tables**.

2.  Select **New**.

3.  On the form, fill in the fields.

    **Note:** You create a remote table in the same manner as a normal table, but designate it as a remote table. The following controls differ in how they operate and what you enter into them when you create a remote table:

<table id="table_yxx_ndv_tr"><thead><tr><th>

Control

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Table name, which is automatically populated based on the table label and a prefix as follows:

-   For a remote table in a scoped application, the name is prefixed with a namespace identifier and the string st\_ to indicate that it’s remote and part of an application.
-   For a remote table in the global application, the name is prefixed with the string u\_st\_.
 You can't modify the prefix; however, you can modify the rest of the table name. The name can contain only lowercase, alphanumeric ASCII characters and underscores \(\_\).

</td></tr><tr><td>

Extends Table

</td><td>

Option that is not available if you select the **Remote Table** option to designate that this table is remote. It no longer appears because you can't extend remote tables from other tables.

</td></tr><tr><td>

Remote Table

</td><td>

Option to designate this table as a remote table. A remote table is a table to which you can associate a script definition for retrieval of data from an external data source. Unlike a standard internal table, the data doesn’t come from records in the current instance. To learn more about remote tables, see [Remote tables](../concept/remote-tables.md).

</td></tr></tbody>
</table>4.  In the Columns section, use the **Table Columns** embedded list to add columns to the remote table like you do when you create columns for a standard internal table.

5.  In the Controls section, define additional remote table options like you do when you define additional table options for a normal table.

6.  In the Application Access section, define the scope protection for the remote table like you do when you define additional table options for a normal table.

    For more information, see [Application access settings](https://www.servicenow.com/docs/access?context=c_ApplicationAccessSettings&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

7.  Select **Submit**.


**Parent Topic:**[Remote tables](../concept/remote-tables.md)

**Related topics**  


[Create a table](https://www.servicenow.com/docs/access?context=t_CreateATable&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

