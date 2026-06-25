---
title: Pool Replication Lag
description: Pool replication lag is the number of seconds that a Standby database or a read replica database lags behind the primary database.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/io-pool-replica-lag.html
release: australia
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 2
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Pool Replication Lag

Pool replication lag is the number of seconds that a Standby database or a read replica database lags behind the primary database.

This may be an indication that a transaction committed on the primary may not yet be committed on the downstream database.

This number should ideally always be 0; however, a non-zero value usually indicates some workload that is performing an excessive amount of inserts, updates, and deletes to the database, causing a delay in processing the transaction bin logs on the standby or read replica database.

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

[Chat details performance metrics]()

[Cluster details performance metrics]()

[Load balancer performance metrics]()

[User information metrics]()

[Instance Data Replication]()

