---
title: Query record form fields
description: A description of the fields in the query record form.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2025-05-12"
reading_time_minutes: 1
breadcrumb: [Platform performance reference, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Query record form fields

A description of the fields in the query record form.

<table id="table_rch_vcz_yz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Example

</td><td>

An SQL statement for an individual query, before being canonicalized to aggregate it with similar queries.

</td></tr><tr><td>

Hash

</td><td>

The hash value for this record.

</td></tr><tr><td>

Example stack trace

</td><td>

A stack trace for an individual query. Lines referencing script code \(includes both custom and base system code\) appear in the following format:

 `table name.sys_id:line number`

 For example, this stack trace indicates a function call from line 119 of a script include.

 `sys_script_include.105f70abc0a8010300d4d79ed1b93eb0:119`

 For more information, see [stack traces](http://marxsoftware.blogspot.com/2010/10/reading-java-stack-traces-few-tips.html).

</td></tr><tr><td>

Example URL

</td><td>

The URL for an individual query, depending on how the query was called.

 -   User transactions: lists the transaction parameters. For example, if a user navigates to the incident list, the URL is `/incident_list.do` `sysparm_query=active=true`
-   Scheduled jobs: lists the name of the scheduled job.
-   Any other method: lists an empty field.

</td></tr><tr><td>

First sighting

</td><td>

The first occurrence of a similar query.

</td></tr><tr><td>

Last sighting

</td><td>

The last occurrence of a similar query.

</td></tr><tr><td>

Total execution time

</td><td>

Total execution time.

</td></tr><tr><td>

Execution Count

</td><td>

The number of similar query occurrences that are aggregated.

</td></tr><tr><td>

Average execution time \(ms\)

</td><td>

The average duration to execute one of these similar queries.

</td></tr></tbody>
</table>**Parent Topic:**[Platform performance reference](../concept/platform-performance-references.md)

