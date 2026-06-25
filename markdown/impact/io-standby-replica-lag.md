---
title: Standby replication Lag
description: A read replica is a copy of the primary DB that reflects changes to the primary in almost real time, in normal circumstances. The lag represents the database server of the instance that is behind in seconds.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-standby-replica-lag.html
release: australia
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 2
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Standby replication Lag

A read replica is a copy of the primary DB that reflects changes to the primary in almost real time, in normal circumstances. The lag represents the database server of the instance that is behind in seconds.

Technical Support will see alert incidents created for database replication lag for either the standby \(far\) database or read replica databases.

**Note:** The cause will be DELETE or UPDATE statements. In the rare case, the cause is INSERT statements.

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

[Pool Replication Lag]()

[Chat details performance metrics]()

[Cluster details performance metrics]()

[Load balancer performance metrics]()

[User information metrics]()

[Instance Data Replication]()

