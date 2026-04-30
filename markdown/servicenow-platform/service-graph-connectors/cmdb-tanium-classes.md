---
title: CMDB classes targeted in Service Graph Connector for Tanium
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Tanium. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Tanium, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Tanium

When you complete setting up the connection, you can configure the integration to periodically pull data from Tanium. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Application \[cmdb\_ci\_appl\]

The following attributes in the Application \[cmdb\_ci\_appl\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Class|sys\_class\_name|
|Name|name|
|Running process command|running\_process\_command|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Application \[cmdb\_ci\_appl\]|Runs on::Runs|Computer\[cmdb\_ci\_computer\]|

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Serial number|serial\_number|
|Class|sys\_class\_name|
|CPU core count|cpu\_core\_count|
|CPU count|cpu\_count|
|CPU speed \(MHz\)|cpu\_speed|
|CPU type|cpu\_type|
|DNS Domain|dns\_domain|
|IP Address|ip\_address|
|CPU manufacturer|cpu\_manufacturer|
|CPU name|cpu\_name|
|Is Virtual|virtual|
|Most recent discovery|last\_discovered|
|Operating System|os|
|OS Domain|os\_domain|
|OS Service Pack|os\_service\_pack|
|OS Version|os\_version|
|RAM \(MB\)|ram|
|Model ID|model\_id|
|Manufacturer|manufacturer|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Computer \[cmdb\_ci\_computer\]|Contains::Contained by|Disk \[cmdb\_ci\_disk\]|
|Computer \[cmdb\_ci\_computer\]|Contains::Contained by|File System \[cmdb\_ci\_file\_system\]|
|Computer \[cmdb\_ci\_computer\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|
|Computer \[cmdb\_ci\_computer\]|Virtualized by::Virtualizes|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

## Disk \[cmdb\_ci\_disk\]

The following attributes in the Disk \[cmdb\_ci\_disk\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Manufacturer|manufacturer|
|Name|name|
|Computer|computer|
|Serial number|serial\_number|
|Device interface|device\_interface|
|Storage type|storage\_type|
|Model ID|model\_id|
|Device ID|device\_id|
|Size bytes|size\_bytes|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Disk \[cmdb\_ci\_disk\]|Reference|Computer \[cmdb\_ci\_computer\]|

## File System \[cmdb\_ci\_file\_system\]

The following attributes in the File System \[cmdb\_ci\_file\_system\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|File system|file\_system|
|Free space bytes|free\_space\_bytes|
|Label|label|
|Media type|media\_type|
|Mount point|mount\_point|
|Size bytes|size\_bytes|
|Computer|computer|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|File System \[cmdb\_ci\_file\_system\]|Reference|Computer \[cmdb\_ci\_computer\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Nic|nic|
|IP Address|ip\_address|
|IP version|ip\_version|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Discovery source|discovery\_source|
|Netmask|netmask|
|Mac manufacturer|mac\_manufacturer|
|MAC Address|mac\_address|
|Name|name|
|Model ID|model\_id|
|DHCP Enabled|dhcp\_enabled|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Serial Number \[cmdb\_serial\_number\]

The following attributes in the Serial Number \[cmdb\_serial\_number\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Serial Number|serial\_number|
|Serial Number Type|serial\_number\_type|
|Valid|valid|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Serial Number \[cmdb\_serial\_number\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data when the Software Asset Management \(SAM\) application isn't installed:

|Attribute label|Attribute name|
|---------------|--------------|
|Version|version|
|Manufacturer|manufacturer|
|Key|key|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data when the SAM application is installed:

|Attribute label|Attribute name|
|---------------|--------------|
|Display name|display\_name|
|Publisher|publisher|
|Version|version|
|Discovery source|discovery\_source|
|Last scanned|last\_scanned|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data when the SAM application isn't installed:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Installed on|installed\_on|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

The following attribute in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table is populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Sys ID|sys\_id|

**Note:** Service Graph Connector for Tanium doesn't create a Virtual Machine Instance CI. During look-up in the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] table, if a VM instance is found that has an object ID that matches the cloud instance ID of a server instance, a relationship is created between that VM instance and the server instance.

