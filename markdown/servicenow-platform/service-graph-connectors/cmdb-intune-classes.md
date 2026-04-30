---
title: CMDB classes targeted in Service Graph Connector for Microsoft Intune
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Microsoft Intune. The data from the regular data sources \(SG-Intune Computer, SG-Intune Devices, and SG-Intune Software\) and the advanced data sources \(SG-Intune Device Reports and SG-Intune Software Reports\) is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2025-10-13"
reading_time_minutes: 3
breadcrumb: [Microsoft Intune, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Microsoft Intune

When you complete setting up the connection, you can configure the integration to periodically pull data from Microsoft Intune. The data from the regular data sources \(SG-Intune Computer, SG-Intune Devices, and SG-Intune Software\) and the advanced data sources \(SG-Intune Device Reports and SG-Intune Software Reports\) is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Serial number|serial\_number|
|Description|short\_description|
|Disk space \(GB\)|disk\_space|
|Manufacturer|manufacturer|
|Operating System|os|
|OS Version|os\_version|
|Model ID|model\_id|
|Assigned to|assigned\_to|
|Chassis type|chassis\_type|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Computer \[cmdb\_ci\_computer\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Computer \[cmdb\_ci\_computer\]|Reference|SG-Intune Computer Related \[sn\_intune\_integrat\_computer\_related\]|
|Computer \[cmdb\_ci\_computer\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|

## Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]

The following attributes in the Handheld Computing Device \[cmdb\_ci\_handheld\_computing\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Serial number|serial\_number|
|Description|short\_description|
|Disk space \(GB\)|disk\_space|
|IMEI|imei|
|MEID|meid|
|Operating System|os|
|OS Version|os\_version|
|Phone Number|phone\_number|
|Root Access|root\_access|
|Model ID|model\_id|
|Carrier|carrier|
|Assigned to|assigned\_to|
|Manufacturer|manufacturer|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Reference|SG-Intune Device Related \[sn\_intune\_integrat\_device\_related\]|
|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Display name|display\_name|
|Version|version|
|Discovery source|discovery\_source|
|Publisher|publisher|
|Installed on|installed\_on|

**Note:** The Publisher attribute is populated by the SG-Intune Software Reports data source only.

<table id="table_xqs_1hv_qwb"><thead><tr><th>

Parent class

</th><th>

Relationship type

</th><th>

Child class

</th></tr></thead><tbody><tr><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Reference

</td><td>

Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]Computer \[cmdb\_ci\_computer\]

</td></tr></tbody>
</table>## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|MAC Address|mac\_address|
|Name|name|
|Configuration Item|cmdb\_ci|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Computer \[cmdb\_ci\_computer\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP version|ip\_version|
|Owned By Configuration Item|owned\_by\_cmdb\_ci|
|IP Address|ip\_address|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Computer \[cmdb\_ci\_computer\]|

## Serial Number \[cmdb\_serial\_number\]

The following attributes in the Serial Number \[cmdb\_serial\_number\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Serial Number|serial\_number|
|Serial Number Type|serial\_number\_type|
|Valid|valid|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Serial Number \[cmdb\_serial\_number\]|Reference|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|
|Serial number \[cmdb\_serial\_number\]|Reference|Computer \[cmdb\_ci\_computer\]|

## SG-Intune Computer Related \[sn\_intune\_integrat\_computer\_related\]

The following attributes in the SG-Intune Computer Related \[sn\_intune\_integrat\_computer\_related\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Device ID|device\_id|
|Azure AD Registered|azure\_ad\_registered|
|Compliance State|compliance\_state|
|Device Enrollment Type|device\_enrollment\_type|
|Email Address|email\_address|
|Encrypted|is\_encrypted|
|Managed Device Owner Type|managed\_device\_owner\_type|
|Management Agent|management\_agent|
|Supervised|is\_supervised|

## SG-Intune Device Related \[sn\_intune\_integrat\_device\_related\]

The following attributes in the SG-Intune Device Related \[sn\_intune\_integrat\_device\_related\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Device ID|device\_id|
|Azure AD Registered|azure\_ad\_registered|
|Compliance State|compliance\_state|
|Device Category|device\_category|
|Device Enrollment Type|device\_enrollment\_type|
|Device State|device\_state|
|Email Address|email\_address|
|Encrypted|is\_encrypted|
|Managed Device Owner Type|managed\_device\_owner\_type|
|Management Agent|management\_agent|
|Security Patch Level|security\_patch\_level|
|Supervised|is\_supervised|
|System Management Bios Version|system\_management\_bios\_version|
|Wifi Subnet ID|wifi\_subnet\_id|

**Note:** The attributes Device Category, Device State, Security Patch Level, System Management Bios Version, and Wifi Subnet ID are populated by the SG-Intune Device Reports data source only.

The attributes Azure AD Registered, Device Enrollment Type, and Management Agent aren't populated by the SG-Intune Device Reports data source.

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
|Software Instance \[cmdb\_software\_instance\]|Reference|Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]|
|Software Instance \[cmdb\_software\_instance\]|Reference|Computer \[cmdb\_ci\_computer\]|

