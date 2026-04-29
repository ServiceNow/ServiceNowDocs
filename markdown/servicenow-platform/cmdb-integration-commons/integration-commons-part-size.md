---
title: Partition size computation for parallel loading in Integration Commons for CMDB
description: Integration Commons for CMDB supports computed partition size for the parallel loading framework, if supported in a Service Graph Connector.
locale: en-US
release: australia
product: CMDB Integration Commons
classification: cmdb-integration-commons
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration Commons for CMDB, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Partition size computation for parallel loading in Integration Commons for CMDB

Integration Commons for CMDB supports computed partition size for the parallel loading framework, if supported in a Service Graph Connector.

The parallel loading feature of ServiceNow AI Platform, executes data load using multiple threads. The partition size for a data source is computed by the Integration Commons for CMDB application used by the parallel loading feature. This partition size confirms that the workload is evenly distributed among the available threads. By balancing the data load, a data source within a Service Graph Connector can manage data loading uniformly across the available nodes, reducing processing time and improving overall efficiency. This approach promotes efficient data loading, minimizes latency, and optimizes the performance of data sources.

The partition size computation for the parallel loading feature within the Integration Commons for CMDB application is based on the following calculations:

-   [Partition size calculation](integration-commons-part-size.md#section_gst_h2g_ccc)
-   [Parallel jobs calculation](integration-commons-part-size.md#section_zfw_z2g_ccc)

## Partition size calculation

The partition size for parallel loading in a data source is determined by both the number of active primary nodes on your ServiceNow instance and the total volume of data to be loaded by the data source using the following formula:

```
Partition size = Total data volume / (10% * Active primary nodes)
```

For example, if there are `4` active primary nodes and the data volume to be loaded is `1000` units, the partition size is calculated as:

```
Partition size = 1000 / (10% * 4) = 1000 / 0.4 = 25
```

## Parallel jobs calculation

Parallel jobs enable distributing the workload evenly across multiple jobs, reducing the data loading time and improving the efficiency of data retrieval. The calculation of the number of parallel jobs created for a partition is based on the following formula:

```
Number of parallel jobs = Total data volume/Partition size

```

In the earlier example, where the total data volume is `1000` units and the partition size is `25`, the number of parallel jobs created is calculated as:

```
Number of parallel jobs = 1000/25 = 40
```

