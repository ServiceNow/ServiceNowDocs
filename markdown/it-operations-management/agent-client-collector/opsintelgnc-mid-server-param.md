---
title: Parameters of MID Server distributed cluster
description: The following MID Server parameters support the MID Server Distributed cluster type.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Parameters of MID Server distributed cluster

The following MID Server parameters support the MID Server Distributed cluster type.

You can access these parameters in the **Configuration Parameters** related list of a MID Server. To add and set any of these parameter, see [Add a MID Server parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=australia&pubname=australia-servicenow-platform&section=t_SetMIDServerParameters&ft:locale=en-US).

<table id="table_psp_b3r_mbb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mid.distributed.cluster.striped.threadpool.size

</td><td>

Size of striped threadpool in MID Server distributed cluster.-   **Type**: integer
-   **Default value**: Number of cores on the virtual machine or server.

</td></tr><tr><td>

mid.distributed.cluster.log.level

</td><td>

Logging level for MID Server distributed cluster, which can help troubleshooting. However, logging impacts the performance of Metric Intelligence.

 An empty value designates no logging.

 -   **Type**: integer
-   **Default value**: none
-   **Other possible values**: info, debug, trace

</td></tr><tr><td>

mid.distributed.cluster.global.timeout

</td><td>

Global timeout in seconds for MID Server distributed cluster.-   **Type**: integer
-   **Default value**: 180
-   **Other possible values**:
    -   **Minimum value**: 60 \(not enforced\)
    -   **Maximum value**: 300 \(not enforced\)

</td></tr><tr><td>

mid.distributed.cluster.node.max.off.heap.memory

</td><td>

The amount of off heap memory used by Metric Intelligence to process data series per minute. The default 4 GB of space is the amount of off heap memory needed for processing 800,000 data series per minute. Adjust this value proportionally to the amount of actual data series. For example, to process 400,000 data series per minute, you can change the value to 2048.

 -   **Type**: integer
-   **Default value**: 4096

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring reference](../../agent-client-collector/reference/acc-monitoring-reference.md)

