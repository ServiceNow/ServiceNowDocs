---
title: Resolving slow queries
description: Identifying and resolving slow queries is an important aspect of improving platform performance. The ServiceNow AI Platform generates index suggestions to help resolve slow queries.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-05-06"
reading_time_minutes: 5
breadcrumb: [Resolving platform performance issues, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Resolving slow queries

Identifying and resolving slow queries is an important aspect of improving platform performance. The ServiceNow AI Platform generates index suggestions to help resolve slow queries.

Database queries that take an unusually long time to execute might be caused by inefficient query design, high data volume, and lack of proper indexing. The best way to resolve slow queries depends on the combination of factors that contribute to the issue.

<table id="table_c4c_lhw_gfc"><thead><tr><th>

Cause

</th><th>

Possible solution

</th></tr></thead><tbody><tr><td>

Inefficient query design

</td><td>

Review and modify query structures to enhance performance. Query modifications might include verifying that you're fetching only the necessary data, or implementing pagination at the query level.

 You can use a slow query log to determine which queries might need to be enhanced. For more information about how to use a slow query log, see [Use a slow query log](../task/t_UseASlowQueryLog.md).

</td></tr><tr><td>

High data volume

</td><td>

Verify that necessary transaction quotas, application quotas, and operational toggles are set to optimize bandwidth use. For more information, see [Configuring the ServiceNow AI Platform to optimize performance](configuring-platform-performance.md).

</td></tr><tr><td>

Lack of proper indexing

</td><td>

Use the Index Suggestion Engine \(ISE\) to generate index suggestions for selected slow queries.

</td></tr></tbody>
</table>## Overview of using the Index Suggestion Engine

The Index Suggestion Engine \(ISE\) can help generate index suggestions for slow queries. If you modify query design and manage data volume but still notice slow queries, you can use the ISE to generate indexes for slow queries.

Use the following steps to resolve slow queries with the ISE:

1.  [Use the slow query log](../task/t_UseASlowQueryLog.md) to identify slow queries that might benefit from improved indexing.
2.  [Generate an index suggestion for a slow query](../task/generate-index-suggestion.md) using the ISE.
3.  [Review the index suggestion](../task/review-index-suggestions.md) and decide whether to move forward.
4.  [Export a query suggestion from a production instance to a non-production instance](../task/export-index-suggestion.md) for evaluation before adding the index in your production instance.
5.  [Create an index from the suggestion](../task/create-index-slowquery.md) or schedule index creation once you're satisfied with the effects of the index suggestion.
6.  [Test index performance](../task/test-index-performance.md) to evaluate query speed improvement.
7.  If an index isn't needed anymore, [drop the index or schedule it to be dropped](../task/drop-index-slowquery.md). If an index isn't being used or isn't performing well, the ISE might display a suggestion to drop an index.

## Additional info

For more information about how the ISE generates index suggestions, see [Index suggestions for slow queries](index-suggestions.md).

-   **[Index suggestions for slow queries](index-suggestions.md)**  
The Index Suggestion Engine \(ISE\) can generate an index suggestion for a selected slow query. When you request an index suggestion for a slow query, the ISE analyzes the query and recommends an index that can improve the query execution time.
-   **[Use a slow query log](../task/t_UseASlowQueryLog.md)**  
Administrators can use slow query logs to gain insight into how queries are affecting platform performance. The Slow Queries log aggregates data for similar queries. Use slow query data to evaluate the need for new indexes, changes to existing indexes, or changes to frequent queries.
-   **[Generate an index suggestion for a slow query](../task/generate-index-suggestion.md)**  
Use the Index Suggestion Engine \(ISE\) to generate an index suggestion for a slow query. The ISE analyzes slow queries and provides index recommendations to improve execution time when possible.
-   **[Review index suggestions for slow queries](../task/review-index-suggestions.md)**  
You can review index suggestions and indexes created by the Index Suggestion Engine \(ISE\). The ISE provides three main views of index suggestions as they move through their life cycle: index suggestions in review, index in progress, and index done.
-   **[Export a slow-query index suggestion to a non-production instance](../task/export-index-suggestion.md)**  
You can export an index suggestion from a production instance to a non-production instance for creation, evaluation, and testing before implementing the index on your production instance.
-   **[Schedule a slow-query index suggestion for creation](../task/create-index-slowquery.md)**  
Use the Index Suggestion Engine \(ISE\) to schedule an index suggestion for creation.
-   **[Test index performance for slow queries](../task/test-index-performance.md)**  
After the Index Suggestion Engine \(ISE\) generates an index suggestion for a slow query, you can test the index to see if it improves execution time. If you're evaluating an index suggestion on a non-production instance, you can run this test after creating the index to get immediate results on index performance.
-   **[Drop a slow query index](../task/drop-index-slowquery.md)**  
You can drop an index for a slow query when the index isn’t used by the database or doesn’t improve query performance. You can drop the index immediately or schedule the drop for a later time.

**Parent Topic:**[Resolving platform performance issues](resolving-plat-performance-issues.md)

