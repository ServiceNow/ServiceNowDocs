---
title: Agent Client Collector CPU protection thresholds
description: When an agent meets the configured thresholds specified in the agent's acc.yml file, it enters CPU protection mode, either for an individual check or for all checks. Agents in CPU protection mode appear in the agent logs with the syntax Agent Protection.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector CPU protection thresholds

When an agent meets the configured thresholds specified in the agent's `acc.yml` file, it enters CPU protection mode, either for an individual check or for all checks. Agents in CPU protection mode appear in the agent logs with the syntax `Agent Protection`.

<table id="table_nmc_yf3_zlb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**agent\_cpu\_threshold\_disabled**

</td><td>

To prevent the agent from shutting itself off when CPU memory reaches a certain threshold, set value to **True**.Default=False

</td></tr><tr><td>

**cpu\_percentage\_limit**

</td><td>

The percentage of the agent's CPU usage that sends the agent into CPU protection mode. Default=5%

</td></tr><tr><td>

**cpu\_protection\_behavior**

</td><td>

Assign **individual** for the system to disable only the individual check that passed the **cpu\_percentage\_limit** value. If multiple checks crossed the threshold, the check with the highest CPU is disabled.Assign **all** to disable all checks and pause data collection.

Possible values: all, individual

Default: all

</td></tr><tr><td>

**repeated\_high\_cpu\_num**

</td><td>

The number of consecutive times CPU consumption exceeds the **cpu\_percentage\_limit** for the agent to enter CPU protection mode.Default=3

</td></tr><tr><td>

**monitor\_interval\_sec**

</td><td>

Indicates the frequency, in seconds, that the agent monitor runs to check if the **cpu\_percentage\_limit** is exceeded.Default=60

</td></tr><tr><td>

**proxy\_cpu\_percentage\_limit**

</td><td>

The percentage of the agent's CPU usage when the agent is running proxy checks too frequently, that sends the agent into CPU protection mode.Default=80

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

