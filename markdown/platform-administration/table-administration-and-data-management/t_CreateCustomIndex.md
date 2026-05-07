---
title: Create a table index
description: Build indexes to access the data held in your tables more easily.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a table index

Build indexes to access the data held in your tables more easily.

## Before you begin

Role required: admin

## About this task

**Note:** Constructing an effective index requires specialized knowledge in database architecture. If you don't have this expertise, consult with a database administrator.

Creating an index on a large table can significantly affect system performance. A large table in this case is generally considered to be any table around 1 TB in size. Therefore, consider creating indexes on larger tables only during off-peak hours. For example, avoid adding an index to a CMDB table while a discovery job is running, as this can lead to increased load and potential delays.

## Procedure

1.  Access the Index creator in one of the following ways.

<table id="choicetable_vmm_bj2_kyb"><thead><tr><th align="left" id="d278252e69">

Option

</th><th align="left" id="d278252e72">

Steps

</th></tr></thead><tbody><tr><td id="d278252e78">

**Tables &amp; Columns module**

</td><td>

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables &amp; Columns**.
2.  In the list, find the table you want and select its label.
3.  Navigate to the Index creator.


</td></tr><tr><td id="d278252e111">

**Database Indexes related list**

</td><td>

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.
2.  In the list, find the table you want and select its label.
3.  Navigate to the **Database Indexes** related list.
4.  Select **New**.


</td></tr></tbody>
</table>2.  Select the fields you want included in the index.

    The order in which you select the fields affects how the index works. If you do not have expertise in database design, you should consult someone who does.

3.  To create a unique index, select the **Unique Index** check box.

4.  Select **Create Index**.

    The **Table Name** field is there for your reference only. Overriding the default has no effect.

5.  Select an index type.

    -   -   **btree**

    The default index type.

    -   -   **Columnstore \(RaptorDB Pro\)**

    Optimize data storage and retrieval by creating a columnstore index. Columnstore indexes store data in a compressed, column-oriented format that can improve query performance, especially when querying large datasets. Available with RaptorDB Professional.


**Parent Topic:**[Managing tables and indexes](../concept/using-table-administration.md)

