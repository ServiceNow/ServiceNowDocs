---
title: Data collector Performance Analytics properties
description: Data collector properties enable you to configure various limits for Performance Analytics data collection. The properties are configured to safeguard the data collection process. The default values are appropriate for most environments.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Performance Analytics properties, Performance Analytics reference, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Data collector Performance Analytics properties

Data collector properties enable you to configure various limits for Performance Analytics data collection. The properties are configured to safeguard the data collection process. The default values are appropriate for most environments.

**Note:** Try not to increase these values beyond what is necessary. Depending on your implementation, increases in these values may impact performance. If possible, consult a domain expert or implementation partner, who may be able to find an alternative solution to increasing the property value.

<table id="tbl_PerformanceAnalyticsDataCollectionProperties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.pa.dc.script\_timeout

</td><td>

The maximum time in seconds that a script is allowed to run during a data collection cycle, such as an indicator source script or a breakdown script. This limit applies individually for each record processed by the data collection job. If a script exceeds this limit, the data collection job skips the current record.

 If your scripts frequently reach the default limit, simplify the scripts as much as possible before modifying this property.

 -   Type: integer
-   Default value: 30

</td></tr><tr><td>

com.snc.pa.dc.query\_time\_limit

</td><td>

The maximum duration in minutes that a single query for a data collection job can run before a warning is logged. -   Type: integer
-   Default value: 60

</td></tr><tr><td>

com.snc.pa.dc.max\_row\_count\_indicator\_source

</td><td>

The maximum number of records that a job can collect from a single indicator source. **Important:** This property applies only to jobs that do not use optimized data collection. If optimized data collection is enabled, which is the default condition, see the property **com.snc.pa.dc.hsql.max\_row\_count\_indicator\_source**.

 This limit applies separately to each indicator source included in a data collection job. The number of indicators associated with each indicator source does not affect this limit.

 For example, if a data collection job collects scores for 12 indicators from three indicator sources, the job can collect a maximum of 150,000 records by default: 50,000 from each indicator source.

 **Warning:**

-   If the number of records that an indicator source contains is higher than the value of this property, no indicators are collected for this indicator source.
-   This property can be overridden on individual indicator sources. In this case, the individual indicator source might not be collected even though the row count is lower than the value of **com.snc.pa.dc.max\_row\_count\_indicator\_source**.

 -   Type: integer
-   Default value: 50,000

</td></tr><tr><td>

com.snc.pa.dc.hsql.max\_row\_count\_indicator\_source

</td><td>

The maximum number of records that a job can collect from a single indicator source.**Important:** This property applies only to jobs that use optimized data collection. Otherwise, **com.snc.pa.dc.max\_row\_count\_indicator\_source** applies. For more information, see [Optimizing data collection](../concept/optimized-data-collection.md).

 This limit applies separately to each indicator source included in a data collection job. The number of indicators associated with each indicator source does not affect this limit.

 For example, if a data collection job collects scores for 12 indicators from three indicator sources, the job can collect a maximum of 3 million records by default: 1 million from each indicator source.

 On upgrade to a later version than San Diego, the optimized data collector becomes enabled. This property then overrides **com.snc.pa.dc.max\_row\_count\_indicator\_source**. The value of the new property is set to the default 1 million, unless the value of **com.snc.pa.dc.max\_row\_count\_indicator\_source** was more than 1 million. In the latter case, the original property value is retained.

 **Warning:**

-   If the number of records that an indicator source contains is higher than the value of this property, no indicators are collected for this indicator source.
-   This property can be overridden on individual indicator sources. In this case, the individual indicator source might not be collected even though the row count is lower than the value of **com.snc.pa.dc.hsql.max\_row\_count\_indicator\_source**.

 -   Type: integer
-   Default value: 1,000,000

</td></tr><tr><td>

com.snc.pa.dc.max\_breakdown\_elements\_limit

</td><td>

