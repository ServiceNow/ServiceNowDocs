---
title: CMDB classes targeted in Service Graph Connector for Observability - AppDynamics
description: When you complete setting up the connection, you can configure the integration to periodically pull data from AppDynamics. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Observability-AppDynamics, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Observability - AppDynamics

When you complete setting up the connection, you can configure the integration to periodically pull data from AppDynamics. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## AppDynamics Extension \[sn\_sg\_appd\_extension\]

The following attributes in the AppDynamics Extension \[sn\_sg\_appd\_extension\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|AppDynamics ID|appdynamics\_id|
|Controller Name|controller\_name|
|Agent Type|agent\_type|
|Type|type|

## Application \[cmdb\_ci\_appl\]

The following attributes in the Application \[cmdb\_ci\_appl\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Class|sys\_class\_name|
|Name|name|
|Running process command|running\_process\_command|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Application \[cmdb\_ci\_appl\]|Runs on::Runs|Server \[cmdb\_ci\_server\]|
|Application \[cmdb\_ci\_appl\]|Reference|AppDynamics Extension \[sn\_sg\_appd\_extension\]|

## Calculated Application Service \[cmdb\_ci\_service\_calculated\]

The following attributes in the Calculated Application Service \[cmdb\_ci\_service\_calculated\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Hide from dashboard|hide\_from\_dashboard|
|Metadata|metadata|
|Operational status|operational\_status|
|Service Populator Status|populator\_status|
|Service Populator|service\_populator|
|Service Type|type|
|Short Description|short\_description|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Depends on::Used by|Application \[cmdb\_ci\_appl\]|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Depends on::Used by|Server \[cmdb\_ci\_server\]|
|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|Depends on::Used by|Calculated Application Service \[cmdb\_ci\_service\_calculated\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|Nic|nic|
|IP version|ip\_version|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|MAC Address|mac\_address|
|Name|name|
|Discovery source|discovery\_source|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Server \[cmdb\_ci\_server\]|

## Server \[cmdb\_ci\_server\]

The following attributes in the Server \[cmdb\_ci\_server\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Server \[cmdb\_ci\_server\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Server \[cmdb\_ci\_server\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Server \[cmdb\_ci\_server\]|Reference|Key Value \[cmdb\_key\_value\]|

