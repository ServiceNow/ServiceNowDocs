---
title: Alerts in Instance Observer
description: ServiceNow Instance Observer provides a comprehensive set of alerts designed to monitor platform health, performance, and user experience. These alerts are categorized for easy consumption and actionability.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Alerts in Instance Observer]
breadcrumb: [Overview of Instance Observer, Platform Health, Using Impact, Impact]
---

# Alerts in Instance Observer

ServiceNow Instance Observer provides a comprehensive set of alerts designed to monitor platform health, performance, and user experience. These alerts are categorized for easy consumption and actionability.

-   **Transactions**

    Monitors application transactions for anomalies, spikes, or degradations in performance such as:

    -   Transaction Decrease: Detects a drop in total transaction volume
    -   Transaction Decrease Node: Identifies transaction volume drop per node
    -   Transaction Increase: Flags unexpected transaction surges
    -   Transaction Increase Node: Highlights node-level transaction spikes
    -   Response Time: Triggers when system-wide response time increases
    -   Response Time Node: Flags nodes with degraded response times
    -   Database Response Time: Monitors database-level latency impacting transactions
    -   Slow Queries Per Second: Identifies the volume of slow database queries affecting responsiveness
-   **Node health \(CPU, memory, or garbage collection\)**

    Tracks node infrastructure health to avoid bottlenecks or failures:

    -   Node CPU time: High CPU usage alert for a node
    -   Node memory: Monitors memory consumption patterns
    -   Node garbage collection time: Tracks JVM GC delays
    -   Load balancer container CPU utilization: Flags CPU overload on LB containers
    -   Load balancer container memory utilization: Detects memory exhaustion on LB containers
-   **Database performance and health**

    Covers critical database indicators to verify query health and data reliability:

    -   Database host health CPU: High CPU on primary DB host
    -   Shards host health CPU: Resource issues on shard hosts
    -   Read replica host health \(CPU\): Read-replica CPU anomalies
    -   Standby replication lag: Lag in standby DB replication
    -   InnoDB row lock: Frequency of row lock waits
    -   Primary database growth: Flags abnormal growth in primary DB
    -   Database table growth: Specific table-level growth indicators
-   **Inbound and outbound email**

    Promotes timely delivery and ingestion of email-based communications:

    -   Outbound email: Delays or failures in outbound email processing
    -   Inbound email: Issues in ingesting incoming emails
-   **Scheduler and job execution**

    Helps detect issues in the job execution life cycle:

    -   Scheduler stuck: Scheduler not progressing or blocked
    -   Long-running jobs: Jobs exceeding typical run time
    -   Specific long-running jobs: Custom job monitoring
    -   Thread running: Threads running unusually long or in high volume
-   **Session and user activity**

    Tracks user login behavior across instance and nodes:

    -   User session logged in – Instance: Log in activity across instance
    -   User session logged in – Node: Node-wise session metrics
-   **Event queue and semaphore management**

    Critical for debugging platform event handling and job execution throttling:

    -   Default semaphore mean: Semaphore wait time trends
    -   Default semaphore QDepth: Depth of queued semaphore requests
    -   Integrated semaphore: Monitors integrated semaphore contention
    -   Event queue check: Tracks backlog in event queues
    -   Specific queue for events: Custom event queue monitoring
    -   High priority event queue: Monitors mission-critical event queues
    -   ECC queue: External communication channel backlog alerts
-   **Asynchronous Messaging Bus \(AMB\)**

    Internal messaging bus observability for real-time app behavior:

    -   AMB send queue depth: Size of outgoing message queue
    -   AMB send in use: Utilization of AMB sending capacity
-   **Historical or list data volume**

    Monitors growth of historical or list data that can impact performance:

    History list length: Flags excessive record count in history tables.

-   **Application host health**

    Monitors health at the application layer:

    Application host health CPU: Application-tier CPU overload alerts.

-   **AI/ML or intelligent alerting**

    Includes alerts generated via AI/ML-based behavior analysis:

    Auriga Intelligent: AI-driven anomaly or pattern detection alerts.


