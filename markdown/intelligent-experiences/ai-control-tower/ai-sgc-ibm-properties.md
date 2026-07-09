---
title: AI Service Graph Connector for IBM properties
description: AI Service Graph Connector for IBM properties control the behavior of the connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/ai-sgc-ibm-properties.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [IBM, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AI Service Graph Connector for IBM properties

AI Service Graph Connector for IBM properties control the behavior of the connector.

## Connection properties

These connection properties are available for AI Service Graph Connector for IBM.

<table id="table_conn_props_datadog"><thead><tr><th>

Property

</th><th>

Service

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IsRuntimeSelected

</td><td>

IBM watsonx Runtime

</td><td>

Enable IBM watsonx Runtime discovery for the connection.

</td></tr><tr><td>

Runtime\_Spaces

</td><td>

IBM watsonx Runtime

</td><td>

Optional: Specify the JSON map of IBM Cloud regions to deployment space IDs.If no value is specified, all accessible spaces in all regions are discovered.

</td></tr><tr><td>

IsOrchestrateSelected

</td><td>

IBM watsonx Orchestrate

</td><td>

Enable IBM watsonx Orchestrate discovery for the connection.

</td></tr><tr><td>

Orchestrate\_Instances

</td><td>

IBM watsonx Orchestrate

</td><td>

Optional: Specify the comma-separated list of IBM watsonx Orchestrate instance GUIDs \(tenant IDs\) to be discovered.If no value is specified, all accessible instances are discovered.

</td></tr><tr><td>

SourceSystem

</td><td>

IBM watsonx RuntimeIBM watsonx Orchestrate

</td><td>

Identifies the source system for the connection. The value is set automatically by the connector to  `IBM WatsonX AI`. **Note:** This property is system-managed and can't be modified manually.

</td></tr></tbody>
</table>