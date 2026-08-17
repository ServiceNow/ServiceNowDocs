---
title: Metric bounds sensitivity
description: Insights Explorer automatically widens metric bounds when too many anomalies are detected, reducing false alerts so you can focus on genuinely important issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/metric-intelligence/metric-bounds-sensitivity.html
release: australia
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [metric bounds, anomaly detection, sensitivity]
breadcrumb: [Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Metric bounds sensitivity

Insights Explorer automatically widens metric bounds when too many anomalies are detected, reducing false alerts so you can focus on genuinely important issues.

Reducing the number of anomalies enables you to focus on genuinely important issues while eliminating irrelevant anomalies.

The system uses measurement ranges, called 'bounds', to determine what is considered normal and abnormal metric behavior. These bounds are calculated automatically from your historical metric data.

## About variation ranges

A variation range is a measurement of how much your metric values typically vary from their average. The system calculates variation ranges automatically by analyzing your historical data. For example, if your CPU usage averages 50%:

-   A small variation range \(like 2%\) indicates that values stay consistent, typically between 48-52%.
-   A large variation range \(like 10%\) indicates that values fluctuate more widely, typically between 40-60%.

## How bounds are set

The system sets bounds by measuring how far away from the average a value can be before it's considered abnormal. The formula is: `Average +/- (multiplier x variation range)`.

The multiplier is a number that controls how wide or narrow the acceptable range is.

-   Smaller multipliers create narrower bounds and detect more anomalies.
-   Larger multipliers create wider bounds and detect fewer anomalies.

## CPU averages 50% and the standard deviation is 5%

|Multiplier|Bounds|
|----------|------|
|2|40% to 60% \(50%+/-10%\)|
|3|35% to 65% \(50%+/-15%\)|
|5|25% to 75% \(50%+/-25%\)|

## Automatic adjustment process

1.  High sensitivity detected: If 95% of a CI's metric values fall within a multiplier of 2, the system recognizes this as overly sensitive. As a result, too many anomalies are created, including some that aren't actually problems.
2.  The system widens the bounds: When high sensitivity is detected, the system automatically adjusts from a multiplier of 2 to 5, creating wider bounds and generating fewer, more meaningful anomalies.
3.  Normal sensitivity: If high sensitivity isn't detected, the system uses a multiplier of 3 for moderate bounds.

Any metric values falling outside the configured bounds are tagged as anomalies.

The multiplier values \(2, 3, and 5\) are set by default. For details on customizing these values, see [Sensitivity bounds properties for Insights Explorer metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/metric-bounds-properties.md).

