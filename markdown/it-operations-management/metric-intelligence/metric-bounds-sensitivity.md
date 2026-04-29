---
title: Metric bounds sensitivity
description: When monitoring metrics in Insights Explorer, the system might detect too many anomalies if the sensitivity settings are too narrow. When detecting a large number of anomalies, the system automatically adjusts to reduce false alerts.
locale: en-US
release: australia
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Metric bounds sensitivity

When monitoring metrics in Insights Explorer, the system might detect too many anomalies if the sensitivity settings are too narrow. When detecting a large number of anomalies, the system automatically adjusts to reduce false alerts.

The system uses measurement ranges, called 'bounds', to determine what is considered normal and abnormal metric behavior. These bounds are calculated automatically from your historical metric data.

## About standard deviation

Standard deviation is a measurement of how much your metric values typically vary from their average. The system calculates standard deviation automatically by analyzing your historical data. For example, if your CPU usage averages 50%: A small standard deviation \(like 2%\) indicates that values stay consistent, typically between 48-52%. A large standard deviation \(like 10%\) indicates that values fluctuate more widely, typically between 40-60%.

## How bounds are set

The system sets bounds by measuring how many standard deviations away from the average a value can be before it's considered abnormal. The formula is: **Average +/- \(number of standard deviations x standard deviation\)**.

The multiplier is a number that controls how wide or narrow the acceptable range is.

-   Fewer standard deviations creates narrower bounds and detects more anomalies.
-   More standard deviations creates wider bounds and detects fewer anomalies.

## CPU averages 50% and the standard deviation is 5%

|Standard deviations|Bounds|
|-------------------|------|
|2|40% to 60% \(50%+/-10%\)|
|3|35% to 65% \(50%+/-15%\)|
|5|25% to 75% \(50%+/-25%\)|

## Automatic adjustment process

1.  High sensitivity detected: If 95% of a CI's metric values fall within 2 standard deviations of the average, the system recognizes this as overly sensitive. As a result, too many anomalies are created, including some that aren't actually problems.
2.  The system widens the bounds: When high sensitivity is detected, the system automatically adjusts from 2 to 5 standard deviations, creating wider bounds and generating fewer, more meaningful anomalies.
3.  Normal sensitivity: If high sensitivity isn’t detected, the system uses 3 standard deviations for moderate bounds.

Any metric values falling outside the configured bounds are tagged as anomalies.

The number of standard deviations \(2, 3, and 5\) is set by default. For details on customizing these values, see [Sensitivity bounds properties for Insights Explorer metrics](../reference/metric-bounds-properties.md).

