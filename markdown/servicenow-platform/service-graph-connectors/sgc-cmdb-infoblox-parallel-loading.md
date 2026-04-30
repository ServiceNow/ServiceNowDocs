---
title: Handling parallel data loading in Service Graph Connector for Infoblox
description: Parallel data loading in the Service Graph Connector for Infoblox optimizes performance.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-03"
reading_time_minutes: 1
breadcrumb: [Infoblox, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Handling parallel data loading in Service Graph Connector for Infoblox

Parallel data loading in the Service Graph Connector for Infoblox optimizes performance.

Parallel data loading is supported in Service Graph Connector for Infoblox version 1.3.0 and later. Parallel data loading can be enabled for the SG-Infoblox Network and SG-Infoblox IP Address data sources by setting the partition size in the **sn\_infoblox\_integ.parallel\_loading\_partition\_size** system property. This system property determines the maximum number of networks that each partition processes. The maximum value that you can set for the partition size is `150`.

-   For the SG-Infoblox Network data source, the partition size is based on network views.
-   For the SG-Infoblox IP Address data source, the partition size is based on the number of networks.

## Related content

[Service Graph Connector for Infoblox properties](../reference/cmdb-sgc-infoblox-props.md)

