---
title: Review index suggestions for slow queries
description: You can review index suggestions and indexes created by the Index Suggestion Engine \(ISE\). The ISE provides three main views of index suggestions as they move through their life cycle: index suggestions in review, index in progress, and index done.
locale: en-US
release: australia
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Resolving slow queries, Resolve issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Review index suggestions for slow queries

You can review index suggestions and indexes created by the Index Suggestion Engine \(ISE\). The ISE provides three main views of index suggestions as they move through their life cycle: index suggestions in review, index in progress, and index done.

## Before you begin

Role required: admin

## About this task

Access index suggestions from the Application Navigator or the Performance homepage.

## Procedure

1.  Access the index suggestions for your instance by navigating to **System Diagnostics** &gt; **Index Suggestions** &gt; **Index Suggestions &gt; To review**.

2.  In the Index Suggestions table, select the table associated with the index suggestion you want to view from the **Table Name** column.

3.  Review the index suggestion for the selected table.

    For a description of the field values in the index suggestion, see [Index suggestion form fields](../reference/index-suggestion-fields.md).

4.  Choose the next processing step for the index suggestion.

<table id="choicetable_msd_x4k_tz"><tbody><tr><td id="d179414e106">

**Export**

</td><td>

Downloads the index suggestion as an .xml file, which can be [exported to a non-production instance for testing and evaluation](export-index-suggestion.md).

</td></tr><tr><td id="d179414e132">

**Ignore**

</td><td>

Changes the index suggestion state to ignore, which indicates the index suggestion is no longer active and available for index creation. Index suggestions with an Ignore state are listed in the **Index Suggestions &gt; Done** view of the Index Suggestion table.

</td></tr><tr><td id="d179414e144">

**Schedule creation**

</td><td>

Opens the Schedule Index Creation window to [schedule an index suggestion for creation](create-index-slowquery.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Resolving slow queries](../concept/resolving-slow-queries.md)

