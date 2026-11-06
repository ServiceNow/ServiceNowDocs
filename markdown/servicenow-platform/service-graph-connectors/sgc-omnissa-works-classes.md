---
title: CMDB classes targeted in Service Graph Connector for Omnissa Workspace ONE UEM
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Omnissa. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/service-graph-connectors/sgc-omnissa-works-classes.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-09-22"
reading_time_minutes: 2
breadcrumb: [Omnissa Workspace ONE UEM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Omnissa Workspace ONE UEM

When you complete setting up the connection, you can configure the integration to periodically pull data from Omnissa. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Is Virtual|virtual|
|Manufacturer|manufacturer|
|Name|name|
|OS Version|os\_version|
|Model ID|model\_id|
|Serial number|serial\_number|
|Most recent discovery|last\_discovered|
|Assigned to|assigned\_to|
|Operating System|os|
|RAM \(MB\)|ram|

## Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]

The following attributes in the Handheld Computing Device \[cmdb\_ci\_handheld\_computing\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Serial number|serial\_number|
|IMEI|imei|
|Carrier|carrier|
|OS Version|os\_version|
|Model ID|model\_id|
|RAM \(MB\)|ram|
|Assigned to|assigned\_to|
|Name|name|
|Most recent discovery|last\_discovered|
|Manufacturer|manufacturer|
|MAC Address|mac\_address|
|Operating System|os|
|Phone Number|phone\_number|

## Hardware \[cmdb\_ci\_hardware\]

The following attribute in the Hardware \[cmdb\_ci\_hardware\] table are populated by collected data:

<table id="table_section_cmdb_ci_hardware_attrs"><tbody><tr><td>

Most recent discovery

</td><td>

last\_discovered

</td></tr></tbody>
</table>|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Hardware \[cmdb\_ci\_hardware\]|Reference|SG-Omnissa WS1 Device Related \[sn\_omnwoneuem\_inte\_sg\_omnissa\_ws1\_device\_related\]|

## Media Player \[cmdb\_ci\_media\_player\]

The following attributes in the Media Player \[cmdb\_ci\_media\_player\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Model ID|model\_id|
|Manufacturer|manufacturer|
|MAC Address|mac\_address|
|Name|name|
|Serial number|serial\_number|
|Most recent discovery|last\_discovered|
|Assigned to|assigned\_to|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
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
|Manufacturer|manufacturer|
|MAC Address|mac\_address|
|Name|name|
|Serial number|serial\_number|
|Most recent discovery|last\_discovered|
|Model ID|model\_id|
|Assigned to|assigned\_to|

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

## SG-Omnissa WS1 Device Related \[sn\_omnwoneuem\_inte\_sg\_omnissa\_ws1\_device\_related\]

The following attributes in the SG-Omnissa WS1 Device Related \[sn\_omnwoneuem\_inte\_sg\_omnissa\_ws1\_device\_related\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Device Id|device\_id|
|Device compliance state|device\_compliance\_state|
|Device ownership|device\_ownership|
|User email|user\_email|
|User name|user\_name|

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
|Installed on|installed\_on|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

