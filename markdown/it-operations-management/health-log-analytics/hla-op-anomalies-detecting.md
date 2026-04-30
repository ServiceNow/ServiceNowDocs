---
title: How Health Log Analytics generates alerts
description: ServiceNow Health Log Analytics identifies patterns in log data and learns pattern behavior. When its artificial intelligence engine detects anomalous behavior, it sends an event to the ServiceNow Event Management application. These predictive alerts enable operators to remediate emerging IT issues before they impact users.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [Health Log Analytics, HLA, HLA alerts, alert generation, alert metrics, anomaly, anomalies, anomalous, pattern, keywords, correlator, correlation]
breadcrumb: [Exploring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# How Health Log Analytics generates alerts

ServiceNow Health Log Analytics identifies patterns in log data and learns pattern behavior. When its artificial intelligence engine detects anomalous behavior, it sends an event to the ServiceNow Event Management application. These predictive alerts enable operators to remediate emerging IT issues before they impact users.

## What is an anomaly

There are many kinds of anomalous \(abnormal or unexpected\) behavior. In this example, the system tracks the baseline rate—the average number of events per minute—of particular messages. The chart shows the values for the previous day as the lightly peach-shaded area and the values for today as a blue line. The chart shows a dramatic deviation from the expected baseline values at around 10:10. This anomalous behavior generates an alert.

Anomalous behavior at around 10:10.

![Anomaly seen as a spike in the rate of messages of a particular type.](../image/anomaly-spike.png "Anomalous behavior")

Health Log Analytics uses the following methods to generate alerts:

## Alert metrics

Health Log Analytics monitors multiple metrics in the log stream to detect anomalous behavior. Each metric is associated with a unique source. A source is the combination of service instance and component. When the system identifies an anomalous pattern for a metric, it generates an alert.

Operators can provide the following types of feedback about alerts to "teach" the application whether a specific alert is significant or it should be muted.

-   A significant alert is more likely to be included in a Log Analytics group when the associated metric behaves anomalously. For more information, see [Mark an alert as significant](../task/hla-op-alert-make-significant.md)
-   Mute an alert for a specified source to eliminate distracting new alerts for unimportant issues. For more information, see [Mute an unimportant alert](../task/hla-op-alert-mute.md).
-   When the situation changes, you can return a significant metric to its default significance. You can also reactivate a muted metric to cause the system to start generating alerts again. For more information, see [Restore a muted alert or a significant alert](../task/hla-op-alert-restore-user-defined.md).

## Lexical keywords

Lexical keywords can indicate important issues in log entries.

The system sets a threshold for each lexical keyword. It bases the threshold on the normal occurrence pattern and frequency of the keyword. The system detects all occurrences of the keyword. When the pattern or frequency exceeds the threshold, the system generates an alert. For more information, see [View the lexical keywords that generate alerts](../task/hla-op-lexical-keywords-manage.md).

## Correlations

Log correlators are keys or values in log data that detect correlations between alerts. For example, a log correlator could detect when the interface ID of a particular network device occurs simultaneously in multiple warnings across different service instances. For more information, see [Using log correlators to detect relationships in log data](hla-op-correlator-what-is-a.md).

## Advanced alert filtering

Add advanced log alert filters to scan alerts for conditions that you specify. The filters reduce noise by dropping alerts that do not indicate a significant issue. While developing a filter, you can test, update, publish, or activate the filter at any time. For more information, see [Create advanced log alert filters](../task/hla-op-adv-alert-filter-crud.md).

## Custom alert rules

Define a Log Analytics alert rule when you encounter log data that should generate an alert. The alert rule generates an alert for a specified metric with a threshold that you specify and sets the properties of the generated alert. For more information, see [Add a Log Analytics alert rule](../task/hla-op-alert-rule-add.md).

**Parent Topic:**[Exploring Health Log Analytics](../../health-log-analytics-admin/concept/hla-exploring.md)

