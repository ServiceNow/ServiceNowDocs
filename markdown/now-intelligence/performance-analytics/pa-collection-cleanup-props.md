---
title: Collection cleanup Performance Analytics properties
description: Several properties determine how long Performance Analytics scores and snapshots are maintained before the scheduled cleanup job deletes them.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Properties, Reference, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Collection cleanup Performance Analytics properties

Several properties determine how long Performance Analytics scores and snapshots are maintained before the scheduled cleanup job deletes them.

<table id="tbl_SystemPropertiesUsedToCleanPerformanceAnalyticsCollections"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.pa.dc.keep\_scores\_for.frequency

</td><td>

Maximum number of periods prior to today for which scores are collected and kept. The number of periods varies according to the score collection frequency, as follows: daily; weekly; bi-weekly; four weeks; monthly; bi-monthly; quarterly; fiscal quarterly; half-yearly; yearly; fiscal yearlyScores older than this limit are not collected during data collection.

 **Note:** This property can be overridden on individual indicators.

 -   Type: String
-   Default value: 732;105;53;40;60;30;20;20;20;10;10
-   Location: **Performance Analytics** &gt; **System** &gt; **Properties**

</td></tr><tr><td>

com.snc.pa.dc.keep\_snapshots\_for.frequency

</td><td>

Maximum number of periods prior to today for which lists of records \([snapshots](../concept/performance-analytics-glossary.md#)\) related to a score are collected and kept. The number of periods varies according to the score collection frequency, as follows: daily; weekly; bi-weekly; four weeks; monthly; bi-monthly; quarterly; fiscal quarterly; half-yearly; yearly; fiscal yearly.Snapshots older than this limit are not collected during data collection.

 **Note:** This property can be overridden on individual indicators.

 -   Type: String
-   Default value: 183;26;13;10;15;8;5;5;5;3;3
-   Location: **Performance Analytics** &gt; **System** &gt; **Properties**

</td></tr></tbody>
</table>**Parent Topic:**[Performance Analytics properties](pa-properties.md)

