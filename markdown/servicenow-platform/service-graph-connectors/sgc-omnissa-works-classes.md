---
title: CMDB classes targeted in Service Graph Connector for Omnissa Workspace ONE UEM
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Omnissa. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-omnissa-works-classes.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-09-22"
reading_time_minutes: 1
breadcrumb: [Omnissa Workspace ONE UEM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Omnissa Workspace ONE UEM

When you complete setting up the connection, you can configure the integration to periodically pull data from Omnissa. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]

The following attributes in the Handheld Computing Device \[cmdb\_ci\_handheld\_computing\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Imei|imei|
|Carrier|carrier|
|Model Id|model\_id|
|Os Version|os\_version|
|Name|name|
|Serial Number|serial\_number|
|Ram|ram|
|Os|os|
|Phone Number|phone\_number|
|Manufacturer|manufacturer|
|Mac Address|mac\_address|
|Assigned To|assigned\_to|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Name|name|
|Version|version|

## Hardware \[cmdb\_ci\_hardware\]

The following attributes in the Hardware \[cmdb\_ci\_hardware\] table are populated by collected data:

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|cmdb\_ci\_hardware|Owns::Owned by|cmdb\_ci\_network\_adapter|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Cmdb Ci|cmdb\_ci|
|Mac Address|mac\_address|

## Media Player \[cmdb\_ci\_media\_player\]

The following attributes in the Media Player \[cmdb\_ci\_media\_player\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Model Id|model\_id|
|Mac Address|mac\_address|
|Assigned To|assigned\_to|
|Serial Number|serial\_number|
|Manufacturer|manufacturer|

## Printer \[cmdb\_ci\_printer\]

The following attributes in the Printer \[cmdb\_ci\_printer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Manufacturer|manufacturer|
|Assigned To|assigned\_to|
|Model Id|model\_id|
|Serial Number|serial\_number|
|Name|name|
|Mac Address|mac\_address|

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Manufacturer|manufacturer|
|Os Version|os\_version|
|Name|name|
|Os|os|
|Serial Number|serial\_number|
|Ram|ram|
|Model Id|model\_id|
|Virtual|virtual|
|Assigned To|assigned\_to|

