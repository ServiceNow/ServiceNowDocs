---
title: Optimizing data collection
description: The optimized Performance Analytics data collector reduces the time, memory, and CPU usage for processing large data sets.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data collection process and logging, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Optimizing data collection

The optimized Performance Analytics data collector reduces the time, memory, and CPU usage for processing large data sets.

The optimized data collector is active by default on all instances starting in Tokyo. It is activated upon upgrading. To deactivate the optimized collector, create the system property **com.snc.pa.dc.hsql** and set it to `false`. For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Important:** Oracle databases are not supported. Other instances that still use the Performance Analytics Scores \[pa\_scores\] table are also not supported. The optimized data collector supports only instances where the indicator scores are on the two tables Scores Level 1 \[pa\_scores\_l1\] and Scores Level 2 \[pa\_scores\_l2\]. For more information, see [Migrating indicator scores](pa-scores-migration.md#).

The optimized data collector supports the following capabilities:

-   Ability to handle over 10 million records without adverse impact to performance.
-   Support for at least 10 breakdowns with breakdown matrix enabled. Breakdown support includes:
    -   Dot-walked conditions
    -   Two large breakdowns, with up to 1 million records
    -   Breakdown relations
-   Support for additional conditions on indicators and breakdowns.
-   Optimizations for Count Distinct aggregation.

**Note:** The default maximum number of records allowed per indicator source for data collection has been increased for optimized data collection. For more information, see the **com.snc.pa.dc.hsql.max\_row\_count\_indicator\_source** property in [Performance Analytics properties](../reference/pa-properties.md).

The optimizations stem from the use of an embedded database. A standard data collection job stores all scores in the node memory during the job. However, an optimized data collection job moves packets of scores to temporary storage on disk. At the end of the job, the scores are written to the scores tables and the temporary database is cleared.

**Note:** Memory optimization using lazy loading has been implemented to eliminate out-of-memory errors. However, this memory optimization could increase CPU usage and lengthen processing time for large jobs. For more information, contact Customer Service and Support.

**Parent Topic:**[Data collection process and logging](data-collection-process-logging.md)

