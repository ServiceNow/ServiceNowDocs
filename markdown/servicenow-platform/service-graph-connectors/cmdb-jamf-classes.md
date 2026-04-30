---
title: CMDB classes targeted in Service Graph Connector for Jamf
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Jamf. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Jamf, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Jamf

When you complete setting up the connection, you can configure the integration to periodically pull data from Jamf. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|MAC Address|mac\_address|
|Name|name|
|Serial number|serial\_number|
|CPU core count|cpu\_core\_count|
|CPU count|cpu\_count|
|CPU name|cpu\_name|
|CPU speed \(MHz\)|cpu\_speed|
|CPU type|cpu\_type|
|DNS Domain|dns\_domain|
|Fully qualified domain name|fqdn|
|Most recent discovery|last\_discovered|
|OS Service Pack|os\_service\_pack|
|OS Version|os\_version|
|RAM \(MB\)|ram|
|Model ID|model\_id|
|Assigned to|assigned\_to|
|Manufacturer|manufacturer|
|Operating System|os|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Computer \[cmdb\_ci\_computer\]|Contains::Contained by|Disk \[cmdb\_ci\_disk\]|
|Computer \[cmdb\_ci\_computer\]|Reference|Key Value \[cmdb\_key\_value\]|
|Computer \[cmdb\_ci\_computer\]|Reference|SG-Jamf Extension Attributes \[sn\_jamf\_integrate\_extension\_attributes\]|

## Disk \[cmdb\_ci\_disk\]

The following attributes in the Disk \[cmdb\_ci\_disk\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Manufacturer|manufacturer|
|Computer|computer|
|Model ID|model\_id|
|Name|name|
|Serial number|serial\_number|
|Most recent discovery|last\_discovered|
|Size bytes|size\_bytes|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Disk \[cmdb\_ci\_disk\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]

The following attributes in the Handheld Computing Device \[cmdb\_ci\_handheld\_computing\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Description|short\_description|
|Carrier|carrier|
|Name|name|
|Serial number|serial\_number|
|Disk spae \(GB\)|disk\_space|
|ICCID|iccid|
|IMEI|imei|
|MEID|meid|
|Operating System|os|
|OS Version|os\_version|
|Phone Number|phone\_number|
|Root Access|root\_access|
|Manufacturer|manufacturer|
|Assigned to|assigned\_to|
|Model ID|model\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Reference|Key Value \[cmdb\_key\_value\]|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Reference|SG-Jamf Extension Attributes \[sn\_jamf\_integrate\_extension\_attributes\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|IP version|ip\_version|
|Most recent discovery|last\_discovered|
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
|Discovery Source|discovery\_source|
|Most recent discovery|last\_discovered|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Computer \[cmdb\_ci\_computer\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|

## Printer \[cmdb\_ci\_printer\]

The following attributes in the Printer \[cmdb\_ci\_printer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|IP Address|ip\_address|
|Most recent discovery|last\_discovered|

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

## SG-Jamf Extension Attributes \[sn\_jamf\_integrate\_extension\_attributes\]

The following attributes in the SG-Jamf Extension Attributes \[sn\_jamf\_integrate\_extension\_attributes\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Id|id|
|Extension Attributes|extension\_attributes|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data Software Asset Management \(SAM\) application isn't installed:

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
|Discovery source|discovery\_source|
|Display name|display\_name|
|Installed on|installed\_on|
|Last scanned|last\_scanned|
|Publisher|publisher|
|Version|version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Installation \[cmdb\_sam\_sw\_install\]|Reference|Server \[cmdb\_ci\_server\]|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data when the SAM application isn't installed:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Installed on|installed\_on|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|
|Software Instance \[cmdb\_software\_instance\]|Reference|Computer \[cmdb\_ci\_computer\]|

