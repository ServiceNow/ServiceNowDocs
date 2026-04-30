---
title: Apache Kafka metrics
description: The following table lists the metrics that are gathered as output from Kafka checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC-M default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector, IT Operations Management]
---

# Apache Kafka metrics

The following table lists the metrics that are gathered as output from Kafka checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|Kafka.Broker.RequestMetrics.TotalTimeMs.FetchConsumer.Mean \(featured metric\)| | |Total time \(in ms\) to serve the Consumer request.|
|Kafka.Broker.RequestMetrics.TotalTimeMs.FetchFollower.Mean \(featured metric\)| | |Total time \(in ms\) to serve the Follower request.|
|Kafka.Broker.RequestMetrics.TotalTimeMs.Produce.Mean \(featured metric\)| | |Total time \(in ms\) to serve the Producer request.|
|Kafka.Broker.BrokerTopicMetrics.BytesOutPerSec.OneMinuteRate \(featured metric\)| | |Aggregate outgoing byte rate.|
|Kafka.Broker.BrokerTopicMetrics.BytesInPerSec.OneMinuteRate \(featured metric\)| | |Aggregate incoming byte rate.|
|Kafka.Broker.ReplicaManager.UnderReplicatedPartitions.Value| | |Number of unreplicated partitions.|
|Kafka.Broker.ReplicaManager.IsrExpandsPerSec.OneMinuteRate| | |Rate at which the pool of in-sync replicas \(ISRs\) shrinks.|
|Kafka.Broker.ReplicaManager.IsrShrinksPerSec.OneMinuteRate| | |Rate at which the pool of in-sync replicas \(ISRs\) shrinks.|
|Kafka.Broker.KafkaController.ActiveControllerCount.Value \(featured metric\)| | |Number of active controllers in cluster.|
|Kafka.Broker.KafkaController.OfflinePartitionsCount.Value| | |Number of offline partitions.|
|Kafka.Broker.ControllerStats.LeaderElectionRateAndTimeMs.OneMinuteRate \(featured metric\)| | |Leader election rate and latency.|
|Kafka.Broker.ControllerStats.UncleanLeaderElectionsPerSec.OneMinuteRate| | |Number of unclean elections per second.|
|Kafka.Broker.DelayedOperationPurgatory.PurgatorySize.Fetch.Value| | |Number of requests waiting in fetch purgatory.|
|Kafka.Broker.DelayedOperationPurgatory.PurgatorySize.Produce.Value| | |Number of requests waiting in producer purgatory.|
|Kafka.Broker.RequestMetrics.RequestsPerSec.Produce.OneMinuteRate \(featured metric\)| | |Number of producer requests per second.|
|Kafka.Broker.RequestMetrics.RequestsPerSec.FetchConsumer.OneMinuteRate \(featured metric\)| | |Number of consumer requests per second.|
|Kafka.Broker.RequestMetrics.RequestsPerSec.FetchFollower.OneMinuteRate \(featured metric\)| | |Number of follower requests per second.|

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|Kafka.Zookeeper.outstanding\_requests \(featured metric\)| | |Number of requests queued.|
|Kafka.Zookeeper.avg\_latency \(featured metric\)| | |Average amount of time it takes to respond to a client request \(in ms\).|
|Kafka.Zookeeper.num\_alive\_connections \(featured metric\)| | |Number of clients connected to ZooKeeper.|
|Kafka.Zookeeper.open\_file\_descriptor\_count| | |Number of file descriptors in use.|
|Kafka.Zookeeper.pending\_syncs| | |Number of pending syncs from followers.|
|Kafka.Zookeeper.followers| | |Number of active followers.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

