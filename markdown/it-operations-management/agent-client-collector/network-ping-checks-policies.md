---
title: Network ping default checks and policies
description: Agent Client Collector provides the following default checks and policies for Network ping monitoring. Policies and checks are available for both Windows and Linux.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Network ping default checks and policies

Agent Client Collector provides the following default checks and policies for Network ping monitoring. Policies and checks are available for both Windows and Linux.

<table id="table_gqp_y3h_mxb"><thead><tr><th>

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

util.metrics-ping

</td><td>

Runs on the ip address discovered in the ServiceNow instance. Pings the host and collects metrics.The monitored CI type is **cmdb\_ci\_hardware** and is bound to the relevant server.

A proxy agent is required.

</td><td>

metrics-ping.rb \(options\)`c --count COUNT Ping count`

`-h Host to ping`

`-t --timeout TIMEOUT Timeout`

Example: ./metrics-ping.rb -h 10.196.121.11

</td><td>

 

</td><td>

```
c7inc0047383.ping.packets_transmitted 5 1675923886
            c7inc0047383.ping.packets_received 5 1675923886
            c7inc0047383.ping.packet_loss 0 1675923886
            c7inc0047383.ping.time 3999 1675923886
            c7inc0047383.ping.min 0.253 1675923886
            c7inc0047383.ping.avg 0.292 1675923886
            c7inc0047383.ping.max 0.318 1675923886
            c7inc0047383.ping.mdev 0.032 1675923886

```

 **Note:** Windows does not support the **ping.time** and **ping.mdev** metrics.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

