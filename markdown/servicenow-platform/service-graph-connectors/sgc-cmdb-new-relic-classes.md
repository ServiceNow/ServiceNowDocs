---
title: CMDB classes targeted in Service Graph Connector for Observability - New Relic
description: When you complete setting up the connection, you can configure the integration to periodically pull data from New Relic. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Observability - New Relic, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Observability - New Relic

When you complete setting up the connection, you can configure the integration to periodically pull data from New Relic. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Server \[cmdb\_ci\_server\]

The following attributes in the Server \[cmdb\_ci\_server\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|CPU core count|cpu\_core\_count|
|Disk space \(GB\)|disk\_space|
|DNS Domain|dns\_domain|
|Fully qualified domain name|fqdn|
|Host name|host\_name|
|Operating System|os|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Server \[cmdb\_ci\_server\]|Contains::Contained by|Disk \[cmdb\_ci\_disk\]|
|Server \[cmdb\_ci\_server\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Server \[cmdb\_ci\_server\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## Calculated Application Service \[cmdb\_ci\_service\_calculated\]

The following attributes in the Calculated Application Service \[cmdb\_ci\_service\_calculated\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Metadata|metadata|
|Service Populator Status|populator\_status|
|Service Type|type|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|IP version|ip\_version|
|Name|name|
|Nic|nic|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Installed on|installed\_on|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Server \[cmdb\_ci\_server\]|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Nic|nic|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

## Disk \[cmdb\_ci\_disk\]

The following attributes in the Disk \[cmdb\_ci\_disk\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Device ID|device\_id|
|Free disk space \(GB\)|free\_space|
|Computer|computer|
|Name|name|
|Disk space \(GB\)|disk\_space|
|File system|file\_system|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Disk \[cmdb\_ci\_disk\]|Hosted on::Hosts|Server \[cmdb\_ci\_server\]|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Configuration Item|cmdb\_ci|
|MAC Address|mac\_address|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Server \[cmdb\_ci\_server\]|

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

