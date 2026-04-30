---
title: Review Access Observer logs
description: Use information in the Access Observer log records for insights on how your data is accessed.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access observer]
---

# Review Access Observer logs

Use information in the Access Observer log records for insights on how your data is accessed.

Once you've configured one or more access observation records, your instance begins creating Access Observer log records with details about access to the columns you have chosen. You can find these records on your instance at **All** &gt; **Access Observer** &gt; **Access Observer Log**.

## Access observer log results

Use the following table to understand the information presented in the logs.

<table id="table_m1t_znb_qbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Observer Table Name

</td><td>

The table selected in the access observation record that generated this record.

</td></tr><tr><td>

Observer Column Name

</td><td>

The column selected in the access observation record that generated this record.

</td></tr><tr><td>

Operation User

</td><td>

User that accessed the column

</td></tr><tr><td>

Operation Role

</td><td>

Roles for the user that accessed the column

</td></tr><tr><td>

Caller Application

</td><td>

The scoped application from which the data was accessed.

</td></tr><tr><td>

Caller Type

</td><td>

The type of element which has accessed the column, such as record producer, scheduled job, or business rule.

</td></tr><tr><td>

Caller Source Document ID

</td><td>

 

</td></tr><tr><td>

Caller Source

</td><td>

Element which accessed the column. Used along the **Caller Type** field to see what specifically has accessed the column.

 For example if the caller type is `Business Rule`, the caller source is the name of the business rule which accessed the column.

</td></tr><tr><td>

Primary Hash

</td><td>

 

</td></tr><tr><td>

Repeat Count

</td><td>

 

</td></tr><tr><td>

Java Stack

</td><td>

 

</td></tr><tr><td>

JavaScript Stack

</td><td>

 

</td></tr><tr><td>

Session ID

</td><td>

ID of the session in which the column was accessed.

</td></tr></tbody>
</table>**Parent Topic:**[Access observer](../concept/access-observer.md)

