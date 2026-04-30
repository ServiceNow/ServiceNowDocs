---
title: Configure records for the Customer Information view
description: Configure the records to display on the Customer Information view. For example, a record could provide information on the contact or consumer.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure the Customer Information view using CSM Agent Workspace, Configure Customer Central, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configure records for the Customer Information view

Configure the records to display on the Customer Information view. For example, a record could provide information on the contact or consumer.

## Before you begin

Role required: admin

## About this task

Records are displayed in the Customer Information view in Agent Workspace.

![Contact section displaying the contact details of the customer.](../image/customer-records.jpg)

## Procedure

1.  Navigate to **All** &gt; **Customer Central** &gt; **Customer Information** &gt; **Record Configurations**.

2.  Select **New**.

3.  Fill out the fields, as required.

<table id="table_vzg_jcs_mlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Enter a title for the record.

</td></tr><tr><td>

Context table

</td><td>

Select a Context table. **Note:** For example, enter Contact if you want to display all the information about a customer contact.

</td></tr><tr><td>

Relationship

</td><td>

Enter the relationship between the context and the record. 1.  To create a new relationship, click the Lookup icon and then New.
2.  Enter a name for the relationship.
3.  In the Applies to table, select the table on which the list appears.

**Note:** Enter either contact or consumer.

4.  In the Queries from table select the table from which this list retrieves data.
5.  In **Query with**, enter a script to build the relationship between the context table and the record table. You can also specify any filter conditions if needed. For example:

    ```
current.addQuery('sys_id', parent.sys_id);

“sys_id” => is the name of the column in the record table that stores the context ID, for example, contact ID.
“parent.sys_id” => is the unique key in the contact table that holds the contact record.
Note: If building a new relationship, ensure that the exact column name from the record table that stores the context ID is specified here.
    ```

</td></tr><tr><td>

Fields

</td><td>

Select the fields to display on the record.

</td></tr></tbody>
</table>4.  Select **Submit**.


