---
title: RabbitMQ default checks and policies
description: Agent Client Collector provides the following default checks and policies for RabbitMQ health monitoring. You must perform RabbitMQ discovery before executing the checks. RabbitMQ checks are available only in a Windows environment.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# RabbitMQ default checks and policies

Agent Client Collector provides the following default checks and policies for RabbitMQ health monitoring. You must perform RabbitMQ discovery before executing the checks. RabbitMQ checks are available only in a Windows environment.

<table id="table_lsp_hsb_3tb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Event

</td><td>

check-rabbitmq-alive

</td><td>

Verifies whether the RabbitMQ server is alive, using the REST API. If the server is down, an alert triggers.

</td><td>

`check-rabbitmq-alive.rb --host {{.labels.params_host}} --port {{.labels.params_port}} -v {{.labels.params_vhost}}`

</td></tr><tr><td>

Event

</td><td>

check-rabbitmq-cluster-health

</td><td>

Verifies whether the RabbitMQ server's cluster nodes are running. If the nodes are down, an alert triggers.

</td><td>

`check-rabbitmq-cluster-health.rb --host {{.labels.params_host}} --port {{.labels.params_port}}`

</td></tr><tr><td>

Event

</td><td>

check-rabbitmq-consumers

</td><td>

Verifies the number of consumers on the RabbitMQ server and triggers an alert based on the configured threshold.

</td><td>

`check-rabbitmq-consumers.rb {{if .labels.params_warn}} --warn {{.labels.params_warn}} {{end}} {{if .labels.params_critical}} --critical {{.labels.params_critical}} {{end}} --host {{.labels.params_host}} --port {{.labels.params_port}}`

</td></tr><tr><td>

Event

</td><td>

check-rabbitmq-messages

</td><td>

Verifies the total number of messages queued on the RabbitMQ server and triggers an alert based on the threshold.

</td><td>

`check-rabbitmq-messages.rb --critical {{.labels.params_critical}} --port {{.labels.params_port}} --warn {{.labels.params_warn}} --host {{.labels.params_host}}`

</td></tr><tr><td>

Event

</td><td>

check-rabbitmq-network-partitions

</td><td>

Verifies whether the RabbitMQ network partition has occurred and triggers an alert based on the threshold.

</td><td>

check-rabbitmq-network-partitions.rb --host \{\{.labels.params\_host\}\} --port \{\{.labels.params\_port\}\}

</td></tr><tr><td>

Event

</td><td>

check-rabbitmq-node-health

</td><td>

Verifies whether the RabbitMQ server node is in a running state.

</td><td>

```
check-rabbitmq-node-health.rb --host {{.labels.params_host}} {{if .labels.params_watchalarms}} --alarms {{.labels.params_watchalarms}} {{end}} {{if .labels.params_socketwarn}} --swarn {{.labels.params_socketwarn}} {{end}} {{if .labels.params_memcrit}} --mcrit {{.labels.params_memcrit}} {{end}} {{if .labels.params_fdcrit}} --fcrit {{.labels.params_fdcrit}} {{end}} {{if .labels.params_socketcrit}} --scrit {{.labels.params_socketcrit}} {{end}} --port {{.labels.params_port}} {{if .labels.params_memwarn}} --mwarn {{.labels.params_memwarn}} {{end}} {{if .labels.params_fdwarn}} --fwarn {{.labels.params_fdwarn}} {{end}}
```

</td></tr><tr><td>

Event

</td><td>

check-rabbitmq-node-usage

</td><td>

Checks and displays usage of the RabbitMQ server node.

</td><td>

```
check-rabbitmq-node-usage.rb {{if .labels.params_procwarn}} --pwarn {{.labels.params_procwarn}} {{end}} --port {{.labels.params_port}} {{if .labels.params_socketwarn}} --swarn {{.labels.params_socketwarn}} {{end}} --type {{.labels.params_type}} {{if .labels.params_diskcrit}} --dcrit {{.labels.params_diskcrit}} {{end}} {{if .labels.params_fdcrit}} --fcrit {{.labels.params_fdcrit}} {{end}} {{if .labels.params_proccrit}} --pcrit {{.labels.params_proccrit}} {{end}} {{if .labels.params_diskwarn}} --dwarn {{.labels.params_diskwarn}} {{end}} {{if .labels.params_socketcrit}} --scrit {{.labels.params_socketcrit}} {{end}} --host {{.labels.params_host}} {{if .labels.params_memcrit}} --mcrit {{.labels.params_memcrit}} {{end}} {{if .labels.params_fdwarn}} --fwarn {{.labels.params_fdwarn}} {{end}} {{if .labels.params_memwarn}} mwarn {{.labels.params_memwarn}} {{end}}
```

</td></tr><tr><td>

Event

</td><td>

check-rabbitmq-queue-drain-time

</td><td>

Verifies the time it will take for each queue on the RabbitMQ server to drain, based on the current message exit rate.For example, if a queue has 1,000 messages in it but only 1 message exits per second, an alert generates because the default critical level of 360 seconds has been exceeded.

</td><td>

`check-rabbitmq-queue-drain-time.rb --host {{.labels.params_host}} --port {{.labels.params_port}} --warn {{.labels.params_warn}} --critical {{.labels.params_critical}}`

</td></tr><tr><td>

Event

</td><td>

check-rabbitmq-queues-synchronised

</td><td>

Verifies that all mirrored queues with secondary queues are synchronised.

</td><td>

`check-rabbitmq-queues-synchronised.rb --host {{.labels.params_host}} --port {{.labels.params_port}}`

</td></tr><tr><td>

Event

</td><td>

check-rabbitmq-stomp-alive

</td><td>

Verifies whether the RabbitMQ server is alive and responding to STOMP.

</td><td>

`check-rabbitmq-stomp-alive.rb --host {{.labels.params_host}} --queue {{.labels.params_queue}} --port {{.labels.params_port}}`

</td></tr></tbody>
</table>|Type|Check|Description|Command|
|----|-----|-----------|-------|
|Metric|metrics-rabbitmq-overview|Provides RabbitMQ overview statistics.|`metrics-rabbitmq-overview.rb --port {{.labels.params_port}} --host {{.labels.params_host}}`|
|Metric|metrics-rabbitmq-queue|Provides RabbitMQ metrics per queue.|`metrics-rabbitmq-queue.rb --port {{.labels.params_port}} --host {{.labels.params_host}} {{if .labels.params_vhost}} --vhost {{.labels.params_vhost}} {{end}}`|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

