---
title: Azure metrics script
description: When creating a new policy for Azure cloud metrics, create a .json script to determine the metrics to be monitored. The format for the script appears below, followed by a table explaining the script contents.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Azure metrics script

When creating a new policy for Azure cloud metrics, create a .json script to determine the metrics to be monitored. The format for the script appears below, followed by a table explaining the script contents.

```
{
  "namespace": "Microsoft.Network/loadBalancers",
  "metrics": [
          "AllocatedSnatPorts",
          "ByteCount",
          "DipAvailability",
          "PacketCount",
          "SnatConnectionCount",
          "SYNCount",
          "UsedSnatPorts",
          "VipAvailability"
  ],
  "time_grain": "PT1M"
}
```

Resources and their metrics are retrievable from the [Supported metrics for Azure resources](https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-metrics/microsoft-compute-virtualmachines-metrics) page.

<table id="table_v1g_1jw_mzb"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

namespace

</td><td>

The name of the resource being monitored.

</td></tr><tr><td>

metrics

</td><td>

The metrics being retrieved from the monitored resource.

</td></tr><tr><td>

time\_grain

</td><td>

The granularity of how often metrics are to be collected. Possible values are:-   PT1M: Metric values are collected every minute.
-   PT5M: Metric values are collected every 5 minutes.
-   PT15M: Metric values are collected every 15 minutes.
-   PT30M: Metric values are collected every 30 minutes.
-   PT1H: Metric values are collected every hour.
-   PT1D: Metric values are collected daily.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring reference](acc-monitoring-reference.md)

