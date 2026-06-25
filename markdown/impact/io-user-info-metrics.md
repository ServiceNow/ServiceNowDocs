---
title: User information metrics
description: The metrics provide the user information performance snapshot within the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-user-info-metrics.html
release: australia
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 4
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# User information metrics

The metrics provide the user information performance snapshot within the ServiceNow AI Platform®.

## Session summary enduser

Sum of sessions that exist on each application node where at least one transaction has been executed; it's meant to be a gauge of real users. This includes sessions that are not logged in but have visited a page that is, login page.

Application nodes can generally support large numbers that is, a few hundred of sessions. If one or more nodes shows evidence of extremely high session counts that is, approaching or over 1000, the application node may suffer performance degradation due to a variety of causes.

**Note:**

-   If all application nodes show evidence of high session counts, review session timeouts to ensure that these are set to a reasonable value \(i.e., 30 minutes with 90 minutes absolute maximum\). If session timeouts are already reasonable, this may be an indication that additional application nodes should be added to the instance.
-   If one or more individual application nodes show unusually high session count, check whether other application nodes have recently restarted which may have caused active users to be 'moved' to remaining nodes causing a session imbalance. In this case, restart the node\(s\) with extremely high session count.

## Session summary loggedin

Sum of all active sessions that is, session objects in memory that exist on each application node for logged-in users.

Application nodes can generally support large numbers that is, a few hundred of active sessions/session objects. If one or more nodes shows evidence of extremely high session counts that is, approaching or over 1000, the application node may suffer performance degradation due to a variety of causes.

**Note:**

-   If all application nodes show evidence of high session counts, review session timeouts to ensure that these are set to a reasonable value that is, 30 minutes with 90 minutes absolute maximum. If session timeouts are already reasonable, this may be an indication that additional application nodes should be added to the instance.
-   If one or more individual application nodes show unusually high session count, check whether other application nodes have recently restarted which may have caused active users to be 'moved' to remaining nodes causing a session imbalance. In this case, restart the node\(s\) with extremely high session count.

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

[Load balancer performance metrics]()

[Instance Data Replication]()

