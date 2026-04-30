---
title: Configure parallel processing of search groups
description: To improve performance, only activate search groups and tables that are necessary to meet business needs.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set global text search properties, Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure parallel processing of search groups

To improve performance, only activate search groups and tables that are necessary to meet business needs.

## Before you begin

Role required: admin

## About this task

For example, if you don't need Change Task results, deactivate that table in the Tasks search group. If only one group of users needs Change Task results, set up a separate search group that includes Change Tasks. Other users search using a group that doesn't contain Change Tasks.

Global text search can render results in parallel to improve performance. To configure the number of parallel processes:

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Global Text Search**.

2.  Locate the property called **Number of simultaneous processes\(1 to 16\) used when searching though multiple groups in a global search**.

3.  Enter the number of processes to run in parallel.

    Each search group uses one thread to render results. Set this value to yield optimal results for your search group configuration. For example, if you have five search groups and four threads, the first four groups run in parallel and the fifth group starts when one of the first four groups finishes. This setup may work well if one of the groups is much larger than another. Similarly, if you have five search groups, setting this value higher than five yields no benefits.

4.  Select **Save**.


**Parent Topic:**[Set global text search properties](set-global-text-search-properties.md)

**Related topics**  


[Revert to the legacy global search UI](revert-to-legacy-global-search.md#)

