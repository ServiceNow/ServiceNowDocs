---
title: CMDB classes targeted in Service Graph Connector for Tanium Endpoints
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Tanium. The data is saved in tables that extend from the Configuration Item \[cmdb\_ci\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-classes.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-05-12"
reading_time_minutes: 4
breadcrumb: [Tanium Endpoints, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Tanium Endpoints

When you complete setting up the connection, you can configure the integration to periodically pull data from Tanium. The data is saved in tables that extend from the Configuration Item \[cmdb\_ci\] table.

**Important:** The Service Graph Connector for Tanium Endpoints populates the Computer class with user-facing endpoints, and doesn't import data from the Server child class. Use this connector if you don't require Server data. If you require Server data, use the Service Graph Connector for Tanium.

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|CPU name|cpu\_name|
|CPU manufacturer|cpu\_manufacturer|
|Name|name|
|Serial number|serial\_number|
|Class|sys\_class\_name|
|CPU core count|cpu\_core\_count|
|CPU count|cpu\_count|
|CPU speed \(MHz\)|cpu\_speed|
|CPU type|cpu\_type|
|DNS Domain|dns\_domain|
|Fully qualified domain name|fqdn|
|IP Address|ip\_address|
|Is Virtual|virtual|
|Most recent discovery|last\_discovered|
|Operating System|os|
|OS Domain|os\_domain|
|OS Version|os\_version|
|Model ID|model\_id|
|OS Service Pack|os\_service\_pack|
|Manufacturer|manufacturer|
|RAM \(MB\)|ram|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Computer \[cmdb\_ci\_computer\]|Contains::Contained by|File System \[cmdb\_ci\_file\_system\]|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Computer \[cmdb\_ci\_computer\]|Contains::Contained by|Disk \[cmdb\_ci\_disk\]|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Computer \[cmdb\_ci\_computer\]|Reference|Key Value \[cmdb\_key\_value\]|
|Computer \[cmdb\_ci\_computer\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|

## Disk \[cmdb\_ci\_disk\]

The following attributes in the Disk \[cmdb\_ci\_disk\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Manufacturer|manufacturer|
|Device interface|device\_interface|
|Computer|computer|
|Model ID|model\_id|
|Device ID|device\_id|
|Name|name|
|Serial number|serial\_number|
|Size bytes|size\_bytes|
|Storage type|storage\_type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Disk \[cmdb\_ci\_disk\]|Reference|Computer \[cmdb\_ci\_computer\]|
|Disk \[cmdb\_ci\_disk\]|Reference|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|

## File System \[cmdb\_ci\_file\_system\]

The following attributes in the File System \[cmdb\_ci\_file\_system\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|File system|file\_system|
|Free space bytes|free\_space\_bytes|
|Label|label|
|Media type|media\_type|
|Size bytes|size\_bytes|
|Computer|computer|
|Mount point|mount\_point|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|File System \[cmdb\_ci\_file\_system\]|Reference|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|
|File System \[cmdb\_ci\_file\_system\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]

The following attributes in the Handheld Computing Device \[cmdb\_ci\_handheld\_computing\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Serial Number|serial\_number|
|Model ID|model\_id|
|Name|name|
|Class|sys\_class\_name|
|CPU core count|cpu\_core\_count|
|CPU name|cpu\_name|
|CPU speed \(MHz\)|cpu\_speed|
|CPU type|cpu\_type|
|DNS Domain|dns\_domain|
|Fully qualified domain name|fqdn|
|Is Virtual|virtual|
|Operating System|os|
|OS Domain|os\_domain|
|Manufacturer|manufacturer|
|CPU manufacturer|cpu\_manufacturer|
|IP Address|ip\_address|
|OS Service Pack|os\_service\_pack|
|OS Version|os\_version|
|RAM \(MB\)|ram|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Contains::Contained by|Disk \[cmdb\_ci\_disk\]|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Contains::Contained by|File System \[cmdb\_ci\_file\_system\]|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Reference|Key Value \[cmdb\_key\_value\]|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|

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

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|
|Tag|tag|

**Note:** Of the four tags available in Tanium \(Custom, Extended Custom, Enhanced, and Meta\), the Service Graph Connector for Tanium Endpoints 1.0.0 version supports only Custom tags. See [Supported Tanium resource types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-sgc-tanium-endpoints-resource-types.md).

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|DHCP Enabled|dhcp\_enabled|
|Model ID|model\_id|
|IP Address|ip\_address|
|MAC Address|mac\_address|
|Netmask|netmask|
|Mac manufacturer|mac\_manufacturer|
|Name|name|
|Discovery source|discovery\_source|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Computer \[cmdb\_ci\_computer\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|

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
|Manufacturer|manufacturer|
|Name|name|
|Key|key|
|Version|version|

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

