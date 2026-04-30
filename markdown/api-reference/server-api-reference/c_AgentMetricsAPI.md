---
title: AgentMetrics - Global
description: The AgentMetrics script include provides methods to process inbound MID Server metrics.Creates an instance of AgentMetrics.Handles counter metrics from the agent by putting them into an array that can be used to update the ECC Agent Counter Metric table \(ecc\_agent\_counter\_metric\).Updates the memory metrics for the given agent.Handles metric information from a remote glide record by putting it into an array.Handles scalar values from the agent by putting them into an array.Updates the specified metrics table with the new metric information.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# AgentMetrics- Global

The AgentMetrics script include provides methods to process inbound MID Server metrics.

This script include updates the following tables:

-   ECC Agent Counter Metric \[ecc\_agent\_counter\_metric\]
-   ECC Agent Memory Metric \[ecc\_agent\_memory\_metric\]
-   ECC Agent RGR Metric \[ecc\_agent\_rgr\_metric\]
-   ECC Agent Scalar Metric \[ecc\_agent\_scalar\_metric\]

Use these methods in server scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## AgentMetrics - AgentMetrics\(\)

Creates an instance of AgentMetrics.

|Name|Type|Description|
|----|----|-----------|
|None| | |

This example shows how to use AgentMetrics\(\) to instantiate an AgentMetrics object.

```
var amtc = new AgentMetrics();
amtc.handleMemory('memory', 'server_name', '1098888bbb9483abcd89981ffaeff');
amtc.updateMetric('ecc_agent_memory_metric', 'm_values', 'memory', '1098888bbb9483abcd89981ffaeff');
```

## AgentMetrics - handleCounter\(String metric, String name, String midId\)

Handles counter metrics from the agent by putting them into an array that can be used to update the ECC Agent Counter Metric table \(ecc\_agent\_counter\_metric\).

|Name|Type|Description|
|----|----|-----------|
|metric|String|The counter object from the agent|
|name|String|The device name|
|midId|String|The MID server sys\_id|

|Type|Description|
|----|-----------|
|void| |

```
var amtc = new AgentMetrics();
amtc.handleCounter('count', 'server_name', '1098888bbb9483abcd89981ffaeff');
```

## AgentMetrics - handleMemory\(String metric, String name, String midId\)

Updates the memory metrics for the given agent.

|Name|Type|Description|
|----|----|-----------|
|metric|String|The memory object from the agent|
|name|String|The device name|
|midId|String|The MID server sys\_id|

|Type|Description|
|----|-----------|
|void| |

```
var amtc = new AgentMetrics();
amtc.handleMemory('mem_obj', 'server_name', '1098888bbb9483abcd89981ffaeff');
```

## AgentMetrics - handleRGR\(String metric, String name, String midId\)

Handles metric information from a remote glide record by putting it into an array.

|Name|Type|Description|
|----|----|-----------|
|metric|String|The remote object from the agent|
|name|String|The device name|
|midId|String|The MID server sys\_id|

|Type|Description|
|----|-----------|
|void| |

```
var amtc = new AgentMetrics();
amtc.handleRGR('remote_obj', 'server_name', '1098888bbb9483abcd89981ffaeff');
```

## AgentMetrics - handleScalar\(String metric, String name, String midId\)

Handles scalar values from the agent by putting them into an array.

|Name|Type|Description|
|----|----|-----------|
|metric|String|The counter object from the agent|
|name|String|The device name|
|midId|String|The MID server sys\_id|

|Type|Description|
|----|-----------|
|void| |

```
var amtc = new AgentMetrics();
amtc.handleScalar('scalar', 'server_name', '1098888bbb9483abcd89981ffaeff');
```

## AgentMetrics - updateMetric\(String tableName, String values, String metric, String midID\)

Updates the specified metrics table with the new metric information.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The metrics table to update|
|values|String|The object containing the values to add to the table|
|metric|String|The metric type to add to the table|
|midID|String|The MID server sys\_id|

|Type|Description|
|----|-----------|
|void| |

```
var amtc = new AgentMetrics();
amtc.handleMemory('memory', 'server_name', '1098888bbb9483abcd89981ffaeff');
amtc.updateMetric('ecc_agent_memory_metric', 'm_values', 'memory', '1098888bbb9483abcd89981ffaeff');
```

