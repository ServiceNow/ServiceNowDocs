---
title: Standardized JSON common data set to support all service graph connectors
description: Use the TSOM architecture to support standardized Service Graph Connectors using a unified schema and reusable ETL logic. This reduces onboarding time for new connectors and simplifies integration with CMDB.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Configure Telecom Discovery Builder, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Standardized JSON common data set to support all service graph connectors

Use the TSOM architecture to support standardized Service Graph Connectors using a unified schema and reusable ETL logic. This reduces onboarding time for new connectors and simplifies integration with CMDB.

## 1. Define the common JSON Schema

Standardize the output of all service graph connectors to align with a single JSON format that conforms to the TNI schema.

Ensure the following points:

1.  Implement conversion logic in the collector or adaptor to output data in the common schema.
2.  Ensure:
    -   Slot-on-slot or card-on-card hierarchies are excluded.
    -   Logical interfaces are clearly marked with `virtual=true`.
    -   Equipment types align to model-class mappings.

**Note:** The schema should support runtime adaptability to TNI changes if available.

The following is the JSON schema common data set that supports all TSOM service graph connectors:

```
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "Telco Generic Schema",
  "version": "2.0.1",
  "oneOf": [
    {
      "type": "object",
      "properties": {
        "logical_composites": {
          "type": "array",
          "items": {
            "$ref": "#/$defs/logical_composite"
          }
        }
      },
      "required": [
        "logical_composites"
      ],
      "additionalProperties": false
    },
    {
      "type": "object",
      "properties": {
        "devices": {
          "type": "array",
          "items": {
            "$ref": "#/$defs/device"
          }
        }
      },
      "required": [
        "devices"
      ],
      "additionalProperties": false
    },
    {
      "type": "object",
      "properties": {
        "logical_connections": {
          "type": "array",
          "items": {
            "$ref": "#/$defs/logical_connection"
          }
        }
      },
      "required": [
        "logical_connections"
      ],
      "additionalProperties": false
    },
    {
      "type": "object",
      "properties": {
        "port_relations": {
          "type": "array",
          "items": {
            "$ref": "#/$defs/port_relation"
          }
        }
      },
      "required": [
        "port_relations"
      ],
      "additionalProperties": false
    },
    {
      "type": "object",
      "properties": {
        "logical_connection_relations": {
          "type": "array",
          "items": {
            "$ref": "#/$defs/logical_connection_relation"
          }
        }
      },
      "required": [
        "logical_connection_relations"
      ],
      "additionalProperties": false
    },
    {
      "type": "object",
      "properties": {
        "numbers": {
          "type": "array",
          "items": {
            "$ref": "#/$defs/number"
          }
        }
      },
      "required": [
        "numbers"
      ],
      "additionalProperties": false
    },
    {
      "type": "object",
      "properties": {
        "topologies": {
          "type": "array",
          "items": {
            "$ref": "#/$defs/network_topology"
          }
        }
      },
      "required": [
        "topologies"
      ],
      "additionalProperties": false
    },
    {
      "type": "object",
      "properties": {
        "topology_relations": {
          "type": "array",
          "items": {
            "$ref": "#/$defs/network_topology_relation"
          }
        }
      },
      "required": [
        "topology_relations"
      ],
      "additionalProperties": false
    }
  ],
  "$defs": {
    "keyRef": {
      "type": "object",
      "properties": { "key": { "type": "string" }
      },
      "required": [ "key" ],
      "additionalProperties": false
    },
    "optionalKeyRef": { "type": [ "object", "null" ],
      "properties": {
        "key": { "type": "string" }
      },
      "additionalProperties": false
    },
    "value": {
      "type": "object",
      "properties": {
        "from": { "type": [ "integer" ], "default": 0, "minimum": 0 },
        "to": { "type": [ "integer" ], "default": 0, "minimum": 0 }
      },
      "required": [ "from", "to" ],
      "additionalProperties": false
    },
    "logical_composite": {
      "type": "object",
      "properties": {
        "class": { "type": "string", "enum": [ "logical_composite" ] },
        "key": { "type": "string" },
        "name": { "type": [ "string", "null" ] },
        "description": { "type": [ "string", "null" ] },
        "devices": { "type": "array", "items": { "$ref": "#/$defs/keyRef" } },
        "power_units": { "type": "array", "items": { "$ref": "#/$defs/pdu" } },
        "fan_shelves": { "type": "array", "items": { "$ref": "#/$defs/fan_shelf" } } },
      "required": [ "key", "name" ]
    },
    "pdu": {
      "type": "object",
      "properties": {
        "class": { "type": "string", "enum": [ "pdu" ] },
        "key": { "type": "string" },
        "name": { "type": [ "string", "null" ] },
        "description": { "type": [ "string", "null" ] },
        "model_name": { "type": [ "string", "null" ] },
        "model_number": { "type": [ "string", "null" ] },
        "unit_position": { "type": [ "integer", "null" ], "minimum": 1 },
        "slots": { "type": "array", "items": { "$ref": "#/$defs/slot" } }
      },
      "required": [ "key", "name" ]
    },
    "fan_shelf": {
      "type": "object",
      "properties": {
        "class": { "type": "string", "enum": [ "fan_shelf" ] },
        "key": { "type": "string" },
        "name": { "type": [ "string", "null" ] },
        "description": { "type": [ "string", "null" ] },
        "slots": { "type": "array", "items": { "$ref": "#/$defs/slot" } }
      },
      "required": [ "key", "name" ]
    },
    "device": {
      "type": "object",
      "properties": {
        "class": { "type": "string", "enum": [ "device" ] },
        "key": { "type": "string" },
        "name": { "type": [ "string", "null" ] },
        "description": { "type": [ "string", "null" ] },
        "ip_address": { "type": [ "string", "null" ] },
        "mac_address": { "type": [ "string", "null" ] },
        "serial_number": { "type": [ "string", "null" ] },
        "model_name": { "type": [ "string", "null" ] },
        "model_number": { "type": [ "string", "null" ] },
        "manufacturer": { "type": [ "string", "null" ] },
        "firmware_version": { "type": [ "string", "null" ] },
        "slots": { "type": "array", "items": { "$ref": "#/$defs/slot" } },
        "ports": { "type": "array", "items": { "$ref": "#/$defs/port" } } },
      "required": [ "key", "name", "serial_number" ]
    },
    "slot": {
      "type": "object",
      "properties": {
        "class": { "type": "string", "enum": [ "slot" ] },
        "key": { "type": "string" },
        "name": { "type": [ "string", "null" ] },
        "description": { "type": [ "string", "null" ] },
        "model_name": { "type": [ "string", "null" ] },
        "model_number": { "type": [ "string", "null" ] },
        "manufacturer": { "type": [ "string", "null" ] },
        "unit_position": { "type": [ "integer", "null" ], "minimum": 1 },
        "cards": { "type": "array", "items": { "$ref": "#/$defs/card" } }
      },
      "required": [ "key", "name" ]
    },
    "card": {
      "type": "object",
      "properties": {
        "class": { "type": "string", "enum": [ "card" ] },
        "key": { "type": "string" },
        "name": { "type": [ "string", "null" ] },
        "description": { "type": [ "string", "null" ] },
        "mac_address": { "type": [ "string", "null" ] },
        "serial_number": { "type": [ "string", "null" ] },
        "firmware_version": { "type": [ "string", "null" ] },
        "model_name": { "type": [ "string", "null" ] },
        "model_number": { "type": [ "string", "null" ] },
        "manufacturer": { "type": [ "string", "null" ] },
        "unit_position": { "type": [ "integer", "null" ], "minimum": 1 },
        "slots": { "type": "array", "items": { "$ref": "#/$defs/slot" } },
        "ports": { "type": "array", "items": { "$ref": "#/$defs/port" } }
      },
      "required": [ "key", "name" ]
    },
    "port": {
      "type": "object",
      "properties": {
        "class": { "type": "string", "enum": [ "port" ] },
        "key": { "type": "string" },
        "name": { "type": [ "string", "null" ] },
        "description": { "type": [ "string", "null" ] },
        "model_name": { "type": [ "string", "null" ] },
        "ip_address": { "type": [ "string", "null" ] },
        "virtual": { "type": "boolean", "default": false },
        "unit_position": { "type": [ "integer", "null" ], "minimum": 1 },
        "bandwidth_name": { "type": [ "string", "null" ] },
        "bandwidth_group": { "type": [ "string", "null" ] },
        "bandwidth": { "type": [ "integer", "null" ], "minimum": 0 },
        "mtu_size": { "type": [ "integer", "null" ], "minimum": 0 }
      },
      "required": [ "key", "name" ]
    },
    "number": {
      "type": "object",
      "properties": {
        "class": { "type": "string", "enum": [ "number" ] },
        "key": { "type": "string" },
        "name": { "type": [ "string", "null" ] },
        "related_ci_type": { "type": "string", "enum": [ "Network Interface", "Physical Connection", "Logical Connection", "Equipment", "Topology" ] },
        "related_ci": { "$ref": "#/$defs/keyRef" },
        "type": { "type": "string", "enum": [ "vlan_range", "vlan_subrange", "vlan", "lag_range", "lag" ] },
        "vlan_type": { "type": "string", "enum": [ "inner", "outer" ] },
        "value": { "$ref": "#/$defs/value" }
      },
      "required": [ "key", "name", "type", "related_ci_type", "related_ci", "value" ] },
    "logical_connection": {
      "type": "object",
      "properties": {
        "class": { "type": "string", "enum": [ "logical_connection" ] },
        "key": { "type": "string" },
        "name": { "type": [ "string", "null" ] },
        "description": { "type": [ "string", "null" ] },
        "model_name": { "type": [ "string", "null" ] },
        "bandwidth_group": { "type": [ "string", "null" ] },
        "bandwidth_name_a_to_z": { "type": [ "string", "null" ] },
        "bandwidth_name_z_to_a": { "type": [ "string", "null" ] },
        "bandwidth_a_to_z": { "type": [ "integer", "null" ], "minimum": 0 },
        "bandwidth_z_to_a": { "type": [ "integer", "null" ], "minimum": 0 },
        "equipment_a": { "$ref": "#/$defs/optionalKeyRef" },
        "equipment_z": { "$ref": "#/$defs/optionalKeyRef" },
        "port_a": { "$ref": "#/$defs/keyRef" },
        "port_z": { "$ref": "#/$defs/keyRef" }
      },
      "required": [ "key", "name", "equipment_a", "equipment_z", "port_a", "port_z" ]
    },
    "port_relation": {
      "type": "object",
      "properties": {
        "class": { "type": "string", "enum": [ "port_relation" ] },
        "parent": { "$ref": "#/$defs/keyRef" },
        "child": { "$ref": "#/$defs/keyRef" }
      },
      "required": [ "parent", "child" ]
    },
    "logical_connection_relation": {
      "type": "object",
      "properties": {
        "class": { "type": "string", "enum": [ "logical_connection_relation" ] },
        "sequence": { "type": [ "integer", "null" ], "minimum": 1 },
        "route": { "type": [ "integer", "null" ], "minimum": 1 },
        "parent": { "$ref": "#/$defs/keyRef" },
        "child": { "$ref": "#/$defs/keyRef" }
      },
      "required": [ "parent", "child" ]
    },
    "network_topology": {
      "type": "object",
      "properties": {
        "class": { "type": "string", "enum": [ "network_topology" ] },
        "key": { "type": "string" },
        "name": { "type": "string" },
        "model_name": { "type": [ "string", "null" ] },
        "devices": { "type": "array", "items": { "key": "#/$defs/optionalKeyRef" } },
        "logical_connections": { "type": "array", "items": { "key": "#/$defs/optionalKeyRef" } }
      },
      "required": [ "key", "name", "devices", "logical_connections" ]
    }
  }
}
```

