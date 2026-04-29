---
title: Configure reports for the Customer Information view
description: Configure which reports to display on the Customer Information view.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Customer Information view using CSM Agent Workspace, Configure Customer Central, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure reports for the Customer Information view

Configure which reports to display on the Customer Information view.

## Before you begin

Role required: admin

## About this task

Reports are displayed in the Customer Information view in Agent Workspace.

![Case overview displaying a circular graph that represents the overall progress of the case.](../image/customer-reports.jpg)

## Procedure

1.  Navigate to **All** &gt; **Customer Central** &gt; **Customer Information** &gt; **Report Configurations**.

2.  Select **New**.

3.  Fill out the fields, as required.

<table id="table_vzg_jcs_mlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Enter a title for the report.

</td></tr><tr><td>

Context table

</td><td>

Select a Context table. **Note:** For example, enter Contact if you want to display all the information about a customer contact.

</td></tr><tr><td>

Report

</td><td>

Select a report. **Note:** Only pie charts, doughnuts, and single score charts are supported.

</td></tr><tr><td>

Relationship

</td><td>

Enter the relationship between the context and the report. 1.  To create a new relationship, click the Lookup icon and then New.
2.  Enter a name for the relationship.
3.  In the Applies to table, select either the contact or consumer context table.
4.  In the Queries from table select the table from which this list retrieves data.
5.  In **Query with**, enter a script to build the relationship between the context table and the report table. You can also specify any filter conditions if needed. For example:

    ```
current.addQuery("contact", parent.sys_id);

“contact” => is the name of the column in the report table that stores the context ID, for example, contact ID.
“parent.sys_id” => is the unique key in the contact table that holds the contact record.
Note: If building a new relationship, ensure that the exact column name from the report table that stores the context ID is specified here.
    ```

</td></tr></tbody>
</table>4.  Select **Submit**.


