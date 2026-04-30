---
title: Performance Analytics concepts
description: Performance Analytics uses terms and concepts that can differ from industry norms due to the unique nature of the ServiceNow platform.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Explore, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics concepts

Performance Analytics uses terms and concepts that can differ from industry norms due to the unique nature of the ServiceNow platform.

**Note:** Performance Analytics is used by other applications, such as Benchmarks. The information below describes the core Performance Analytics functionality. For information about other applications that use Performance Analytics, refer to the documentation for those applications.

Performance Analytics includes the following concepts and components:

## Key components

-   **[Indicators](c_Indicators.md)**

    \(KPIs\) define a performance measurement taken at regular intervals of a business service, an activity, or organizational behavior. These performance measurements result in a series of indicator scores over time. Businesses track these scores to measure current conditions and to forecast trends.

    Technically, an indicator combines a data set and a data aggregate, such as Count, along with optional conditions.

    Key characteristics of indicators include:

    -   Indicator scores can be generated automatically from a set of records defined in an [indicator source](performance-analytics-glossary.md#), entered manually, or calculated from other indicators.
    -   Indicator scores can be viewed or analyzed in Platform Analytics data visualizations and KPI Details. In the Core UI, view them in the Analytics Hub or in widgets on dashboards.
    For convenience, you can organize indicators thematically into an indicator group.

    Synonyms: Metrics, business metrics, KPIs

-   **[Breakdowns and elements](c_CreatingBreakdowns.md)**

    enable you to group or filter indicator scores by a qualitative attribute such as Priority, Category, or Assignment Group. You can apply a breakdown on the Analytics Hub, in KPI Details, and on dashboards.

    For example, you can look at the Number of Open Changes by Assignment Group. Or you can see the Number of New Changes by Priority.

    The values for each breakdown are called breakdown elements. For example, the Priority breakdown may have the elements Critical, High, and Low. Breakdowns are categorized as automated, manual, or external, depending on where these elements come from. Automated breakdown elements are specified in breakdown sources. Manual breakdowns have their elements entered manually to define an organization. Lastly, an external breakdown specifies the JDBC data source and SQL statement for retrieving breakdown elements.

    You cannot apply more than two levels of breakdown to an indicator.

    Synonyms: dimensions, drill-downs

-   **[Data collector](c_ClctData.md)**

    is the engine that takes periodic snapshots of your process tables and stores them in the Scores and Snapshots tables. You can set up data collector jobs to run automatically according to a schedule. Usually set a job schedule to match the frequency in the indicator source. One job usually generates scores for multiple indicators that use the same indicator source. You can also set up jobs that run manually, such as historical jobs, which you run only when collecting data for a new indicator.


## Other concepts

-   **Aggregate/Aggregation**

    can refer to either of the following functions:

    -   The Performance Analytics function of aggregating, or collecting, indicator scores over time. The indicator configuration includes the frequency with which indicator scores are collected.
    -   Statistical functions applied to collected indicator scores over a time period. For example, you can apply a 3-month SUM to indicator scores. Aggregation functions can be added either in the indicator form or later in the the Analytics Hub or widget. Aggregation functions in the Analytics Hub or widget are named time series.
-   **[Breakdown mappings](../task/create-breakdown-mapping.md#)**

    specify the relationships, or 'map,' breakdowns to indicator sources. A breakdown mapping either specifies a field on the indicator source or specifies a script that queries the indicator source. The latter is sometimes called a scripted breakdown mapping, and a breakdown with such a mapping is called a scripted breakdown.

-   **[Breakdown sources](../task/t_DefiningABreakdownSource.md)**

    specify which unique values, called breakdown elements, a breakdown contains. A breakdown source is defined as a set of records from a table or database view or as a bucket group. Multiple breakdowns can use the same breakdown source. For example, instead of seeing ALL assignment groups for the Number of Open Changes indicator, you can limit the element list to just those groups that are part of the change process by configuring the Breakdown Source.

-   **[Bucket groups](c_BucketGroups.md#)**

    are used to recategorize data so it can be used as a breakdown, for example by grouping a range of values into discrete buckets.

    To work with a bucket group, create a breakdown source that uses Bucket \[pa\_buckets\] as the facts table and specifies the bucket group in a condition. If a breakdown built on this source uses a breakdown mapping with a script, the breakdown groups the values that the script returns into buckets. If the breakdown mapping specifies a field instead of using a script, the breakdown groups the values of the mapped field into buckets.

    In the data architecture, bucket groups are defined in Bucket Group \[pa\_bucket\_groups\] records and buckets in Bucket \[pa\_buckets\] records. Each Bucket \[pa\_buckets\] record contains a Bucket Group field that is a reference to a Bucket Group \[pa\_bucket\_groups\] record.

-   **Day**

    A day in Performance Analytics is always defined as 24 hours. Performance Analytics does not use the concept of 'business days.'

-   **[Indicator sources](c_IndicatorSources.md#)**

    are data sets consisting of filtered records from one table or database view. An indicator source configuration specifies a table, such as Incident \[incident\], conditions for filtering records from that table, and a frequency that you base on the conditions. An indicator source cannot specify a rotated table. Multiple indicators can use the same indicator source. Data collection jobs query the database once for each indicator source. Thus, all indicators that use the same indicator source get data from the same point in time.

    Typically, an indicator tracks the situation on a certain date. The indicator source conditions usually include a date-related filter, such as **\[Opened\]\[on\]\[Today\]**. Indicators collected less frequently might specify a larger date range, such as **\[Closed\]\[on\]\[This month\]**.

-   **Scripted breakdown**

    is a breakdown that uses a script to query the indicator source as its breakdown mapping.

-   **Snapshots**

    are the lists of records \(sys\_ids\) that are collected at the time that the scores for those records are collected. A snapshot is made only for automated indicators with **Collect records** selected.

    The snapshot/list of records can be retrieved in the Analytics Hub or KPI Details.

    Snapshots are kept for the main indicator and for first-level breakdowns. Second-level breakdown snapshots are derived as an intersection of the two first-level breakdown snapshot lists.


-   **[Put a Spotlight on records](put-spotlight-on-records.md)**  
Use the Spotlight feature to illuminate records that you might overlook.
-   **[Try out Complimentary Performance Analytics for Incident Management](../reference/r_StUpPAInctMgmt.md)**  
Complimentary Performance Analytics for Incident Management is a limited version of Performance Analytics that is included in the base system, enabling you to become familiar with the functionality. Subscribe to Performance Analytics for complete functionality.

**Parent Topic:**[Exploring Performance Analytics](c_GetStartedwithPA.md)

