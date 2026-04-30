---
title: Stats Tools
description: To aid in performance evaluation, the Stats Tools records statistics for system activities that affect performance such as the execution of queries, scripts, and transactions.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [System Diagnostics, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Stats Tools

To aid in performance evaluation, the Stats Tools records statistics for system activities that affect performance such as the execution of queries, scripts, and transactions.

**Note:** The Stats Tools plugin is activated by default. It requires the admin role to activate or upgrade, and it requires the com.snc.jrobin.

Stats Tools adds modules under **System Diagnostics** &gt; **Stats**, including **Slow Queries**, **Slow Scripts**, and **Slow Transactions**. Each module accesses a table of activity patterns \[sys\_query\_pattern\], \[sys\_script\_pattern\], \[sys\_transaction\_pattern\]. Each pattern table represents a collection of unique activities. Each collection is an aggregation of executions of that unique activity over all time. Each record provides basic timing analysis with example identifiable details of the activity.

**Note:** To aid in debugging, you can filter most of these logs by application scope, limiting the transactions \(for example, slow scripts or events\) to only those transactions originating in specific scopes.

Activity patterns are immediately recorded to a cache and are later persisted to their pattern table. If you flush server caches, then recorded activities that have not been persisted are cleared. The following are examples of pattern records.

-   Each time a query is executed that meets the recording and persistence threshold it is aggregated and stored as a query pattern record.
-   Each time a particular business rule is executed it aggregates to a script pattern record.
-   Each time a particular background job runs it aggregates into a unique transaction pattern record.
-   Each click of the **New** button on the Incidents list counts as a list type transaction pattern with specific form action.

## Metrics

Metrics include total and average times of interest per unique execution pattern over the total execution count. Metrics are aggregated with each new instance of the unique activity and persisted to the pattern record.

## Metadata

Example data from specific executions are included on each pattern to identify execution details.

## Characterizations of each activity type

<table id="simpletable_yyk_115_jt"><tbody><tr><td>

Transactions

</td><td>

Any transaction type includes server-side and related client-side transactions.

 Metrics include **Total server load time**, which aggregates the total server-side time excluding semaphore and session wait times. It also aggregates relevant server transaction times that are found on the syslog\_transaction table.

 Transaction types:

 -   An HTTP Request transaction is identified by a URL, transaction type, processor, form/list action, URL query \(filters\), and related table name.
-   Any other transaction is identified by its transaction URL/page/name, transaction type, and processor or thread name.

</td></tr><tr><td>

Scripts

</td><td>

Any script activity type includes scripts evaluated by GlideScopedEvaluator.

 Script Types:

 -   A Jelly Script is identified by the sys\_jelly\_file table, jelly file path, line number, and script that was executed.
-   Any other script is identified by the table and sys\_id.

</td></tr><tr><td>

Queries

</td><td>

Any query activity includes prepared statements executed by GlideDBI.

 Query Types:

 All queries are identified by MongoDB query or insert, update, or select statements, as well as other components of the statement like selected columns, where clause, unions, column sets, and limits.

</td></tr></tbody>
</table>