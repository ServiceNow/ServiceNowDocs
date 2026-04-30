---
title: CMDB classes targeted in Service Graph Connector for Google Console
description: When you complete setting up the connection, you can configure the integration to periodically pull Google Console data from Chromebook devices. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Google Console, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Google Console

When you complete setting up the connection, you can configure the integration to periodically pull Google Console data from Chromebook devices. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|Google Console attribute|
|---------------|--------------|------------------------|
|Install Status|install\_status|status|
|Model number|model\_number|model|
|Model ID|model\_id|model|
|Manufacturer|manufacturer|model|
|Name|name|serialNumber|
|Serial number|serial\_number|serialNumber|
|Assigned|assigned|lastEnrollmentTime|
|Operating System|os|os|
|Operational status|operational\_status|status|
|OS Version|os\_version|osVersion|
|Assigned to|assigned\_to|annotatedUser|

<table id="table_ndv_jds_zxb"><thead><tr><th>

Parent class

</th><th>

Relationship type

</th><th>

Child class

</th></tr></thead><tbody><tr><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

Owns::Owned by

</td><td>

Network Adapter \[cmdb\_ci\_network\_adapter\]

</td></tr><tr><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

Owns::Owned by

</td><td>

IP Address \[cmdb\_ci\_ip\_address\]

</td></tr><tr><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

Reference

</td><td>

When the Software Asset Management \(SAM\) and SAM Foundation applications aren't installed:

 Software \[cmdb\_ci\_spkg\]

 Software Instance \[cmdb\_software\_instance\]

 When the SAM or SAM Foundation application is installed:

 Software Installation \[cmdb\_sam\_sw\_install\]

</td></tr></tbody>
</table>## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|Google Console attribute|
|---------------|--------------|------------------------|
|IP Address|ip\_address|lastKnownNetwork.ipAddress|
|Name|name|lastKnownNetwork.ipAddress|
|Nic|nic|macAddress|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|Google Console attribute|
|---------------|--------------|------------------------|
|Configuration Item|cmdb\_ci|serialNumber|
|MAC Address|mac\_address|macAddress|
|Name|name|macAddress|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data when the Software Asset Management \(SAM\) and SAM Foundation applications are not installed:

|Attribute label|Attribute name|Google Console attribute|
|---------------|--------------|------------------------|
|Key|key|name-version|
|Name|name|name|
|Version|version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data when the SAM application, the SAM Foundation application, or both are installed:

|Attribute label|Attribute name|Google Console attribute|
|---------------|--------------|------------------------|
|Discovery source|discovery\_source|None|
|Display name|display\_name|Name|
|Installed on|installed\_on|serialNumber|
|Version|version|Version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Installation \[cmdb\_sam\_sw\_install\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data when the SAM and SAM Foundation applications are not installed:

|Attribute label|Attribute name|Google Console attribute|
|---------------|--------------|------------------------|
|Installed on|installed\_on|serialNumber|
|Name|name|name, version, serialNumber|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Computer \[cmdb\_ci\_computer\]|

