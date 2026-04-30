---
title: Agent Client Collector Framework default checks
description: Agent Client Collector Framework provides default checks with the base system.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector Framework default checks

Agent Client Collector Framework provides default checks with the base system.

## Checks

The following table lists the default checks that come with the Agent Client Collector Framework base system.

<table id="table_r1l_p43_jpb"><thead><tr><th>

Type

</th><th>

Name

</th><th>

Description

</th><th>

Command

</th></tr></thead><tbody><tr><td>

Restart

</td><td>

restart

</td><td>

Restarts the agent.Check is active by default

</td><td>

Restart agent

</td></tr><tr><td>

Discovery

</td><td>

check-discovery-basic

</td><td>

Performs basic discovery of the agent's host to discover:-   Host CI, including IP address, serial number, and hostname.
-   Running processes \(cmdb\_running\_process\) of the host
-   TCP ports \(cmdb\_tcp\)

 The check is performed by default every 12 hours \(43200 seconds\), and times out after 600 seconds of inactivity.

 Plugins: osquery, acc-f-commons, acc-f-modules

</td><td>

endpoint\_discovery.rb

</td></tr></tbody>
</table>**Note:** The **check-read-log** and **config-file-reader** checks are for internal use only.

**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

