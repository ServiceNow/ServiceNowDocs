---
title: Break up a large export
description: If the number of records to be exported exceeds the actual export limit, you may want to break the export into smaller increments that do not place a significant performance load on the platform.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Export directly from a URL, Exports, Creating integrations with applications]
---

# Break up a large export

If the number of records to be exported exceeds the actual export limit, you may want to break the export into smaller increments that do not place a significant performance load on the platform.

## Before you begin

Role required: none

## Procedure

1.  Create a filtered list of records that you want to export by following the steps in [Export directly from a URL](t_ExportDirectlyFromTheURL.md).

2.  Write down the number of records returned.

3.  If the record number is higher than the defined threshold, issue a sysparm query for the first 10,000 records using the following syntax:

    ```
    https://<instance name>.service-now.com/syslog_list.do?XML&sysparm_orderby=sys_id&sysparm_record_count=10000
    ```

    This exports the first 10,000 records in order, sorted by the sys\_id number.

4.  Find the next record in order, such as 10,001.

    You can find the next Sys ID value by creating a database view on the table and adding the sys\_id column to the view. You don't need to specify a where clause. After you create the database view, view the records and their Sys ID values by selecting **Try it**. You can sort by the sys\_id column and enter 10,001 to skip to that row.

5.  Right-click the row and copy the sys\_id of the next record you want to export.

6.  Access the next series of records with a greater than or equal to query run against the sys\_id of record 10,001.

    The following example shows a query that uses a sys\_id of b4aedb520a0a0b1001af10e278657d27. Use the syntax shown in this query to export the next set of records.

    ```
    https://<instance name>.service-now.com/syslog_list.do?XML&sysparm_query=sys_id%3E%3Db4aedb520a0a0b1001af10e278657d27&sysparm_orderby=sys_id&sysparm_record_count=10000
    ```

    **Note:** URL queries use typical percent encoding. In this example, the greater than sign \(&gt;\) is encoded as %3E and the equal sign \(=\) is encoded as %3D.

7.  Continue issuing this query, using the starting sys\_id for the next set of records until you have exported all the necessary records.


