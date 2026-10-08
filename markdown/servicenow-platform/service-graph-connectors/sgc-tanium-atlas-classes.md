---
title: CMDB classes targeted in Service Graph Connector for Tanium Atlas
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Tanium Atlas. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.html
release: brazil
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 2
breadcrumb: [Tanium Atlas, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Tanium Atlas

When you complete setting up the connection, you can configure the integration to periodically pull data from Tanium Atlas. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Software 1 - Computer \[cmdb\_ci\_spkg\]

The following attributes in the Software 1 - Computer \[cmdb\_ci\_spkg\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Key|key|
|Version|version|
|Manufacturer|manufacturer|

## Virtual Machine Instance 2 - Handheld Computing Device \[cmdb\_ci\_vm\_instance\]

The following attributes in the Virtual Machine Instance 2 - Handheld Computing Device \[cmdb\_ci\_vm\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Object Id|object\_id|

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Cpu Speed|cpu\_speed|
|Model Id|model\_id|
|Cpu Name|cpu\_name|
|Dns Domain|dns\_domain|
|Ram|ram|
|Cpu Type|cpu\_type|
|Name|name|
|Ip Address|ip\_address|
|Fqdn|fqdn|
|Virtual|virtual|
|Cpu Count|cpu\_count|
|Os Domain|os\_domain|
|Cpu Manufacturer|cpu\_manufacturer|
|Serial Number|serial\_number|
|Manufacturer|manufacturer|
|Os Service Pack|os\_service\_pack|
|Cpu Core Count|cpu\_core\_count|
|Os Version|os\_version|
|Os|os|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|cmdb\_ci\_computer|Runs on::Runs|cmdb\_ci\_vm\_instance|

## File System 1 - Computer \[cmdb\_ci\_file\_system\]

The following attributes in the File System 1 - Computer \[cmdb\_ci\_file\_system\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|File System|file\_system|
|Computer|computer|
|Media Type|media\_type|
|Label|label|
|Name|name|
|Size Bytes|size\_bytes|
|Mount Point|mount\_point|
|Free Space Bytes|free\_space\_bytes|

## Disk 1 - Computer \[cmdb\_ci\_disk\]

The following attributes in the Disk 1 - Computer \[cmdb\_ci\_disk\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Serial Number|serial\_number|
|Device Interface|device\_interface|
|Model Id|model\_id|
|Manufacturer|manufacturer|
|Size Bytes|size\_bytes|
|Computer|computer|
|Device Id|device\_id|
|Storage Type|storage\_type|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Ip Address|ip\_address|
|Mac Manufacturer|mac\_manufacturer|
|Netmask|netmask|
|Mac Address|mac\_address|
|Name|name|
|Discovery Source|discovery\_source|
|Dhcp Enabled|dhcp\_enabled|
|Model Id|model\_id|

## IP Address 2 - Handheld Computing Device \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address 2 - Handheld Computing Device \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Ip Address|ip\_address|
|Nic|nic|
|Ip Version|ip\_version|
|Name|name|

## Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]

The following attributes in the Handheld Computing Device \[cmdb\_ci\_handheld\_computing\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Serial Number|serial\_number|
|Os Domain|os\_domain|
|Cpu Speed|cpu\_speed|
|Os Service Pack|os\_service\_pack|
|Os|os|
|Ip Address|ip\_address|
|Os Version|os\_version|
|Cpu Type|cpu\_type|
|Cpu Manufacturer|cpu\_manufacturer|
|Manufacturer|manufacturer|
|Cpu Core Count|cpu\_core\_count|
|Dns Domain|dns\_domain|
|Cpu Name|cpu\_name|
|Fqdn|fqdn|
|Name|name|
|Virtual|virtual|
|Model Id|model\_id|
|Ram|ram|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|cmdb\_ci\_handheld\_computing|Runs on::Runs|cmdb\_ci\_vm\_instance|

