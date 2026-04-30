---
title: RabbitMQ metrics
description: The following table lists the metrics that are gathered as output from RabbitMQ checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC-M default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector, IT Operations Management]
---

# RabbitMQ metrics

The following table lists the metrics that are gathered as output from RabbitMQ checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|rabbitmq.queue\_totals.messages.count| |count|Provides metrics on the total number of messages \(ready plus unacknowledged\).|
|rabbitmq.queue\_totals.messages.rate \(featured metric\)| |rate / sec|Provides metrics on the total number of messages \(ready plus unacknowledged\)|
|rabbitmq.queue\_totals.messages\_ready.count| |count|Provides metrics on the number of messages ready for delivery.|
|rabbitmq.queue\_totals.messages\_ready.rate| |rate / sec|Provides metrics on the number of messages ready for delivery.|
|rabbitmq.queue\_totals.messages\_unacknowledged.count| |count|Provides metrics on the number of unacknowledged messages.|
|rabbitmq.queue\_totals.messages\_unacknowledged.rate| |rate / sec|Provides metrics on the number of unacknowledged messages.|
|rabbitmq.message\_stats.deliver\_get.count| |count|Provides metrics on messages recently delivered to consumers.|
|rabbitmq.message\_stats.deliver\_get.rate \(featured metric\)| |rate / sec|Provides metrics on messages recently delivered to consumers.|
|rabbitmq.message\_stats.deliver\_no\_ack.count| |count|Provides metrics on unacknowledged messages recently delivered to consumers.|
|rabbitmq.message\_stats.deliver\_no\_ack.rate| |rate / sec|Provides metrics on unacknowledged messages recently delivered to consumers.|
|rabbitmq.message\_stats.publish.count| |count|Provides metrics on recently published messages.|
|rabbitmq.message\_stats.publish.rate| |rate / sec|Provides metrics on the recently published messages.|
|rabbitmq.object\_totals.channels.count| |count|Provides metrics on the total number of channels.|
|rabbitmq.object\_totals.connections.count \(featured metric\)| |count|Provides metrics on the total number of connections.|
|rabbitmq.object\_totals.consumers.count \(featured metric\)| |count|Provides metrics on the total number of consumers.|
|rabbitmq.object\_totals.exchanges.count| |count|Provides metrics on the total number of exchanges.|
|rabbitmq.object\_totals.queues.count \(featured metric\)| |count|Provides metrics on the total number of queues.|

| | | | |
|---|---|---|---|
|rabbitmq.queue.\{\{QueueName\}\}.avg\_egress\_rate \(featured metric\)|Queue Name|count|Provides queue specific metrics on the rate at which unacknowledged message records enter RAM for the given queue.|
|rabbitmq.queue.\{\{QueueName\}\}.consumers|Queue Name|count|Provides queue specific metrics on the total consumers for the given queue.|
|rabbitmq.queue.\{\{QueueName\}\}.messages|Queue Name|count|Provides queue specific metrics on the total messages in the given queue.|
|rabbitmq.queue.\{\{QueueName\}\}.drain\_time|Queue Name|count|Provides queue specific metrics on the message drain time for the given queue.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

