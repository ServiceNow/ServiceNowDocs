---
title: Log anomaly detection
description: Health Log Analytics discovers patterns in your log data and learns their unique data behavior. When it finds an anomalous pattern, it sends an event to the ServiceNow Event Management application. You can use these predictive alerts to handle emerging IT issues before they impact users.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Log anomaly detection

Health Log Analytics discovers patterns in your log data and learns their unique data behavior. When it finds an anomalous pattern, it sends an event to the ServiceNow® Event Management application. You can use these predictive alerts to handle emerging IT issues before they impact users.

Health Log Analytics uses various methods to detect anomalies.

## Lexical keywords

Health Log Analytics scans your logs for words that can indicate important issues. Lexical keywords such as "crashed" or "failed" signal a condition that can merit attention.

The system sets a threshold for each lexical keyword that is based on what it considers the normal occurrence pattern and frequency of that keyword in your logs. When it scans your logs, it finds all occurrences of the keyword. If the number exceeds the threshold, it generates an alert.

For information about managing global keywords, see [Add, edit, or delete Health Log Analytics lexical keywords](../task/hla-lexical-keywords-admin.md). To create or delete keywords for a specific source type, see [Configure source type capabilities](../task/hla-source-types.md).

## Alert metrics

Health Log Analytics monitors multiple metrics as a means to detect anomalies. When it identifies an anomalous pattern for a metric, it generates an alert.

Operators can provide feedback about the generated alerts. Their feedback "teaches" Health Log Analytics that a specific alert is significant or irrelevant to them. The application then either raises the priority of the alert metric or mutes it to reduce noise.

When a metric is muted, Health Log Analytics removes the current alert and any other alerts based on that metric from the feed. It also stops generating new alerts from that metric. You can reactivate a muted alert metric. For more information, see [Restore normal importance to an alert metric](../../health-log-analytics-operator/task/hla-op-alert-restore-user-defined-sow.md).

## Correlations

Log correlators are keys or values in log data that detect correlations between alerts. For example, a log correlator could detect when the interface ID of a particular network device occurs simultaneously in multiple warnings across different service instances. For more information, see [Using log correlators to detect relationships in log data](../../health-log-analytics-operator/concept/hla-op-correlator-what-is-a.md).

## Advanced alert filtering

Add advanced log alert filters to scan alerts for conditions that you specify. The filters reduce noise by dropping alerts that do not indicate a significant issue. While developing a filter, you can test, update, publish, or activate the filter at any time. For more information, see [Create advanced log alert filters](../../health-log-analytics-operator/task/hla-op-adv-alert-filter-crud.md).

## Custom alerting rules

Define a Log Analytics alert rule when you encounter log data that should generate an alert. The alert rule generates an alert for a specified metric with a threshold that you specify and sets the properties of the generated alert. For more information, see [Add a Log Analytics alert rule](../../health-log-analytics-operator/task/hla-op-alert-rule-add.md).

## Learn

[What is anomaly detection?](https://www.servicenow.com/products/it-operations-management/what-is-anomaly-detection.html)

-   **[Add, edit, or delete Health Log Analytics lexical keywords](../task/hla-lexical-keywords-admin.md)**  
Manage the keywords that Health Log Analytics looks for in your log data.
-   **[View the lexical keywords that generate alerts](../../health-log-analytics-operator/task/hla-op-lexical-keywords-manage.md)**  
View the list of lexical keywords that can indicate important issues in log entries.
-   **[Add a log correlator to identify relationships in logs](../task/hla-correlators-add.md)**  
Log correlators are keys or values in log data that detect correlations between alerts. For example, a log correlator could detect when the interface ID of a particular network device occurs simultaneously in multiple warnings across different application services.

**Parent Topic:**[Using Health Log Analytics](../../health-log-analytics-operator/reference/hla-op-guide-binder.md)

