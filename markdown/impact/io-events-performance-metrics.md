---
title: Event queues performance metrics
description: The metrics provide the event performance snapshot within the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-events-performance-metrics.html
release: australia
topic_type: reference
last_updated: "2026-05-20"
reading_time_minutes: 4
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Event queues performance metrics

The metrics provide the event performance snapshot within the ServiceNow AI Platform®.

## Event Queue Backlog

This represents the total number of unprocessed events. These events are either in ready or queued states, ready is the start of the processing life cycle and queued means they have already been claimed by an event processor.

These metric values should remain relatively low. If the value gets too high, it is likely to indicate a processing delay.

## Events Processed Delta

This represents the delta change in the number of events that are in a processed state since the previous data collection point \(i.e., in the previous 2 seconds\). These events have fully processed by the event processor.

If the events processed delta is at zero, then it means that the queue has nothing further to process or there has been a failure in the event processor.

## Event Queue Backlog Delta

This represents the delta change in the number of events **unprocessed** \(increasing or decreasing backlog \) since the previous data collection \(that is, in the previous 2 minutes\).

## High Priority \(HIPR\) Events Backlog

This represents the total number of unprocessed events that were high priority. These high priority events are either in ready or queued states, ready is the start of the processing lifecyle and queued means they have already been claimed by an event processor.

These metric values should remain relatively low. If the value gets too high, it is likely to indicate a processing delay.

## High Priority \(HIPR\) Events Processed

This represents the delta change in the number of high priority events that are in a "processed" state since the previous data collection point \(that is, in the previous 2 seconds\). These high priority events have fully processed by the event processor.

If the high priority events processed delta is at zero, then it means that the queue has nothing further to process or there has been a failure in the event processor.

**Parent Topic:**[Overview of Instance Observer metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-observer-ovr-metric.md)

**Related topics**  


[Instance Observer reports overview]()

[Anomaly insights]()

[Feature availability based on package]()

[Auriga Intelligent Alert report]()

[Transaction or response metrics]()

[Database performance metrics]()

[Semaphores performance metrics]()

[ECC Queue performance metrics]()

[Email performance metrics]()

[Scheduler performance metrics]()

[Job details performance metrics]()

[Node health performance metrics]()

[Host health performance metrics]()

[Standby replication Lag]()

[Pool Replication Lag]()

[Chat details performance metrics]()

[Cluster details performance metrics]()

[Load balancer performance metrics]()

[User information metrics]()

[Instance Data Replication]()

