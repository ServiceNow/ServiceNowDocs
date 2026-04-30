---
title: CMDB classes targeted in the Service Graph Connector for Splunk
description: When you complete setting up the connection, you can configure the integration to periodically pull data. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Splunk, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in the Service Graph Connector for Splunk

When you complete setting up the connection, you can configure the integration to periodically pull data. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Hardware \[cmdb\_ci\_computer\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Serial Number|serial\_number|
|Operating System|os|
|OS Version|os\_version|
|CPU name|cpu\_name|
|CPU manufacturer|cpu\_manufacturer|
|CPU type|cpu\_type|
|CPU speed \(MHz\)|cpu\_speed|
|CPU core count|cpu\_core\_count|
|CPU count|cpu\_count|
|Manufacturer|manufacturer|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|IP Address|ip\_address|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|MAC Address|mac\_address|
|Manufacturer|manufacturer|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Version|version|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Product name|software|
|Installed On|installed\_on|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data. This table is populated only when the Software Asset Management applications are installed.

|Attribute label|Attribute name|
|---------------|--------------|
|Display Name|display\_name|
|Version|version|
|Discovery Source|discovery\_source|

## Splunk Asset Details \[sn\_sec\_sgc\_splunk\_asset\_details​\]

The following attributes in the Splunk Asset Details \[sn\_sec\_sgc\_splunk\_asset\_details​\] table are populated by collected data.

|Attribute label|Attribute name|
|---------------|--------------|
|Configuration Item|configuration\_item|
|Forwarder GUID|forwarder\_guid|
|Forwarder Type|forwarder\_type|
|Forwarder Version|forwarder\_version|
|Host Name|host\_name|
|Host Status|host\_status|
|Host type|host\_type|
|Last logon date|last\_check\_in|
|Model Name|model\_name|
|OS Architecture|os\_architecture|
|OS Build Number|os\_build\_number|
|OS Family|os\_family|

## Relationships created for Computer

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Computer \[cmdb\_rel\_ci|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Computer \[cmdb\_rel\_ci|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Computer \[cmdb\_rel\_ci|Contains::Contained by|File system \[cmdb\_ci\_file\_system\]|

