---
title: Scheduler performance metrics
description: The metrics provide the Schedulers performance snapshot within the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-schedulers-perf-metrics.html
release: australia
topic_type: reference
last_updated: "2026-05-20"
reading_time_minutes: 5
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Scheduler performance metrics

The metrics provide the Schedulers performance snapshot within the ServiceNow AI Platform®.

## Completed Scheduled Jobs

The number of scheduled jobs completed per node.

There are many types of scheduled jobs. They could be scheduled reports, scheduled script executions, one-time jobs like SLA or Workflow Timers, or repeating jobs like Email Sender or Event Processor. In addition to what you might think of as traditional scheduled "jobs" there is also a couple special case of operations that run on the scheduled job queue called, Asynchronous business rules. These can be work that was triggered from the UI or an integration but runs as a scheduled job to achieve asynchronous behavior. Typical examples of Asynchronous business rules are Discovery Sensors or perhaps a job that iterates over a large number of child records, making so many updates that it would not be a good user experience to have to wait for them all to complete.

**Note:**

-   When scheduled job counts suddenly shoot up this can be concerning as it may overwhelm processing and cause lag.
-   This should be considered together with other job metrics like the scheduler age, scheduler queue length, and pending jobs counts.

## Scheduler mean queue age

The average age of all unprocessed jobs in an application node in memory scheduler queue \(i.e., the delta between the job being claimed by the node or placed in the queue and the point at which metrics were collected\). Note that this does not include time the job spent pending in the sys\_trigger table between its 'Next Action' time \(that is, when it should have run\) and when it was claimed.

A large scheduler mean queue age can indicate that an application node is struggling to process claimed jobs \(that is, those in its in memory queue\) in a timely manner.

**Note:** Check to see if the majority of worker threads on the corresponding node are busy executing long running scheduled jobs — in this scenario long running jobs should be investigated to reduce frequency/improve performance/stagger execution. In New York and later a node which is unable to process claimed jobs can send these jobs back to the sys\_trigger table to be claimed by other nodes. Check whether this functionality is working as expected

## Scheduler queue length

The number of claimed scheduled jobs in each application nodes in memory scheduler queue. Note that this does not include scheduled jobs which are currently executing on a worker thread on the application node.

It is common for application nodes to claim multiple jobs at once and therefore have a significant scheduler queue length at any point in time. If a single node has significant queue length for a sustained period \(that is, more than 60 minutes\), where queue length does not drop down to 0 and scheduler age is increasing, this may indicate the node has an issue processing scheduled jobs.

If multiple nodes see similar issues it may indicate either all nodes are having issues processing scheduled jobs or the instance is simply overwhelmed by scheduled jobs.

**Note:**

-   Check scheduled jobs executing on application nodes to determine type or source.
-   Address performance or scheduling of jobs as necessary to prevent them overloading worker threads.

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

