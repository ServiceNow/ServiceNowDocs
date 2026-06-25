---
title: Node health performance metrics
description: The metrics provide the node health performance snapshot within the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-node-health-perf-metrics.html
release: australia
topic_type: reference
last_updated: "2026-05-23"
reading_time_minutes: 3
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Node health performance metrics

The metrics provide the node health performance snapshot within the ServiceNow AI Platform®.

## Node CPU Time

Node CPU Time is the absolute value in milliseconds of CPU utilization per node at a given data point in history. This metric will include activities occurring on a node that are outside the customer's control.

## Node Memory Mean

Node Memory Mean is the in use memory mean \(Megabytes\) per node at a given data point in history. This value normally ranges between 1000 MB and 2000 MB.

## Node Memory Max

Node Memory Max is the in use memory max \(Megabytes\) per node at a given data point in history. This value normally ranges between 1000MB to 2048MB. In the legend of the chart, the max of total available memory for the nodes of that particular instance has been provided to compare the maximum used memory vs. available memory for any node.

**Note:** In case for any node, maximum memory used reaches 95% of the total available memory at least 5 times in a past 15 minute time-period, that indicates that node memory is almost full.

## Node Garbage Collection Time

Garbage Collection Mean Time is the percentage of time spent doing Java garbage collection. It is the average of three samples; one sample being collected every 20 seconds. The values are collected for specific nodes and do not distinguish between the type of garbage collection. For example, young vs. old.

**Parent Topic:**[Overview of Instance Observer metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-observer-ovr-metric.md)

**Related topics**  


[Instance Observer reports overview]()

[Anomaly insights]()

[Feature availability based on package]()

[Auriga Intelligent Alert report]()

[Transaction or response metrics]()

[Database performance metrics]()

[Semaphores performance metrics]()

[Event queues performance metrics]()

[ECC Queue performance metrics]()

[Email performance metrics]()

[Scheduler performance metrics]()

[Job details performance metrics]()

[Host health performance metrics]()

[Standby replication Lag]()

[Pool Replication Lag]()

[Chat details performance metrics]()

[Cluster details performance metrics]()

[Load balancer performance metrics]()

[User information metrics]()

[Instance Data Replication]()

