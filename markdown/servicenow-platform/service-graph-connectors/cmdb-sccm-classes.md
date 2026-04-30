---
title: CMDB classes targeted in Service Graph Connector for Microsoft SCCM
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Microsoft SCCM. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Microsoft SCCM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Microsoft SCCM

When you complete setting up the connection, you can configure the integration to periodically pull data from Microsoft SCCM. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Serial number|serial\_number|
|CPU core count|cpu\_core\_count|
|CPU speed \(MHz\)|cpu\_speed|
|CPU type|cpu\_type|
|CPU manufacturer|cpu\_manufacturer|
|Name|name|
|Asset tag|asset\_tag|
|Assigned|assigned|
|Chassis type|chassis\_type|
|Class|sys\_class\_name|
|CPU core thread|cpu\_core\_thread|
|CPU count|cpu\_count|
|CPU name|cpu\_name|
|Default Gateway|default\_gateway|
|DNS Domain|dns\_domain|
|Most recent discovery|last\_discovered|
|Operating System|os|
|OS Address Width \(bits\)|os\_address\_width|
|OS Domain|os\_domain|
|OS Service Pack|os\_service\_pack|
|OS Version|os\_version|
|RAM \(MB\)|ram|
|Model ID|model\_id|
|Manufacturer|manufacturer|
|Assigned to|assigned\_to|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Computer \[cmdb\_ci\_computer\]|Contains::Contained by|Disk \[cmdb\_ci\_disk\]|
|Computer \[cmdb\_ci\_computer\]|Reference|Key Value \[cmdb\_key\_value\]|
|Computer \[cmdb\_ci\_computer\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|
|Computer \[cmdb\_ci\_computer\]|Reference|SG-SCCM Computer Related \[sn\_sccm\_integrate\_sccm\_2019\_computer\_related\]|

## Disk \[cmdb\_ci\_disk\]

The following attributes in the Disk \[cmdb\_ci\_disk\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Disk space \(GB\)|disk\_space|
|Size bytes|size\_bytes|
|Computer|computer|
|Device ID|device\_id|
|Name|name|
|Description|short\_description|
|Drive type|drive\_type|
|Manufacturer|manufacturer|
|Model ID|model\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Disk \[cmdb\_ci\_disk\]|Reference|Computer \[cmdb\_ci\_computer\]|

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
|DHCP Enabled|dhcp\_enabled|
|Netmask|netmask|
|Configuration Item|cmdb\_ci|

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

## SG-SCCM Computer Related \[sn\_sccm\_integrate\_sccm\_2019\_computer\_related\]

The following attributes in the SG-SCCM Computer Related \[sn\_sccm\_integrate\_sccm\_2019\_computer\_related\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Resource ID|resource\_id|
|OU Name|ou\_name|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Name|name|
|Version|version|
|Vendor|vendor|
|Manufacturer|manufacturer|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data when the SAM application is installed:

|Attribute label|Attribute name|
|---------------|--------------|
|Publisher|publisher|
|Last scanned|last\_scanned|
|Installed on|installed\_on|
|Display name|display\_name|
|Discovery source|discovery\_source|
|Install date|install\_date|
|Prod id|prod\_id|
|Version|version|
|Revision|revision|
|Sccm group ID|sccm\_group\_id|
|SCCM TimeStamp|sccm\_timestamp|
|Assigned to|assigned\_to|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Installation \[cmdb\_sam\_sw\_install\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Installed on|installed\_on|
|Install date|install\_date|
|Sccm group ID|sccm\_group\_id|
|SCCM TimeStamp|sccm\_timestamp|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Computer \[cmdb\_ci\_computer\]|

