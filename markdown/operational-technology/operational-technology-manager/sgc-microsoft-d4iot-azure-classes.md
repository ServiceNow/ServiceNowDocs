---
title: CMDB classes targeted in the Service Graph Connector for Microsoft Defender for IoT \(Azure\)
description: When you complete the guided setup, you can configure the integration to periodically pull data from a Service Graph Connector for Microsoft Defender for IoT \(Azure\) \(Azure\) project. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Service Graph Connector for Microsoft Defender for IoT \(Azure\), Integrate, Operational Technology Manager, Operational Technology]
---

# CMDB classes targeted in the Service Graph Connector for Microsoft Defender for IoT \(Azure\)

When you complete the guided setup, you can configure the integration to periodically pull data from a Service Graph Connector for Microsoft Defender for IoT \(Azure\) \(Azure\) project. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Viewing class mappings

You can view the available class mappings for the Service Graph Connector for Microsoft Defender for IoT \(Azure\) by navigating to **All** &gt; **Service Graph for MSFT D4IoT \(Azure\)** &gt; **Class Mappings**. In the class mappings table, you can view the following attributes.

<table id="table_b2z_zgx_cdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Class

</td><td>

The device type from the source system \(Azure\).

</td></tr><tr><td>

Target CMDB class

</td><td>

The expected ServiceNow class for the CI.

</td></tr><tr><td>

OT Device type

</td><td>

The category type that the OT device is classified as. The device type is also the function that the device plays on the OT network. For example:An IT device, such as a server, can be converted to an OT device, and the function it plays on the network is an HMI. Therefore, its class is **server** and its device type is **HMI**.

**Note:** In some cases, there are OT devices with no OT function or OT devices where the device type is unknown. For OT devices with no OT function, select **No OT Function**. For OT devices where the device type is unknown, select **Unknown**.

</td></tr><tr><td>

Allow OS classification

</td><td>

When set to **True**, if an operating system is found on the CI, the target is switched away from the target CMDB class to a ServiceNow class that matches its OS.

</td></tr><tr><td>

Active

</td><td>

When checked, the class mapping is set to **Active**.

</td></tr></tbody>
</table>## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Most recent discovery|last\_discovered|
|Operating System|os|
|OS Address Width \(bits\)|os\_address\_width|
|OS Domain|os\_domain|
|OS Version|os\_version|

## External system metadata \[cmdb\_key\_value\_v2\]

The following attributes in the External system metadata \[cmdb\_key\_value\_v2\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Discovery source|discovery\_source|
|Key|key|
|Source key|source\_key|
|String value|string\_value|
|URL value|url\_value|
|Value type|value\_type|

## Hardware \[cmdb\_ci\_hardware\]

The following attributes in the Hardware \[cmdb\_ci\_hardware\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Class|sys\_class\_name|
|Model number|model\_number|
|Most recent discovery|last\_discovered|
|Location|location|
|Model ID|model\_id|
|Manufacturer|manufacturer|
|First discovered|first\_discovered|
|Owned by|owned\_by|
|Approval group|change\_control|
|Managed By Group|managed\_by\_group|
|Managed by|managed\_by|
|Name|name|
|Company|company|
|Support group|support\_group|
|Change Group|assignment\_group|
|Assigned to|assigned\_to|
|Supported by|supported\_by|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Hardware \[cmdb\_ci\_hardware\]|Reference|External system metadata \[cmdb\_key\_value\_v2\]|
|Hardware \[cmdb\_ci\_hardware\]|Reference|OT Device \[cmdb\_ot\_entity\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|IP version|ip\_version|
|Owned By Configuration Item|owned\_by\_cmdb\_ci|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Network Intrusion Detection System \[cmdb\_ci\_nids\]|
|IP Address \[cmdb\_ci\_ip\_address\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|MAC Address|mac\_address|
|Name|name|
|Discovery source|discovery\_source|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Network Intrusion Detection System \[cmdb\_ci\_nids\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

## Network Intrusion Detection System \[cmdb\_ci\_nids\]

The following attributes in the Network Intrusion Detection System \[cmdb\_ci\_nids\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|First discovered|first\_discovered|
|NIDS source name|source\_name|
|Life Cycle Stage|life\_cycle\_stage|
|Life Cycle Stage Status|life\_cycle\_stage\_status|
|Name|name|
|Correlation ID|correlation\_id|
|Firmware version|firmware\_version|
|Fully qualified domain name|fqdn|
|NIDS assignment zone|zone|
|NIDS manager connection state|connection\_state|
|Validated|validated|
|Manufacturer|manufacturer|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Intrusion Detection System \[cmdb\_ci\_nids\]|Detects::Detected by|Hardware \[cmdb\_ci\_hardware\]|
|Network Intrusion Detection System \[cmdb\_ci\_nids\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Network Intrusion Detection System \[cmdb\_ci\_nids\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|

## Operational Technology \(OT\) \[cmdb\_ci\_ot\]

The following attributes in the Operational Technology \(OT\) \[cmdb\_ci\_ot\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Most recent discovery|last\_discovered|

## OT Control Module \[cmdb\_ci\_ot\_control\_module\]

The following attributes in the OT Control Module \[cmdb\_ci\_ot\_control\_module\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Vendor|vendor|
|Support group|support\_group|
|Serial number|serial\_number|
|Class|sys\_class\_name|
|First discovered|first\_discovered|
|Approval group|change\_control|
|Managed by|managed\_by|
|Managed By Group|managed\_by\_group|
|Change Group|assignment\_group|
|Company|company|
|Rack number|rack\_number|
|Slot number|slot\_number|
|Location|location|
|Name|name|
|Firmware version|firmware\_version|
|Most recent discovery|last\_discovered|
|Assigned to|assigned\_to|
|Owned by|owned\_by|
|Supported by|supported\_by|
|Model ID|model\_id|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|OT Control Module \[cmdb\_ci\_ot\_control\_module\]|Reference|OT Device \[cmdb\_ot\_entity\]|

## OT Control System \[cmdb\_ci\_ot\_control\]

The following attributes in the OT Control System \[cmdb\_ci\_ot\_control\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Has module|has\_module|
|Most recent discovery|last\_discovered|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|OT Control System \[cmdb\_ci\_ot\_control\]|Owns::Owned by|OT Control Module \[cmdb\_ci\_ot\_control\_module\]|

## OT Device \[cmdb\_ot\_entity\]

The following attributes in the OT Device \[cmdb\_ot\_entity\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|ISA entity site|isa\_entity\_site|
|OT discovery source ID|ot\_correlation\_id|
|Device criticality|business\_criticality|
|Purdue level|purdue\_level|
|Zone|zone|
|OT device type|ot\_asset\_type|
|IRE criterion attribute|ire\_criterion\_attribute|

## PLC \[cmdb\_ci\_ot\_plc\]

The following attributes in the PLC \[cmdb\_ci\_ot\_plc\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Most recent discovery|last\_discovered|
|Switch position|switch\_position|
|Switch remote|switch\_remote\_mode|

## Serial Number \[cmdb\_serial\_number\]

The following attributes in the Serial Number \[cmdb\_serial\_number\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Serial Number|serial\_number|
|Serial Number Type|serial\_number\_type|
|Valid|valid|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Serial Number \[cmdb\_serial\_number\]|Reference|Hardware \[cmdb\_ci\_hardware\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

**Parent Topic:**[Service Graph Connector for Microsoft Defender for IoT \(Azure\)](../concept/integration-sgc-microsoft-defender-iot-azure.md)

