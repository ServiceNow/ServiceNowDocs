---
title: CMDB classes targeted in Service Graph Connector for VMware Workspace ONE UEM
description: When you complete setting up the connection, you can configure the integration to periodically pull data from VMware Workspace ONE Unified Endpoint Management \(UEM\). The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [VMware Workspace ONE UEM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for VMware Workspace ONE UEM

When you complete setting up the connection, you can configure the integration to periodically pull data from VMware Workspace ONE Unified Endpoint Management \(UEM\). The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Serial number|serial\_number|
|Is Virtual|virtual|
|Most recent discovery|last\_discovered|
|Operating System|os|
|OS Version|os\_version|
|RAM \(MB\)|ram|
|Assigned to|assigned\_to|
|Model ID|model\_id|
|Manufacturer|manufacturer|

## Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]

The following attributes in the Handheld Computing Device \[cmdb\_ci\_handheld\_computing\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|MAC Address|mac\_address|
|Name|name|
|Serial number|serial\_number|
|IMEI|imei|
|Most recent discovery|last\_discovered|
|Operating System|os|
|OS Version|os\_version|
|Phone Number|phone\_number|
|RAM \(MB\)|ram|
|Root Access|root\_access|
|Manufacturer|manufacturer|
|Model ID|model\_id|
|Carrier|carrier|
|Assigned to|assigned\_to|

## Hardware \[cmdb\_ci\_hardware\]

The following attribute in the Hardware \[cmdb\_ci\_hardware\] table is populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Most recent discovery|last\_discovered|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Hardware \[cmdb\_ci\_hardware\]|Reference|SG-Workspace ONE UEM Device Related \[sn\_vmwoneuem\_integ\_device\_related\]|
|Hardware \[cmdb\_ci\_hardware\]|Reference|Key Value \[cmdb\_key\_value\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Nic|nic|
|IP Address|ip\_address|
|IP version|ip\_version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|

## Media Player \[cmdb\_ci\_media\_player\]

The following attributes in the Media Player \[cmdb\_ci\_media\_player\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Serial number|serial\_number|
|Manufacturer|manufacturer|
|Model ID|model\_id|
|MAC Address|mac\_address|
|Assigned to|assigned\_to|
|Most recent discovery|last\_discovered|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Configuration Item|cmdb\_ci|
|MAC Address|mac\_address|
|Most recent discovery|last\_discovered|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

## Printer \[cmdb\_ci\_printer\]

The following attributes in the Printer \[cmdb\_ci\_printer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Assigned to|assigned\_to|
|MAC Address|mac\_address|
|Name|name|
|Most recent discovery|last\_discovered|
|Manufacturer|manufacturer|
|Model ID|model\_id|
|Serial number|serial number|

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
|Serial Number \[cmdb\_serial\_number\]|Reference|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|
|Serial Number \[cmdb\_serial\_number\]|Reference|Printer \[cmdb\_ci\_printer\]|
|Serial Number \[cmdb\_serial\_number\]|Reference|Media Player \[cmdb\_ci\_media\_player\]|

## SG-Workspace ONE UEM Device Related \[sn\_vmwoneuem\_integ\_device\_related\]

The following attributes in the SG-Workspace ONE UEM Device Related \[sn\_vmwoneuem\_integ\_device\_related\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Device ID|device\_id|
|Device Compliance State|compliance\_state|
|Device Ownership|device\_ownership|
|User Email|user\_email|
|User Name|user\_name|

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

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Installed on|installed\_on|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