## 2. Decouple Connectivity from ETL

Ensure flexibility by separating device interaction logic from transformation logic \(ETL ingestion\). Users can develop their own collectors independently of the ETL logic.

Ensure the following points:

1.  Design collectors to focus only on connectivity and data conversion to the unified schema.
2.  Use or reuse any EMS/NMS adaptor \(including third-party adaptors like Atrinet\).
3.  Push the standardized data into ServiceNow import sets.

## 3. Configure Generic ETL for CMDB Updates

Use a single reusable ETL to process all standardized import sets and update the CMDB accurately.

Ensure the following points:

1.  Validate the import set contains data in the standardized JSON format.
2.  Use the TSOM Generic ETL to:
    -   Detect the entity type \(e.g., Slot, Card, Logical Interface\).
    -   Map each entity to the correct CI class based on model mapping logic.
    -   Populate fields including Inventory Category where applicable.

Special Handling:

-   Logical Interfaces → Port table \(`virtual=true`\)
-   Logical Connections → Logical Connection table
-   PDU Cards → PDU table
-   Equipment → Model-based CI class \(most recent mapping if multiple exist\)

## 4. Configure support for Multi-Chassis and Composite Devices

Model complex devices such as multi-chassis routers with correct CMDB relationships.

Ensure the following points:

1.  Use the Logical Composite construct to represent grouped entities like Router + PDU.
2.  Define individual components \(Fan, Management, Slot\) under their respective hierarchy.
3.  Map each entity as per the TNI modeling guidance.

Example: For a 7750-2s multi-chassis device:

-   Logical Composite → contains Router and PDU
-   PDU → contains Slots → Cards → Sub-slots

## 5. Enable TNI Entity Creation Based on Installation

Ensure consistency with TNI standards without unnecessary record creation.

Ensure the following points:

-   If TNI is installed:
    -   Automatically create a TNI Entity for each discovered CI.
    -   Set Inventory Category appropriately \(e.g., "Logical Connection", "Interface"\).
-   If TNI is not installed: Skip TNI entity creation to avoid orphaned or invalid records.

