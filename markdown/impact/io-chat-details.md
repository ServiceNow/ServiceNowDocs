---
title: Chat details performance metrics
description: For the operations team to get the insights of current load across main components of AWA channel infrastructure like queues and agents, and to monitor load during events of chat spikes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-chat-details.html
release: australia
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 3
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Chat details performance metrics

For the operations team to get the insights of current load across main components of AWA channel infrastructure like queues and agents, and to monitor load during events of chat spikes.

ServiceNow instance provides an end point that can provide instance based metrics for consumption by monitoring systems and store them for analysis and alerting use cases.

This consists of the following metrics:

-   **Chat Queued**

    Count of chat queued for the operations team.

-   **Agent Available**

    Number of CS agents available.

-   **Count of chat**

    Count of chat that was created, accepted, cancelled, or offered in CS queue.

-   **Chat Average Wait Time**

    Average waiting time for chat in the queue.

-   **Chat Arrival Ratio**

    Chats created vs. Agents available at a particular time period.

-   **Chat Acceptance Ratio**

    Count of chats accepted by number of agents available at a particular time period.

-   **Virtual agent**

    Interactions that were accepted, resolved, and transferred.


**Note:**

-   If Chat Queued count for Live Agents \(LA\) is higher and they are not receiving any chat for Virtual Agent \(VA\), this may be an indication that there is higher load on LA and VA responses for guiding users are limited.
-   If Chat arrival ratio or acceptance ratio is continuously trending higher, that may indicate that there is demand for availability of more live agents by the users.

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

[Cluster details performance metrics]()

[Load balancer performance metrics]()

[User information metrics]()

[Instance Data Replication]()

