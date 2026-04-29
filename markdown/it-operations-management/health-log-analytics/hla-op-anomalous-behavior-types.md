---
title: Types of anomalous behavior in Health Log Analytics
description: Anomalous behavior in a CI or a service can indicate an important issue. For example, a spike in the frequency or number of messages of a particular type can indicate a problem.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Types of anomalous behavior in Health Log Analytics

Anomalous behavior in a CI or a service can indicate an important issue. For example, a spike in the frequency or number of messages of a particular type can indicate a problem.

## Understanding anomalies

To build models of expected behavior, Health Log Analytics monitors the log stream to learn baselines for patterns, metrics, and gauges over various time periods. Time periods can be hourly, daily, weekly, or unlimited. Behavior that departs from the learned models is considered anomalous behavior.

## Types of log property

-   **Pattern**

    A pattern is a value or rate that repeats, whether in text, time, or relationships.

-   **Meter**

    A meter property is a numeric or text value. For example, a status code, a response code, an action, or a pattern.

-   **Gauge**

    A gauge property has a numerical value that is reported continuously. Gauge properties represent operations that consume resources. For example, CPU usage, memory usage, or response time.


## How anomalies appear in Health Log Analytics

The Anomaly card illustrates the anomalous activity that led to the alert.

-   The blue line shows the recent anomalous activity.
-   On some charts, the lightly shaded area indicates the expected \(learned baseline\) behavior.

    A peach-shaded area represents the baseline values for the same hour one day earlier. A pink-shaded area shows the values for the same period in the previous week.

-   Click the information icon to see how the anomaly was identified: ![Information icon](../image/icon-info.png).

In this example, the peach-shaded area shows the same data for the same hour one day earlier. The spike in the metric value \(events per minute\) is clearly visible.

![Anomaly card identifies and illustrates anomalous behavior.](../image/anomaly-spike.png "Anomaly card")

## Kinds of anomalies

|Behavior|Description|
|--------|-----------|
|New behavior|A pattern that has not ever been seen. The New Behavior alert type does not display a chart.|
|Signal dead/Stopped appearing|All pattern or log data from a source has stopped. There has been no signal for at least five minutes.|
|Signal alive/Appearing again|A pattern or log data from a "dead" source is appearing again​. For a baseline of one hour, a pattern is "dead" if it appears less than once per minute.|
|Anomaly above average or below average|Activity that deviates from expected baseline behavior for pattern or meter or gauge metrics, such as keywords metrics or severity metrics.|
|Baseline reference​ increase or decrease|An increase or decrease in the value or volume of a log property as compared to the one-hour or one-week baseline.|
|Correlation of severity and keyword alerts|An increase in the volume of a severity level or keyword.|

