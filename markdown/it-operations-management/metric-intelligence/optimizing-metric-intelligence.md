---
title: Optimizing Metric Intelligence
description: You can perform a variety of tasks to optimize your use of Metric Intelligence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/metric-intelligence/optimizing-metric-intelligence.html
release: australia
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Metric Intelligence, IT Operations Management]
---

# Optimizing Metric Intelligence

You can perform a variety of tasks to optimize your use of Metric Intelligence.

-   **[Create an anomaly test rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/anomaly-model-testing.md)**  
To use the anomaly model testing, create an anomaly test rule in which you specify up to 20 metric series to test anomaly detection for. Run the anomaly test, and after it completes, use the provided URL to open the Insights Explorer which is pre-loaded with the model testing results.
-   **[View metric to CI and resource binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/view-metric-to-CI-binding.md)**  
View the metric to CI and resource binding results, including details for failed bindings which you can use to mitigate the failure. If Metric Intelligence cannot map and bind a metric to a CI or to a resource, then that CI or resource is not included in anomaly detection until it is properly mapped.
-   **[Disable a metric for a CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/disable-metric-per-ci.md)**  
Metric Intelligence can be configured to collect significant amounts of data, some of which might not be necessary. To improve performance, you can disable a specific metric for a specific CI to stop processing data related to the specified metric and CI.
-   **[Disable event collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/disable-event-collection.md)**  
For performance reasons, you might want to disable the collection of events from a data source from which metric data is also collected. You can disable event collection for data sources such as Nagios XI server, SolarWinds monitoring system, and Zabbix server.
-   **[Configure anomaly score thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/cnfgr-anomaly-score-thresholds.md)**  
Metric Intelligence scores anomalies on a range 0-10. This range is broken down to the five levels of event severities, each represented by a different color in the Insights Explorer and in the Anomaly Map. You can configure the anomaly score threshold for each level of severity.
-   **[View anomaly alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/view-metrics-anomaly-alerts.md)**  
Anomaly alerts indicate deviation from projected metric values for monitored CIs. Anomaly alerts are separate from regular IT alerts. They appear in the Service Operations Workspace but not in Express List. You can define an anomaly alert promotion rule to generate an IT alert that is based on anomaly alerts.
-   **[View metric charts in Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/view-metric-charts-workspace.md)**  
Agent Workspace for Metric Intelligence provides easy access to metric charts for a CI. On an alert form, you can drill down to important metric charts for the CI that is associated with the alert.
-   **[Configure metric charts for Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/configure-metric-chart-workspace.md)**  
Configure the set of Metric Intelligence metric charts, chart types, and other chart characteristics, that appear in Agent Workspace.
-   **[View self-health monitoring statistics for Metric Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/xmlstats-oi-self-health.md)**  
Monitor the status of components and processes of Metric Intelligence. Use the XMLStats page to view statistics and diagnostic details that can help with troubleshooting issues with Metric Intelligence.
-   **[Verify that the definitions for the Advanced Promotion Engine are active](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/verify-ape-definition-active.md)**  
Verify that the Advanced Promotion Engine definitions that come with the base system are active.
-   **[Create a definition for the Advanced Promotion Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/create-advanced-promotion-engine.md)**  
Create a definition for the Advanced Promotion Engine so that you can define the conditions for promoting the anomaly alerts to IT alerts. By promoting the alerts that meet the conditions, only the most relevant alerts move to the table.
-   **[View the promoted events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/view-promoted-events.md)**  
View the anomaly alerts that the Advanced Promotion Engine promoted to IT events. Viewing IT events enables you to track the source of the event.
-   **[View the promoted anomaly alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/view-promoted-alerts.md)**  
View the anomaly alerts that the Advanced Promotion Engine promoted to events, which are then processed as alerts in the All Alerts table. Viewing alerts in the All Alerts table enables you to track the source of the alert.
-   **[Create metric rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/create-metric-rules.md)**  
Create a metric rule to determine the metric, the threshold values and ranges, and the severity level of generated events. You can add a filter that determines the Configuration Items \(CI\) types or resources for which you receive alerts. For example, you can configure a filter to receive alerts only for Windows servers.
-   **[Create an event rule to bind metric events to host CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/event-rule-bind-metrics-to-host.md)**  
Create event rules to explicitly allow binding of metric events to host CIs.

**Parent Topic:**[Metric Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/operational-metrics.md)

