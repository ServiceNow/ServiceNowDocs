---
title: Semaphores performance metrics
description: The metrics provide the key performance indicators calculated at the instance level for the selected duration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-semaphores-performance-metrics.html
release: australia
topic_type: reference
last_updated: "2026-05-18"
reading_time_minutes: 12
keywords: [Semaphores, performance metrics]
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Semaphores performance metrics

The metrics provide the key performance indicators calculated at the instance level for the selected duration.

## Semaphore Default Mean

The average number of semaphores in use over a 1-minute period. In other words, the number of end user transactions being processed at once. The default semaphore pool is a group of threads that handle any transaction that is not handled by a more specific semaphore pool. Integration transactions, for example, are handled by the integrations pool \(API\_INT\) semaphore pool and thus would not go through the Default Semaphore pool. Most significant end user transactions will go through the Default semaphore pool with the exception of some very fast transactions like the UI Presence, Asynchronous Message Bus or Debugging transactions.

The Default semaphore pool has 16 threads, which is what the base system provides, and thus, the hypothetical max would be 16. In practice you would see extreme performance issues before reaching the 16 thread max and often a sustained usage of 10 or more might be indicative of a severe issue. Small spikes of semaphore usage on a single node can be ignored, but sustained spikes on a single node can be indicative of some type of performance issue. It is very rare that semaphore usage itself is the root cause of an issue — if more semaphores are needed, then a new node with 16 more semaphores is added to the ServiceNow cluster.

**Note:**

-   Some of you may have customized the number of Default semaphores or ServiceNow may have done this on your behalf. To find out how many Default semaphore threads are on your instance go to .
-   If a dangerously high spike of semaphore usage is observed the next step would be to find out if some resource has been maxed out.
-   If only one node is spiking at a time then it is likely an application layer issue. If all nodes are spiking at the same time, then it is likely a database issue.

## Semaphore Default Qdepth

The number of transactions which are currently queued in the default semaphore pools request queue awaiting processing. Note that the default request queue holds details of inbound end user transactions.

As transactions arrive at application nodes they are placed into the corresponding semaphore pools request queue. This queue is then drained as corresponding semaphores/threads become free and execute transactions from the request queue. As a result, it is common to see small numbers of requests in a semaphore pools request queue during normal operation. If, however, the request queue on one or more nodes sees spikes where the queue starts to fill, then this indicates either that there are spikes in transaction rates hitting those nodes, default threads on the nodes are busy executing some long running transactions, or performance of the node is periodically degrading such that transactional throughput decreases.

By default the default semaphore pools request queue can hold a maximum of 150 transactions. If the queue fills, additional transactions will be rejected with a 429 error indicating that the transaction could not be processed \(and potential loss of service\).

**Note:** Check metrics from impacted nodes to determine any unusual patterns. For example, patterns of default transactions which are extremely frequent/long running, an unusually high number of sessions, or evidence of memory/CPU contention. Take steps to remediate any issues discovered.

## Semaphore Session Waiters Mean

Semaphore session wait time refers to the duration a new request from a given session waits for the prior request from the same session to complete. In most scenarios, the ServiceNow AI Platform uses a session-based synchronization mechanism to process requests in the order they are received. High semaphore session wait times can indicate that an individual session may be executing long-running requests, causing other requests from the same session to wait. This is metric is the mean of that wait time.

## Semaphore Waiters Mean

Semaphore waiters refer to the duration a new request \(user or API\) waits for a semaphore to become available. Semaphores are used to process requests from users \(typically 16 max per node\) and APIs \(typically 4 max per node\) and are limited in number. If the semaphore waiters mean is high, it indicates semaphore contention and suggests a bottleneck due to resource constraints.

## Integrations Semaphore in use

The number of API\_INT semaphores/threads which are in-use \(i.e., currently executing a transaction\) on an application node at a given point in time.

Ideally all application nodes should have some free API\_INT semaphores available at all times — this guarantees the best response time for integrations transactions \(as there will be a semaphore available to execute a transaction as soon as it hits the semaphore pools request queue\).

**Note:** It is not uncommon for application nodes to have no free API\_INT semaphores especially during periods of peak integrations traffic. This is generally not an issue as long as individual transactions are generally being executed in a timely manner and the API\_INT request queue is not in danger of becoming exhausted.

## Integrations Semaphore Qdepth

The number of transactions which are currently queued in the API\_INT semaphore pools request queue awaiting processing. Note that the API\_INT request queue holds details of inbound integrations \(REST/SOAP/JSON\) transactions.

As transactions arrive at application nodes they are placed into the corresponding semaphore pools request queue. This queue is then drained as corresponding semaphores/threads become free and execute transactions from the request queue. As a result it is common to see small numbers of requests in a semaphore pools request queue during normal operation. If, however, the request queue on one of more nodes sees spikes where the queue starts to fill this indicates either that there are spikes in transaction rates hitting those nodes, API\_INT threads on the nodes are busy executing some long running transactions, or performance of the node is periodically degrading such that transactional throughput decreases. By default the API\_INT semaphore pools request queue can hold a maximum of 50 transactions. If the queue fills additional transactions will be rejected with a 429 error indicating that the transaction could not be processed \(and potential loss of service\).

