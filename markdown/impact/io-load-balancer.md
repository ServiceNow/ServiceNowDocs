---
title: Load balancer performance metrics
description: The metrics provide the load balancer performance snapshot within the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-load-balancer.html
release: australia
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 4
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Load balancer performance metrics

The metrics provide the load balancer performance snapshot within the ServiceNow AI Platform®.

## Memory Utilization \(1 to 100 max\)

Memory Utilization is the percentage of memory that has been utilized at a given time. Memory percentage is the Memory utilization that occurred on the container level where your instance traffic is load balanced. If the instance traffic is managed over multiple DCs, each DC's container's memory utilization is provided. Usually there is one primary container that is handling most of the load and others are in standby mode.

## Memory Utilization \(max\)

Absolute value of Memory Utilization that has been utilized at a given time.

## CPU Utilization \(1 to 100 max\)

CPU Utilization is the percentage of CPU capacity that has been utilized at a given time. CPU percentage is the CPU utilization that occurred on the container level where your instance traffic is load balanced. If the instance traffic is managed over multiple DCs, each DC's container's CPU utilization is provided. Usually there is one primary container that is handling most of the load and others are in standby mode.

## CPU Utilization \(max\)

Absolute value of CPU Utilization that has been utilized at a given time.

## 2xx Responses \(Success\) Rate 5 mins

Total number of http responses/second with response code 2XX \(successful response to a http request\) that the server has sent over the last 5 minutes. Note that this is an aggregated value that includes all responses sent for the instance in question. The rate 5 mins is calculated based on two data points within the last 5 minutes window divided by time lapsed between them. For more information on 2xx responses, see [https://en.wikipedia.org/wiki/List\_of\_HTTP\_status\_codes\#2xx\_success](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#2xx_success).

## 5xx Responses \(Failure\) Rate 5 mins

Total number of HTTP responses/second with response code 5XX \(server error response to a HTTP request\) that the server has sent over the last 5 minutes. Note that this is an aggregated value that includes all responses sent for the instance in question. The rate 5 minutes is calculated based on two data points within the last 5 minutes window divided by time lapsed between them. For more information on 5xx responses, see [https://en.wikipedia.org/wiki/List\_of\_HTTP\_status\_codes\#5xx\_server\_errors](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#5xx_server_errors).

## Load balancer active \(processing\) HTTP requests

This represents the total number of active \(processing\) requests at a given timestamp. Note that this is an aggregated value that includes all responses sent for the instance in question.

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

[Node health performance metrics]()

[Host health performance metrics]()

[Standby replication Lag]()

[Pool Replication Lag]()

[Chat details performance metrics]()

[Cluster details performance metrics]()

[User information metrics]()

[Instance Data Replication]()

