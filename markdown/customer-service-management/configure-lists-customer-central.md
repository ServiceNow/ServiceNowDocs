---
title: Configure lists for the Customer Information view
description: Configure lists for the Customer Information view.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Customer Information view using CSM Agent Workspace, Configure Customer Central, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure lists for the Customer Information view

Configure lists for the Customer Information view.

## Before you begin

Role required: admin

## About this task

Lists are displayed in the Customer Information view in Agent Workspace.

![Recent cases section displaying a list of recent cases and their details.](../image/customer-lists.jpg)

## Procedure

1.  Navigate to **All** &gt; **Customer Central** &gt; **Customer Information** &gt; **List Configurations**.

2.  Select **New**.

3.  Fill out the fields, as required.

<table id="table_dzp_v1s_mlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Enter a title for the list configuration.

</td></tr><tr><td>

Context table

</td><td>

Select a context table.

</td></tr><tr><td>

Relationship

</td><td>

Enter the relationship between the context and the list. 1.  To create a new relationship, click the Lookup icon and then New.
2.  Enter a name for the relationship.
3.  In the Applies to table, select either the contact or consumer context table.
4.  In the Queries from table select the table from which this list retrieves data.
5.  In **Query with**, type a script to specify the records to include from the table for the relationship queries. For example:

    ```
current.addQuery("contact", parent.sys_id);

“contact” => is the name of the column in the list table that stores the context ID, for example, contact ID.
“parent.sys_id” => is the unique key in the contact table that holds the contact record.
Note: If building a new relationship, ensure that the exact column name from the list table that stores the context ID is specified here.
    ```

</td></tr><tr><td>

View

</td><td>

Select the name of the view that has the set of columns to display for this list. For information on how to create a view, see [Configure the list layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-administration/t_ConfigureTheListLayout.md).

</td></tr><tr><td>

List limit

</td><td>

Enter the number of records to display in the list. You can access the remaining records using pagination.

</td></tr></tbody>
</table>4.  Select **Submit**.


