---
title: Scheduled jobs included with MID Server distributed cluster
description: The following MID Server scheduled job is included with the MID Server Distributed cluster type.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring reference, Agent Client Collector, IT Operations Management]
---

# Scheduled jobs included with MID Server distributed cluster

The following MID Server scheduled job is included with the MID Server Distributed cluster type.

<table id="table_obt_4nq_4bb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Validate MID distributed cluster

</td><td>

Validates status of the cluster node for each MID Server in the cluster. For a MID Server that is down and its status is not stopped, updates the node status to stopped.Also, validates overall status of the cluster. During this validation, the job stops the cluster if there are multiple sub-clusters in a single cluster.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring reference](../../agent-client-collector/reference/acc-monitoring-reference.md)