**Note:** Check metrics from impacted nodes to determine any unusual patterns. For example, patterns of API\_INT transactions which are extremely frequent or long running, an unusually high number of sessions, or evidence of memory/CPU contention. Take steps to remediate any issues discovered.

## AMB Send In Use

The number of AMB Send semaphores/threads which are in-use \(that is, currently executing a transaction\) on an application node at a given point in time.

Ideally all application nodes should have some free AMB Send semaphores available at all times - this guarantees the best response time for corresponding transactions \(as there will be a semaphore available to execute a transaction as soon as it hits the semaphore pools request queue\).

**Note:** It is not uncommon for application nodes to have no free AMB Send semaphores especially during periods of peak integrations traffic. This is generally not an issue as long as individual transactions are generally being executed in a timely manner and the AMB Send request queue is not in danger of becoming exhausted.

## AMB Send Qdepth

The number of transactions which are currently queued in the AMB Send semaphore pools request queue awaiting processing. Note that the AMB Send request queue holds details of operations such as channel subscription or AMB message publication.

As transactions arrive at application nodes, they are placed into the corresponding semaphore pools request queue. This queue is then drained as corresponding semaphores/threads become free and execute transactions from the request queue. As a result, it is common to see small numbers of requests in a semaphore pools request queue during normal operation. If, however, the request queue on one of more nodes sees spikes where the queue starts to fill, this indicates either that there are spikes in transaction rates hitting those nodes, AMB Send threads on the nodes are busy executing some long running transactions, or performance of the node is periodically degrading such that transactional throughput decreases.

By default the AMB Send semaphore pools request queue can hold a maximum of 50 transactions. If the queue fills, additional transactions will be rejected with a 429 error indicating that the transaction could not be processed \(and potential loss of service\).

**Note:** Check metrics from impacted nodes to determine any unusual patterns for example patterns of AMB Send transactions which are extremely frequent or long running, an unusually high number of sessions, or evidence of memory or CPU contention. Take steps to remediate any issues discovered.

## AMB Receive in use

The number of AMB Receive semaphores or threads which are in-use \(that is, not currently executing a transaction\) on an application node at a given point in time.

Ideally all application nodes should have some free AMB Receive semaphores available at all times — this guarantees the best response time for corresponding transactions \(as there will be a semaphore available to execute a transaction as soon as it hits the semaphore pools request queue\).

**Note:** It is not uncommon for application nodes to have no free AMB Receive semaphores, especially during periods of peak integrations traffic. This is generally not an issue as long as individual transactions are generally being executed in a timely manner and the AMB Receive request queue is not in danger of becoming exhausted.

## AMB Receive Qdepth

The number of transactions which are currently queued in the AMB Receive semaphore pools request queue awaiting processing. Note that the AMB Receive request queue holds details of operations such as AMB message delivery.

As transactions arrive at application nodes they are placed into the corresponding semaphore pools request queue. This queue is then drained as corresponding semaphores or threads become free and execute transactions from the request queue. As a result it is common to see small numbers of requests in a semaphore pools request queue during normal operation. If, however, the request queue on one of more nodes sees spikes where the queue starts to fill, this indicates either that there are spikes in transaction rates hitting those nodes, AMB Receive threads on the nodes are busy executing some long running transactions, or performance of the node is periodically degrading such that transactional throughput decreases.

By default the AMB Receive semaphore pools request queue can hold a maximum of 50 transactions. If the queue fills, additional transactions will be rejected with a 429 error indicating that the transaction could not be processed \(and potential loss of service\).

**Note:** Check metrics from impacted nodes to determine any unusual patterns. For example, patterns of AMB Receive transactions which are extremely frequent or long running, an unusually high number of sessions, or evidence of memory or CPU contention. Take steps to remediate any issues discovered.

## Semaphore Rejected Metrics

-   **Semaphore Default Rejected**

    This represents the number of rejected executions of semaphore default for last minute. Semaphore default means the number of end user transactions processed at once.

-   **Integration Semaphore Rejected**

    This represents the number of rejected executions of API\_INT semaphore or thread for last minute on an application node at given point of time.

-   **AMB Receive Rejected**

    This represents the number of rejected executions of AMB receive semaphore or thread for last minute on an application node at given point of time.

-   **AMB Send Rejected**

    This represents the number of rejected executions of AMB send semaphore/thread for last minute on an application node at given point of time.


**Note:** The API\_INT is one of the semaphores used by the MID servers when communicating to the instance. If the API\_INT semaphores are exhausted, and the queue depth has reached the max queue depth, then the instance will return the error `Too Many Requests with code: 429` to any MID Server clients attempting communication. Because there are no available semaphores, the instance will not be able to receive any inputs from the MID Server. This could be due to the long-running transactions keeping the semaphores busy. Therefore, you can kill the transactions to free up the semaphores.

**Parent Topic:**[Overview of Instance Observer metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-observer-ovr-metric.md)

**Related topics**  


[Instance Observer reports overview]()

[Anomaly insights]()

[Feature availability based on package]()

[Auriga Intelligent Alert report]()

[Transaction or response metrics]()

[Database performance metrics]()

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

