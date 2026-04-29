---
title: Exploring MetricBase
description: Collect, retain, analyze, and act on time-series data using MetricBase.
locale: en-US
release: australia
product: MetricBase
classification: metricbase
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Exploring MetricBase

Collect, retain, analyze, and act on time-series data using MetricBase.

## MetricBase overview

MetricBase helps you work with large amounts of data by using a smaller summary of that data that is stored in the MetricBase database.

-   Integrate MetricBase seamlessly with ServiceNow IoT-based applications that monitor or act on large amounts of machine-generated data.
-   Trigger flows in Workflow Studio based on time-series data in MetricBase.
    -   Generate an email if the average CPU usage is more than 85% in the last 5 minutes.
    -   Generate an email if MetricBase detects a gap in data submitted for 10 minutes or more.
    -   Generate an alert if the average of the collected data is less than 10 or greater than 500 in the last 5 minutes.
    -   Generate an alert if memory usage is likely to exceed 90% in the next 10 minutes.
-   Visualize MetricBase data using time-series charts.
-   Use the Reporting application to graph the time-series data that is stored in MetricBase.
-   Detect anomalies by training a machine language model and execute a Workflow Studio trigger when an anomaly is detected.

MetricBase works with:

-   An instance that stores machine-generated data
-   A server that has the MetricBase application and database

## MetricBase users

|User|Description|
|----|-----------|
|Administrator|An administrator collects, retains, analyzes, and acts on time-series data using MetricBase.|

## MetricBase workflow

The following figure shows that machine-generated data is sampled every 4 seconds. You send the average of the values in each sampling period to the MetricBase database, which stores the data until its expiration date.

![Infographic showing how machine-generated data is sampled at regular intervals and sent to the MetricBase database by the API. For details, refer to the following description.](../image/mb-time-series-data.png "Storing time series data")

1.  The administrator specifies a metric to store and how often to collect it by creating a time-series definition in MetricBase.
2.  The administrator sends data from the instance to the MetricBase server using the MetricBase REST or JavaScript APIs.
3.  The administrator configures trigger definitions that execute flows based on time-series data in MetricBase.
4.  The administrator configures and trains predictive models in MetricBase to detect anomalies and execute flows when new data is significantly different than the trained data.
5.  The administrator monitors collected data using time-series charts in MetricBase. Time-series data remains in the MetricBase database for a prescribed amount of time, after which MetricBase deletes the data.

## MetricBase benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Store time series summary of a large collection of data|[Create a time-series definition in MetricBase](../task/set-up-data-monitoring.md)|Administrator|
|Insert and retrieve time-series data from the MetricBase database|[Developer resources](developer-resources.md)|Administrator|
|Access and visualize time-series data in the MetricBase database|[Accessing MetricBase data](accessing-metricbase-data.md)|Administrator|
|Trigger flows when new data is significantly different than the trained data|[Detecting anomalies in MetricBase data using predictive models](metricbase-predictive-models.md)|Administrator|
|Trigger flows that can log incidents, send emails, and create other alerts|[Triggering flows using MetricBase data](metricbase-triggers.md)|Administrator|

## What to explore next

To learn more about configuring and using MetricBase, see:

-   [Configuring MetricBase](configuring-metricbase.md)
-   [Defining and collecting MetricBase data](collecting-metricbase-data.md)
-   [Triggering flows using MetricBase data](metricbase-triggers.md)
-   [Managing MetricBase](maintain-metricbase.md#)
-   [MetricBase reference](reference-metricbase.md)

