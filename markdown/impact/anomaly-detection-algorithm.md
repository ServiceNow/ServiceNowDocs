---
title: Anomaly detection algorithm
description: Instance Observer is performing anomalies detection through the Z-score Statistical model, otherwise referred to as a univariate method.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Anomalies detection, Performance, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Anomaly detection algorithm

Instance Observer is performing anomalies detection through the Z-score Statistical model, otherwise referred to as a univariate method.

Anomaly detection analyzes a set of five metrics, Memory Max, Semaphore Mean, SQL response time, Server Response Time and Transaction count. The detection model has been validated with samplings with multiple instances of daily, weekly, and monthly level data.

Metrics representing anomalies using the Z-score model are Transaction count, Server Response Time &amp; SQL Response time. Metrics representing anomalies using an upper threshold-based approach are Semaphore Mean, Node max Memory, and Job execution. Refer to [Getting started with Performance charts](../task/io-getting-started-perf-charts.md) for details on the five metrics.

## Upper threshold-based methodology

Upper threshold-based methodology uses metrics with an exhausting limit. For example, metric A, which has a semaphore mean value of 14 or 16, which is used on the platform to limit the number of transactions that can occur on a node at one time to protect resources on the node. Metric B, memory max of 2 GB, where each node memory has a pre-defined maximum capacity. In all such similar cases, the situation is alarming only when the metrics are closer to the exhaustion limit. Even if the deviation is higher than the mean, but lower than the exhausting limit, then the threshold limit wouldn’t result in an alarm.

## Z-score methodology

A Z-score is  a numerical measurement that describes the relationship between a value to the mean of a group of values. Z-score is measured in terms of standard deviations from the mean. If a Z-score is 0, then the data point score is identical to the mean score.

The formula for calculating a Z-score is `z = (x-μ)/σ`:

-   `x`: The raw score of the data, as the moving average of the previous 15 minutes
-   `μ`: The data population mean that is the average of the previous four weeks on the same day, same hour, and same minute
-   `σ`: The data population standard deviation

When calculating Z-scores or making comparisons, it’s essential to consider these patterns of the analyzed data with inherent cyclical patterns. Cyclicity in a dataset refers to repeating patterns that occur at regular intervals, such as daily, weekly, or seasonal cycles. For example, sales data may exhibit higher values during holiday seasons or lower values during off-peak periods.

The cyclicity score is the similarity between two series which measure the similarity between two vectors and helps ensure that the Z-score model provides reliable insights and identifies true anomalies or outliers while considering the natural patterns of the data.

The cyclical score is calculated at the instance level with a data selection of four weeks divided into two-week vector increments, excluding weekends. The score returns the similarity score between the two, where a higher score indicates a more aligned similarity trend in the compared vector data.

**Parent Topic:**[Anomalies detection](../task/anomalies-detection.md)

