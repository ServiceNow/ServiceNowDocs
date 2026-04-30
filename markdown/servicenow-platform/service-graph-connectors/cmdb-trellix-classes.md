---
title: CMDB classes targeted in Service Graph Connector for Trellix
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Trellix. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Trellix, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Trellix

When you complete setting up the connection, you can configure the integration to periodically pull data from Trellix. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## File System \[cmdb\_ci\_file\_system\]

The following attributes in the File System \[cmdb\_ci\_file\_system\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Computer|computer|
|Disk Space \(GB\)|disk\_space|
|Free space bytes|free\_space\_bytes|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|File System \[cmdb\_ci\_file\_system\]|Reference|Server \[cmdb\_ci\_server\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|Netmask|netmask|
|Nic|nic|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Configuration Item|cmdb\_ci|
|IP Address|ip\_address|
|MAC Address|mac\_address|
|Name|name|
|Netmask|netmask|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Server \[cmdb\_ci\_server\]|

## Server \[cmdb\_ci\_server\]

The following attributes in the Server \[cmdb\_ci\_server\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Class|sys\_class\_name|
|CPU count|cpu\_count|
|CPU speed \(MHz\)|cpu\_speed|
|CPU type|cpu\_type|
|DNS Domain|dns\_domain|
|Host name|host\_name|
|Install Status|install\_status|
|IP Address|ip\_address|
|Is Virtual|virtual|
|MAC Address|mac\_address|
|Manufacturer|manufacturer|
|Model ID|model\_id|
|Name|name|
|Operating System|os|
|OS Service Pack|os\_service\_pack|
|OS Version|os\_version|
|RAM \(MB\)|ram|
|Serial number|serial\_number|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Server \[cmdb\_ci\_server\]|Contains::Contained by|Storage Disk \[cmdb\_ci\_storage\_disk\]|
|Server \[cmdb\_ci\_server\]|Contains::Contained by|File System \[cmdb\_ci\_file\_system\]|
|Server \[cmdb\_ci\_server\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Server \[cmdb\_ci\_server\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Name|name|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Discovery Source|discovery\_source|
|Installed on|installed\_on|
|Name|name|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Installation \[cmdb\_sam\_sw\_install\]|Reference|Server \[cmdb\_ci\_server\]|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Installed on|installed\_on|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Server \[cmdb\_ci\_server\]|

## Storage Disk \[cmdb\_ci\_storage\_disk\]

The following attributes in the Storage Disk \[cmdb\_ci\_storage\_disk\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Computer|computer|
|Disk space \(GB\)|disk\_space|
|Free disk space \(GB\)|free\_space|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Storage Disk \[cmdb\_ci\_storage\_disk\]|Reference|Server \[cmdb\_ci\_server\]|

**Related topics**  


[Service Graph Connector for Trellix](../concept/sgc-integration-trellix.md)

