---
title: Export a slow-query index suggestion to a non-production instance
description: You can export an index suggestion from a production instance to a non-production instance for creation, evaluation, and testing before implementing the index on your production instance.
locale: en-US
release: australia
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Resolving slow queries, Resolve issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Export a slow-query index suggestion to a non-production instance

You can export an index suggestion from a production instance to a non-production instance for creation, evaluation, and testing before implementing the index on your production instance.

## Before you begin

Role required: admin

## About this task

This task involves exporting an index suggestion as an .xml file from your production instance and importing it to a non-production instance. You can then create the index and evaluate its performance on the non-production instance.

## Procedure

1.  In your production instance, navigate to the index suggestion to be exported:

    1.  Navigate to **System Diagnostics** &gt; **Index Suggestions** &gt; **Index Suggestions &gt; To review**.

    2.  In the Index Suggestions table, select the table associated with the index suggestion you want to open from the **Table Name** column.

2.  In the Index Suggestions form, click **Export**.

    The index suggestion is downloaded as an .xml file with the file name `sys_index_suggestion_<alphanumeric identifier>.xml`. The file name has a unique alphanumeric string to differentiate it from other index suggestions.

3.  In your non-production instance, navigate to **System Diagnostics** &gt; **Index Suggestions** &gt; **Index Suggestions &gt; To review**.

4.  In the Index Suggestions table under Related Links, click **Import Suggestions**.

5.  In the Import XML form, choose the index suggestion file that you exported and click **Upload**.

    After the import, the imported index suggestion appears in the Index Suggestions table on your non-production instance.

6.  To continue the index evaluation process on your non-production instance, you can [schedule the index suggestion for creation](create-index-slowquery.md) and [test index performance](test-index-performance.md).


**Parent Topic:**[Resolving slow queries](../concept/resolving-slow-queries.md)