Maximum number of [breakdown elements](../concept/performance-analytics-glossary.md#) retrieved by data collection for each [breakdown source](../concept/performance-analytics-glossary.md#). If the number of elements on a breakdown source exceeds this limit, the data collector does not collect scores from that breakdown source.

 **Important:** This property applies only to jobs that do not use optimized data collection. For optimized data collection, see the property **com.snc.pa.dc.hsql.max\_breakdown\_elements\_limit**. Also see [Optimizing data collection](../concept/optimized-data-collection.md).

 This limit applies separately to each breakdown source included in a data collection job. The number of breakdowns associated with each breakdown source does not affect this limit.

 For example, if a data collection job collects scores for 12 breakdowns from three breakdown sources, the job can collect a maximum of 30,000 records by default: 10,000 from each breakdown source.

**Warning:** Increasing this limit increases the processing load on the node.

 This property is handled differently depending on whether nested collection is enabled:

 If nested collection is enabled, only elements with non-null scores count against this limit. The count is taken as the data collection job runs. When the number of elements with scores reaches this limit, the breakdown source is disabled and the scores cleared from memory.

 When nested collection is not enabled, all elements of a breakdown source are counted against the limit. The count is taken before any scores are collected.

 Consider a case where the default limit of 10,000 elements is applied to a breakdown source with 1 million elements of which 5,000 have scores. Under nested collection, the job collects the scores for those 5,000 elements. With nested collection turned off, the job does not collect any scores for this breakdown source.

 -   Type: integer
-   Default value: 10,000

</td></tr><tr><td>

com.snc.pa.dc.hsql.max\_breakdown\_elements\_limit

</td><td>

Maximum number of breakdown elements retrieved by data collection for each breakdown source. If the number of elements on a breakdown source exceeds this limit, the data collector does not collect scores from that breakdown source.

 **Important:** This property applies only to jobs that use optimized data collection. Otherwise, **com.snc.pa.dc.max\_breakdown\_elements\_limit** applies. For more information, see [Optimizing data collection](../concept/optimized-data-collection.md).

 This limit applies separately to each breakdown source included in a data collection job. The number of breakdowns associated with each breakdown source does not affect this limit.

 By default, no limit is set on the number of breakdown elements. If you experience performance issues on jobs with breakdown sources with large numbers of elements, consider setting a limit in consultation with Customer Service and Support.

 On upgrade to a later version than San Diego, optimized data collection is activated. This property then overrides **com.snc.pa.dc.max\_breakdown\_elements\_limit**.

 -   Type: integer
-   Default value: -1

</td></tr><tr><td>

com.snc.pa.dc.max\_breakdown\_elements\_level2\_limit

</td><td>

Maximum number of breakdown elements allowed in a matrix of two breakdowns. If this limit is exceeded, the breakdown elements in the matrix are not collected.

 **Important:** This property applies only to jobs that do not use optimized data collection. For optimized data collection, see the property **com.snc.pa.dc.hsql.max\_breakdown\_elements\_level2\_limit**. Also see [Optimizing data collection](../concept/optimized-data-collection.md).

 For example, with the default limit of 1 million elements, a first-level breakdown with 10,000 elements, and a second-level breakdown with 500, the resulting matrix of 5 million elements is not collected. If the first-level breakdown had only 1,000 elements, the resulting 500,000 elements would be collected.

**Note:** This limit is also affected by the **com.snc.pa.dc.max\_breakdown\_elements\_limit** property. No breakdown matrix is collected where one of the breakdown sources exceeds that limit.

-   Type: integer
-   Default value: 1,000,000

</td></tr><tr><td>

com.snc.pa.dc.hsql.max\_breakdown\_elements\_level2\_limit

</td><td>

Maximum number of breakdown elements allowed in a matrix of two breakdowns. If this limit is exceeded, the breakdown elements are not collected.

 **Important:** This property applies only to jobs that use optimized data collection. See [Optimizing data collection](../concept/optimized-data-collection.md).

 By default, no limit is set on the number of breakdown elements in a matrix. If you experience performance issues on jobs with breakdown sources with large numbers of elements, consider setting a limit in consultation with Customer Service and Support.

 **Note:** This limit could be affected by the **com.snc.pa.dc.hsql.max\_breakdown\_elements\_limit** property. If that limit is set, no breakdown matrix is collected where one of the breakdown sources exceeds that limit.

 -   Type: integer
-   Default value: -1

</td></tr><tr><td>

com.snc.pa.dc.max\_error\_count

</td><td>

The maximum number errors that may occur for a single data collection job run before data collection is stopped.Errors during data collection usually occur due to an invalid script, or when encountering the script timeout limit.

 If you encounter this limit, review any scripts that run during data collection to ensure that they are valid and perform as expected.

 -   Type: integer
-   Default value: 500

</td></tr><tr><td>

com.snc.pa.dc.max\_records

</td><td>

Maximum number of sys IDs that are stored in a single Snapshot \[pa\_snapshots\] record. A Snapshot record is created for each collected score, and a field in this record contains all the sys IDs of the records that contribute to the score. If this limit is exceeded, a Snapshot record is created with the maximum number of records. This limit applies only when **Collect records** is selected for an indicator. For example, say you are using the default limit of 5,000 and you run a job where 5,010 records contribute to the score. The system creates a Snapshot record with a comma-separated list of the first 5,000 sys IDs in the sys\_id field.

 Generally, the default limit provides enough detail into collected records. Increasing this limit may impact performance during data collection or when performing operations on the Snapshot table.

 -   Type: integer
-   Default value: 5000

</td></tr></tbody>
</table>**Parent Topic:**[Performance Analytics properties](pa-properties.md)

