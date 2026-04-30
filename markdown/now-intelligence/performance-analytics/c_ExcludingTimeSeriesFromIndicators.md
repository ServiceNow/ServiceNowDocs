---
title: Exclude time series from an indicator
description: Some time series aggregations are inappropriate to apply to some indicators. You can exclude time series on automated, formula, and manual indicators. Excluded time series are not selectable from the Analytics Hub, KPI Details, or widgets. Other time series remain selectable.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Exclude time series from an indicator

Some time series aggregations are inappropriate to apply to some indicators. You can exclude time series on automated, formula, and manual indicators. Excluded time series are not selectable from the Analytics Hub, KPI Details, or widgets. Other time series remain selectable.

To exclude a time series from an indicator, select the time series in the **Time series exclusions** related list on the indicator form.

One use case for excluding time series is the logical relationship between the indicator aggregation and the time series aggregation. For example, you may not want to allow a time series aggregation that takes a SUM or an AVG of an indicator that itself is an average.

|Indicator aggregate|Consider excluding time series:|
|-------------------|-------------------------------|
|Average|All SUM, AVG. All partial periods \(+\).|
|Sum|All SUM|
|Minimum|All SUM|
|Maximum|All SUM|

You may also want to exclude time series based on the indicator unit type. For example, if you have an indicator whose score is a percentage value, you may not want to display any SUMs of these percentages. Similarly, time series aggregations for indicators which themselves are measured in days, weeks, months, quarters, or years may not make much sense.

As a final point, consider the subject matter of the indicator. Some time series aggregations may not be appropriate for an indicator for qualitative reasons.

