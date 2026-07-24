---
title: Hermes background jobs
description: These background jobs are associated with Hermes settings. The table lists their default run frequencies and descriptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/multi-instance-framework-hermes/hermes-settings-background-jobs.html
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: reference
last_updated: "2026-05-21"
reading_time_minutes: 2
keywords: [Hermes, Hermes background jobs, scheduled jobs, hermes\_admin, maint]
breadcrumb: [Reference, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Hermes background jobs

These background jobs are associated with Hermes settings. The table lists their default run frequencies and descriptions.

|Job name|Frequency|Description|
|--------|---------|-----------|
|Hermes Active Cluster Heartbeat|Every 10 min|Sends periodic heartbeats to indicate node availability and monitors cluster health status.|
|Hermes Health Status Check|Every 1 min|Monitors the health of Hermes services and checks that all components are running correctly.|
|Auto Flush hermes\_system\_status|Scheduled|Automatically cleans up old records from the hermes\_system\_status table.|
|Hermes Failover State Refresh Job|On trigger|Monitors and updates the failover state across nodes to help recover from node failures.|
|Hermes IP ACL Publish Job|Every 5 min|Publishes IP ACL updates. Only runs when IP ACL is enabled.|
|Auto Flush hermes\_ip\_filtering\_audit|Scheduled|Automatically cleans up old records from the hermes\_ip\_filtering\_audit table.|
|Hermes Kafka Client Metrics Collection|Every 2 min|Collects detailed Apache Kafka client metrics across all nodes.|
|Hermes Usage Metrics Aggregation and Clean Up Daily|Daily at 4AM GMT|Aggregates hourly metrics into daily summaries and cleans up old hourly data after aggregation.|
|Hermes Usage Metrics Aggregation Monthly|2nd day of month, 4:00 a.m. GMT|Aggregates daily metrics into monthly summaries.|
|Hermes Flush Expired Idle Consumers|Hourly|Cleans up inactive consumer connections to free system resources and prevent resource leaks.|
|Auto Flush hermes\_metrics\_collection|Scheduled|Automatically cleans up records older than approximately 1 day from the hermes\_metrics\_collection table.|
|Hermes Periodic Purge|Every 10 min|Performs regular cleanup of temporary data.|
|Hermes Metadata Collection|Every 30 min|Collects and updates topic, cluster, consumer, producer, broker, and partition metadata.|
|Auto Flush hermes\_usage\_metrics \(Daily\)|Scheduled|Deletes hermes\_usage\_metrics records older than approximately 1 year.|
|Auto Flush hermes\_usage\_metrics \(Yearly\)|Scheduled|Deletes hermes\_usage\_metrics records older than approximately 3 months where roll\_up\_type = 1.|
|Hermes Topics Util|Scheduled|Synchronizes topic metadata across the cluster and verifies that all nodes have consistent topic configurations.|

**Parent Topic:**[Hermes Messaging Service reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/hermes-messaging-service-reference.md)

**Related topics**  


[Hermes Messaging Service components]()

[Hermes Messaging Service security model]()

[Hermes Messaging Service system properties]()

[Hermes Messaging Service roles]()

[Hermes Messaging Service domain separation]()

