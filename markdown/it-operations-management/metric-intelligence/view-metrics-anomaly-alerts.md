---
title: View anomaly alerts
description: Anomaly alerts indicate deviation from projected metric values for monitored CIs. Anomaly alerts are separate from the regular IT alerts, and are not displayed in the Service Operations Workspace. You can define an anomaly alert promotion rule to generate an IT alert that is based on anomaly alerts.
locale: en-US
release: australia
product: Metric Intelligence
classification: metric-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Optimizing Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# View anomaly alerts

Anomaly alerts indicate deviation from projected metric values for monitored CIs. Anomaly alerts are separate from the regular IT alerts, and are not displayed in the Service Operations Workspace. You can define an anomaly alert promotion rule to generate an IT alert that is based on anomaly alerts.

## Before you begin

Role required: evt\_mgmt\_user

## About this task

The statistical model is used to calculate standard deviations, upper and lower bounds, and statistical outliers which are then used to detect anomalies. An anomaly occurs when metric values are out of the projected values according to the statistical model. The system monitors the frequency and persistence of statistical outliers across time to compute a score between 0-10 that indicates how abnormal a deviation is.

Metric Intelligence constantly generates anomaly alerts whenever the anomaly score is above zero. If there is a score that is above four and which has changed from the previous score, then it is sent to the instance. On the instance, the entire sequence of anomaly scores over time can then be displayed in the Insights Explorer.

Metric Intelligence monitors historical data to ensure that metric bounds are accurate and that the alerts close when the anomalous behavior stops. Metric Intelligence also ignores irrelevant anomalies based on the metric's labels. For example, if the available CPU increases from its upper bound of 50% to 60%, the **available** label is identified as an indicator that the behavior should not register as an anomaly. This is because the increase in available CPU represents a favorable outcome, even though the metric of 60% would otherwise represent an anomaly.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Metrics** &gt; **Anomaly Alerts**.

2.  In the **Alerts Anomalies** list view, double-click an alert that you want to view.

    Information about an anomaly alert includes details such as the metric value, promotion parameter, events relevant to the alert \(which appear in the alert's work notes\), and upper and lower bounds \(lower bounds cannot be less than 0\). Description includes details about why the anomaly alert was generated, and other details such as the metric name and the anomaly score.


## What to do next

Create an Advanced Promotion Engine Definition, to define the conditions which must be met to promote anomaly alerts to IT alerts. For details, see [Create a definition for the Advanced Promotion Engine](../../agent-client-collector/task/create-advanced-promotion-engine.md).

**Parent Topic:**[Optimizing Metric Intelligence](../../metric-intelligence/concept/optimizing-metric-intelligence.md)

