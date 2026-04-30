---
title: Index suggestions for slow queries
description: The Index Suggestion Engine \(ISE\) can generate an index suggestion for a selected slow query. When you request an index suggestion for a slow query, the ISE analyzes the query and recommends an index that can improve the query execution time.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Resolving slow queries, Resolve issues, Platform performance, Maintain and monitor, Administer]
---

# Index suggestions for slow queries

The Index Suggestion Engine \(ISE\) can generate an index suggestion for a selected slow query. When you request an index suggestion for a slow query, the ISE analyzes the query and recommends an index that can improve the query execution time.

In new and upgraded instances, the Index Suggestion Engine plugin \(com.glide.index\_suggestion\) is activated by default.

**Note:** The ISE supports MySQL databases only.

Administrators use the ISE to:

-   Generate an index suggestion for a slow query.
-   Review index suggestions for slow queries in your instance.
-   Export an index suggestion to a non-production instance for evaluation and testing.
-   Schedule an index for creation.
-   Monitor the effectiveness of an index during the index evaluation period.
-   Test index performance \(this test is an immediate performance assessment of the index\).
-   Drop an index that does not optimize query performance, as recommended by the ISE.

If you choose to use the index suggestion and create the index, the ISE continues to review the effectiveness of that index during a 14-day evaluation period. The ISE provides details on the index during the evaluation, including recommendations for managing the index.

## How index suggestions work

You start the index suggestion process by requesting an index suggestion for a selected slow query. The ISE runs a daily job that collects column statistics from tables in the slow query, gathering data such as cardinality \(unique columns in a table\) and null/not null count.

Next, the ISE aggregates and analyzes the information collected, applies a weighted column ranking algorithm to the slow query, and generates an index suggestion for the query.

After an index suggestion is generated, you review the suggestion and determine whether to create the index for the slow query. When you create the index, the ISE provides information on the index as it moves through its life cycle. You can track the index suggestion through three main processing stages:

-   **Index suggestions to review**

    During this initial stage, you can review index suggestions that the ISE generated for your slow queries. You can choose to ignore a suggestion, export the index suggestion to a non-production instance for further testing, or schedule the index for creation. If the ISE successfully generates an index suggestion and you choose to schedule the index for creation, the index suggestion moves to the next processing stage. However, if the database cannot use the suggestion or the suggestion degrades query performance, the ISE recommends that you drop the index suggestion.

-   **Index in progress**

    In this stage, the ISE creates the index and the 14-day evaluation period begins. The ISE does an hourly evaluation to determine whether the index improves or degrades the query execution time. The ISE updates the index state, including recommended actions that you can take. For example, if the index does not improve the performance of the slow query, the ISE advises that you drop the index. You can then schedule the index to be dropped from the database. During this stage, you can also choose to test index performance or accept an index, even if the ISE recommends dropping it.

-   **Index done**

    In the last processing stage, the ISE describes the final state of the index and related processing activity. If the index improved the slow query time, the ISE changes the index state to Created and the database continues to use the index. If the index did not improve the query time and you chose to drop the index, the ISE drops the index from the database and changes the index state to Dropped.


![Flowchart that shows the processing stages in the index suggestion life cycle](../image/IndexSuggFlow.png "Index suggestion life cycle")

## Processing states for index suggestions

The Index Suggestions \[sys\_index\_suggestion\] table provides state information on your indexes as they move through the three main processing stages:

-   **Index Suggestions &gt; To review**
-   **Index Suggestions &gt; In Progress**
-   **Index Suggestions &gt; Done**

The ISE uses the following states to describe the processing activity for an index.

<table id="table_abj_bnf_rz"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr class="sub-head"><td class="sub-head">

Index suggestions to review

</td><td>

 

</td></tr><tr><td>

Suggested

</td><td>

ISE generated an index suggestion for the slow query.

</td></tr><tr><td>

Drop Suggested—Unused

</td><td>

ISE recommends that you drop the index, since the database is not using the index for the slow query.

</td></tr><tr><td>

Drop Suggested—Performance Degradation

</td><td>

ISE recommends that you drop the index because the index did not improve the query time or made the performance worse.

</td></tr><tr class="sub-head"><td class="sub-head">

Index in progress

</td><td>

 

</td></tr><tr><td>

Creation Scheduled

</td><td>

You scheduled the index for creation.

</td></tr><tr><td>

Creation in Progress

</td><td>

ISE is creating the index.

</td></tr><tr><td>

Creation Failed

</td><td>

ISE could not create the index.

</td></tr><tr><td>

Evaluating Effectiveness

</td><td>

ISE created the index and is assessing index performance during the 14-day index evaluation period.

</td></tr><tr><td>

Drop Suggested—Unused

</td><td>

ISE recommends that you drop the index from the table for which the index was created, since the database is not using the index for the slow query.

</td></tr><tr><td>

Drop Suggested—Performance Degradation

</td><td>

ISE recommends that you drop the index because the index did not improve the query time.

</td></tr><tr><td>

Drop Scheduled

</td><td>

You scheduled the index to be dropped from the database.

</td></tr><tr><td>

Drop in Progress

</td><td>

ISE is dropping the index from the database.

</td></tr><tr><td>

Drop Failed

</td><td>

ISE could not drop the index. Contact Customer Service and Support for assistance.

</td></tr><tr class="sub-head"><td class="sub-head">

Index done

</td><td>

 

</td></tr><tr><td>

Created

</td><td>

After the 14-day evaluation period, the ISE determined that the index improved query performance. Indicates that the database continues to use the index.

</td></tr><tr><td>

Ignored

</td><td>

You chose to ignore the index suggestion.

</td></tr><tr><td>

Dropped

</td><td>

ISE successfully dropped the index.

</td></tr><tr><td>

Accepted

</td><td>

You chose to keep the index even though the ISE recommended dropping it.

</td></tr><tr><td>

Superseded

</td><td>

A recent index suggestion replaced the index for the same table and slow query.

</td></tr></tbody>
</table>**Parent Topic:**[Resolving slow queries](resolving-slow-queries.md)

