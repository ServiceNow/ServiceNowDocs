---
title: Test index performance for slow queries
description: After the Index Suggestion Engine \(ISE\) generates an index suggestion for a slow query, you can test the index to see if it improves execution time. If you're evaluating an index suggestion on a non-production instance, you can run this test after creating the index to get immediate results on index performance.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2025-05-12"
reading_time_minutes: 2
breadcrumb: [Resolving slow queries, Resolving platform performance issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Test index performance for slow queries

After the Index Suggestion Engine \(ISE\) generates an index suggestion for a slow query, you can test the index to see if it improves execution time. If you're evaluating an index suggestion on a non-production instance, you can run this test after creating the index to get immediate results on index performance.

## Before you begin

Role required: admin

## About this task

This test is an optional assessment of the index. The test isn’t part of the 14-day index evaluation process that automatically occurs after you create an index.

**Note:** Index test results from your non-production instance might not necessarily predict similar performance results on your production instance.

## Procedure

1.  Open the Index Suggestion record for the index that you want to test:

    1.  Navigate to **System Diagnostics** &gt; **Index Suggestion** &gt; **Index Suggestions &gt; In progress**.

    2.  In the Index Suggestions table, select the table associated with the index suggestion you want to view in the **Table Name** column.

2.  In the Index Suggestion record, select **Test Performance** to start the performance test.

3.  When the Test Index Suggestion progress indicator shows that testing is complete, select **Go to Result**.

    ![Progress indicator window that shows the Query Execution Timer](../image/IndexSuggTestPerfProgress.png)

4.  In the Query Performance Test Results form, compare the **Average with index** and **Average without index** fields to see if the index improved the query time.

    In the following example, the index improved the query time. The **Forced** check box is cleared, indicating that the database is using the index. If the check box is selected, the database is forced to use the index during the test, but not outside of the test.

    ![Test results of the Test Performance option, which checks the average query time with and without the index.](../image/QueryPerfTestResults.png)

    |Field|Description|
    |-----|-----------|
    |Index Suggestion|Name of the index suggestion.|
    |Created|Date and time this performance test was run.|
    |Average with Index \(ms\)|Query time using the index suggestion.|
    |Average without Index \(ms\)|Query time before using the index suggestion.|
    |Forced|Check box indicating whether the database is using the index. If this box is selected, the database is forced to use the index suggestion, but only for this test. If the box is cleared, the database is using the index.|

5.  Select the back arrow to navigate back to the Index Suggestion record for the table.

    The result of this index performance test doesn’t change the index state recorded in the Index Suggestion record.


**Parent Topic:**[Resolving slow queries](../concept/resolving-slow-queries.md)

