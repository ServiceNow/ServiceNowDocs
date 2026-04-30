---
title: Cassandra default checks and policies
description: Agent Client Collector provides the following policies for Cassandra health monitoring. Policies come with the checks specified in the indicated table. Policies and checks are available for Linux only.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC-M default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector, IT Operations Management]
---

# Cassandra default checks and policies

Agent Client Collector provides the following policies for Cassandra health monitoring. Policies come with the checks specified in the indicated table. Policies and checks are available for Linux only.

<table id="table_mqy_xzd_2tb"><thead><tr><th>

Check

</th><th>

Description

</th><th>

Usage

</th><th>

Command

</th><th>

Output

</th></tr></thead><tbody><tr><td>

app.cassandra.metrics-cassandra

</td><td>

Returns metrics of a Cassandra database.

</td><td>

`metrics-cassandra-graphite.rb`

 Options:

-   **-h host**

Hostname where the Cassandra database is running

-   **-P port**

Cassandra JMX port


</td><td>

`metrics-cassandra-graphite.rb --cfstats -P {{.labels.params_port}} -h {{.labels.params_host}}`

</td><td>

`<host>.cassandra.load 132270.08 1645107221`

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

