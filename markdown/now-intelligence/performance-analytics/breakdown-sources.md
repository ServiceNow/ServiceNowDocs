---
title: Breakdown sources
description: Breakdown sources specify which unique values, called breakdown elements, a breakdown contains.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Breakdown sources

Breakdown sources specify which unique values, called breakdown elements, a breakdown contains.

A breakdown source is defined as a set of records from a table or database view or as a bucket group. External data is supported via Workflow Data Fabric tables. Multiple breakdowns can use the same breakdown source. For example, instead of seeing ALL assignment groups for the Number of Open Changes indicator, you can limit the element list to just those groups that are part of the change process by configuring the Breakdown Source.

-   **[Define a breakdown source](../task/t_DefiningABreakdownSource.md)**  
Specify a facts table to serve as a data source for breakdowns. External data is supported via Workflow Data Fabric tables. Apply conditions to specify the elements for this breakdown source.
-   **[Bucket groups for breakdown sources](c_BucketGroups.md#)**  
Bucket groups are used to recategorize data so it can be used as a breakdown, for example by grouping a range of values into discrete buckets.

**Parent Topic:**[Indicator breakdowns](c_CreatingBreakdowns.md)

