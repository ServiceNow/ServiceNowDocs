---
title: Database performance metrics
description: The metrics provide the database performance snapshot within the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-database-performance-metrics.html
release: australia
topic_type: reference
last_updated: "2026-05-18"
reading_time_minutes: 5
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Database performance metrics

The metrics provide the database performance snapshot within the ServiceNow AI Platform®.

## SQL Response Time

Reported mean of database response time. This is measured at the application layer with a timer that starts when a query is sent to the database and finishes when the response has been received.

Since this is measured at the application layer, it is therefore inclusive of time spent on the network between application server and database server as well as being susceptible to misleading increases during periods of application layer resource contention \(for example, CPU or JVM memory shortages\).

Most database queries in ServiceNow are extremely fast \(a few milliseconds or less\). When interpreting the mean SQL response time metric this is very important to understand because individual slow queries, that typically cause most ServiceNow performance issues, will likely not have an impact on this graph. Conversely, things that do have an impact on this graph are very not likely to signify actual business impacting issues — particularly things that cause it to jump for very short periods of time or things that cause it to grow slowly over time.

If the SQL response time quickly jumps up multiple times its normal rate and stays elevated for more than 15 minutes this might correlate to a service impacting issue, but must be validated with a primary performance indicator for further troubleshooting.

**Note:** This indicator is only a secondary indicator, which can be used to understand the context where it is used, and cannot be directly used for troubleshooting.

## Database Response Time by Type

The average response time of individual database transaction types. The database transaction types are stacked individually to give a granular breakdown. Database transaction types such as selects, inserts, updates and deletes are tracked individually. In case of a response time issue, the breakdown of individual statement types allows the user to narrow down the impacting query type.

## Database Throughput

The total number of database transaction types performed per data point. The database transaction types are stacked individually to give a granular breakdown. Database transaction types such as selects, inserts, updates and deletes are tracked individually. The breakdown of counts per type allows the user to identify any deviation in volume at the more granular level.

## Database Size

otal DBI Size \(based on sum of all tables\) along with any primary shard\(s\) size \(based on sum of all tables on shards\), this is calculated every 4 hours and can be used to visualize database growth over time.

## History List Length

The InnoDB history list is the undo logs which are used to store these modifications. This is a fundamental part of InnoDB's transactional architecture. InnoDB is an MVCC storage engine, which means you can start a transaction and continue to see a consistent snapshot even as the data changes. This is implemented by keeping old versions of rows as they're modified. They're kept in a linked list. The most recent version points to the previous one, which points to the previous one, and others.

**Note:** The value on larger DBs over 5-10 million is bad and on smaller DBs over 1 million.

## Threads Running

This metric represents the number of process threads running at the given point in time on the instance. When a thread is in the "running" state, it is actively using CPU resources to execute its code.

## Slow Queries

This metric represents the max time taken by slow queries. Slow queries refer to database queries that take longer to execute, typically due to lack of indexes, design, and others.

## InnoDBrowLock

This metric represents the duration InnoDB waits to acquire a row lock before timing out, specified in seconds. Adjusting it affects concurrency and performance in database transactions.

**Parent Topic:**[Overview of Instance Observer metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-observer-ovr-metric.md)

**Related topics**  


[Instance Observer reports overview]()

[Anomaly insights]()

[Feature availability based on package]()

[Auriga Intelligent Alert report]()

[Transaction or response metrics]()

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

[Load balancer performance metrics]()

[User information metrics]()

[Instance Data Replication]()

