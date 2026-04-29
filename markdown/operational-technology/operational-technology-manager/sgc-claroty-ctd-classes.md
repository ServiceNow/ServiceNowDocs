---
title: CMDB classes targeted in the Service Graph Connector Integration for Claroty CTD
description: When you complete the setup tasks, you can configure the integration periodically to pull data from Claroty CTD. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Service Graph Connector Integration for Claroty CTD, Integrate, Operational Technology Manager, Operational Technology]
---

# CMDB classes targeted in the Service Graph Connector Integration for Claroty CTD

When you complete the setup tasks, you can configure the integration periodically to pull data from Claroty CTD. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Viewing class mappings

You can view the available class mappings for the Service Graph Connector Integration for Claroty CTD by navigating to **All** &gt; **Service Graph Connector Claroty CTD** &gt; **Class Mappings**. In the class mappings table, you can view the following attributes.

<table id="table_b2z_zgx_cdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Class

</td><td>

The class of the source CI.

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
</table>The Service Graph Connector Integration for Claroty CTD also uses Claroty types and codes. For more information, see the [Default class mapping](sgc-claroty-ctd-classes.md#default-class-mapping) table.

## Computer \[cmdb\_ci\_computer\]

The following attributes in the Computer \[cmdb\_ci\_computer\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Most recent discovery|last\_discovered|
|Operating System|os|
|OS Version|os\_version|

## External system metadata \[cmdb\_key\_value\_v2\]

The following attributes in the External system metadata \[cmdb\_key\_value\_v2\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Discovery source|discovery\_source|
|Key|key|
|Source key|source\_key|
|URL value|url\_value|
|Value type|value\_type|

## Firmware Installation \[cmdb\_firmware\_install\] 

The following attributes in the Firmware Installation \[cmdb\_firmware\_install\]  table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Source Native Key|firmware\_version\_snk|
|IRE criterion attribute|firmware\_ire\_criterion\_key|
|Discovered version|firmware\_version\_cleansed|
|Discovery source|firmware\_version\_discovery\_source|

## Hardware \[cmdb\_ci\_hardware\]

The following attributes in the Hardware \[cmdb\_ci\_hardware\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Change Group|assignment\_group|
|Support group|support\_group|
|Company|company|
|Vendor|vendor|
|Name|name|
|Serial number|serial\_number|
|Class|sys\_class\_name|
|First discovered|first\_discovered|
|Location|location|
|Model number|model\_number|
|Most recent discovery|last\_discovered|
|Supported by|supported\_by|
|Assigned to|assigned\_to|
|Managed By Group|managed\_by\_group|
|Managed by|managed\_by|
|Model ID|model\_id|
|Approval group|change\_control|
|Owned by|owned\_by|
|Manufacturer|manufacturer|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Hardware \[cmdb\_ci\_hardware\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Hardware \[cmdb\_ci\_hardware\]|Reference|OT Device \[cmdb\_ot\_entity\]|
|Hardware \[cmdb\_ci\_hardware\]|Reference|External system metadata \[cmdb\_key\_value\_v2\]|
|Hardware \[cmdb\_ci\_hardware\]|Reference|Software Installation \[cmdb\_sam\_sw\_install\]|

## IP Address \[cmdb\_ci\_ip\_address\]

The following attributes in the IP Address \[cmdb\_ci\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Owned By Configuration Item|owned\_by\_cmdb\_ci|
|IP Address|ip\_address|
|IP version|ip\_version|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|IP Address \[cmdb\_ci\_ip\_address\]| |Network Intrusion Detection System \[cmdb\_ci\_nids\]|
|IP Address \[cmdb\_ci\_ip\_address\]| |Hardware \[cmdb\_ci\_hardware\]|

## Network Adapter \[cmdb\_ci\_network\_adapter\]

The following attributes in the Network Adapter \[cmdb\_ci\_network\_adapter\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|MAC Address|mac\_address|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

## Network Intrusion Detection System \[cmdb\_ci\_nids\]

The following attributes in the Network Intrusion Detection System \[cmdb\_ci\_nids\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Manufacturer|manufacturer|
|Name|name|
|Correlation ID|correlation\_id|
|Description|short\_description|
|Firmware version|firmware\_version|
|NIDS manager connection state|connection\_state|
|Life Cycle Stage Status|life\_cycle\_stage\_status|
|Life Cycle Stage|life\_cycle\_stage|
|Validated|validated|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Network Intrusion Detection System \[cmdb\_ci\_nids\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Network Intrusion Detection System \[cmdb\_ci\_nids\]|Detects::Detected by|Hardware \[cmdb\_ci\_hardware\]|

## Operational Technology \(OT\) \[cmdb\_ci\_ot\]

The following attributes in the Operational Technology \(OT\) \[cmdb\_ci\_ot\] table are populated by collected data:

|Attribute label|Attribute name\\|
|---------------|----------------|
|Firmware version|firmware\_version|
|Most recent discovery|last\_discovered|

## OT Device \[cmdb\_ot\_entity\]

The following attributes in the OT Device \[cmdb\_ot\_entity\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Purdue level|purdue\_level|
|ISA entity site|isa\_entity\_site|
|OT discovery source ID|ot\_correlation\_id|
|Device criticality|business\_criticality|
|Zone|zone|
|OT device type|ot\_asset\_type|
|IRE criterion attribute|ire\_criterion\_attribute|

## OT Control Module \[cmdb\_ci\_ot\_control\_module\]

The following attributes in the OT Control Module \[cmdb\_ci\_ot\_control\_module\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Location|location|
|Supported by|supported\_by|
|Name|name|
|Serial number|serial\_number|
|Slot number|slot\_number|
|Manufacturer|manufacturer|
|Firmware version|firmware\_version|
|Approval group|change\_control|
|Assigned to|assigned\_to|
|Most recent discovery|last\_discovered|
|Model ID|model\_id|
|Model number|model\_number|
|Company|company|
|Owned by|owned\_by|
|Managed by|managed\_by|
|Support group|support\_group|
|Managed By Group|managed\_by\_group|
|Change Group|assignment\_group|
|Vendor|vendor|

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

## Serial Number \[cmdb\_serial\_number\]

The following attributes in the Serial Number \[cmdb\_serial\_number\] table are populated by collected data:

**Note:** A fix script is automatically applied to clean up the serial number \[cmdb\_serial\_number\] records imported into the sys\_object\_source table from the Service Graph Connector. The script ensures that a null pointer exception doesn't occur when a serial number and MAC address are the same.

This fix script only runs once during the upgrade of Service Graph Connector Integration for Claroty CTD but doesn't run on zbooted instances or fresh installation. This doesn't affect the functionality or lead to any data loss.

|Attribute label|Attribute name|
|---------------|--------------|
|Serial Number|serial\_number|
|Serial Number Type|serial\_number\_type|
|Valid|valid|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Serial Number \[cmdb\_serial\_number\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

## Software \[cmdb\_ci\_spkg\]

The following attributes in the Software \[cmdb\_ci\_spkg\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Version|version|
|Manufacturer|manufacturer|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software \[cmdb\_ci\_spkg\]|Reference|Software Instance \[cmdb\_software\_instance\]|

## Software Instance \[cmdb\_software\_instance\]

The following attributes in the Software Instance \[cmdb\_software\_instance\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Install date|install\_date|
|Installed on|installed\_on|
|Name|name|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

## Software Installation \[cmdb\_sam\_sw\_install\]

The following attributes in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Display name|display\_name|
|Version|version|
|Discovery source|discovery\_source|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Software Instance \[cmdb\_software\_instance\]|Reference|Hardware \[cmdb\_ci\_hardware\]|

## Default class mapping

A default class mapping is shipped with the Service Graph Connector Integration for Claroty CTD application.

**Note:** You can find the class mapping in the **sn\_clarotyctdsgc.SGOTClarotyCTDConstants** script.

|Claroty CTD Type|ServiceNow Type|Class|OT Entity Type|Claroty Types and Codes|
|----------------|---------------|-----|--------------|-----------------------|
|eAAAServer|\(Empty\)​|cmdb\_ci\_server​| |eAAAServer = 61​|
|eAccessControl​|\(Empty\)​|cmdb\_ci\_iot​| |eAccessControl = 50​|
|eAccessPoint​|\(Empty\)​|cmdb\_ci\_ip\_switch​| |eAccessPoint = 60​|
|eADServer​|\(Empty\)​|cmdb\_ci\_server​| |eADServer = 33​|
|eAutonomousVehicle​|OT Field Device​|cmdb\_ci\_ot\_field\_device​|ot\_field\_device​|eAutonomousVehicle = 58​|
|eAVServer​|\(Empty\)​|cmdb\_ci\_server​| |eAVServer = 32​|
|eBarcodeScanner​|OT Field Device​|cmdb\_ci\_ot\_field\_device​|ot\_field\_device​|eBarcodeScanner = 48​|
|eBluetoothDevice​|\(Empty\)​|cmdb\_ci\_iot​| |eBluetoothDevice = 41​|
|eBroadcast​|\(Empty\)​|cmdb\_ci\_netgear​| |eBroadcast = 4​|
|eCamera​|OT Field Device​|cmdb\_ci\_ot\_field\_device​|ot\_field\_device​|eCamera = 42​|
|eCleaningDevice​|OT Field Device​|cmdb\_ci\_ot\_field\_device​|ot\_field\_device​|eCleaningDevice = 55​|
|eController​|OT Control System​|cmdb\_ci\_ot\_control​|ot\_control\_system​|eController = 20​|
|eDataLogger​|OT Control System​|cmdb\_ci\_ot\_control​|ot\_control\_system​|eDataLogger = 66​|
|eDBServer​|\(Empty\)​|cmdb\_ci\_server​| |eDBServer = 35​|
|eDomainController​|\(Empty\)​|cmdb\_ci\_server​| |eDomainController = 5​|
|eElectricalDrive​|Industrial Drive​|cmdb\_ci\_ot\_industrial\_drive​|industrial\_drive​|eElectricalDrive = 68​|
|eEndpoint​|Operational Technology Device​|cmdb\_ci\_ot​|ot\_base​|eEndpoint = 2​|
|eEngineeringStation​|EWS|cmdb\_ci\_ot\_ews​|ews|eEngineeringStation = 14​|
|eFileServer​|\(Empty\)​|cmdb\_ci\_server​| |eFileServer = 10​|
|eFirewall​|\(Empty\)​|cmdb\_ci\_ip\_firewall​| |eFirewall = 31|
|eFrontEndProcessor​|OT Control System​|cmdb\_ci\_ot\_control​|ot\_control\_system​|eFrontEndProcessor = 26​|
|eGateway​|\(Empty\)​|cmdb\_ci\_ip\_switch​| |eGateway = 15​|
|eGPSClock​|Operational Technology Device​|cmdb\_ci\_ot​|ot\_base​|eGPSClock = 37​|
|eGPSDevice​|Operational Technology Device​|cmdb\_ci\_ot​|ot\_base​|eGPSDevice = 62​|
|eHistorian​|Historian|cmdb\_ci\_ot\_historian​|historian|eHistorian = 9​|
|eHMI​|HMI|cmdb\_ci\_ot\_hmi​|hmi|eHMI = 1​|
|eHomeAssistant​|\(Empty\)​|cmdb\_ci\_iot​| |eHomeAssistant = 53​|
|eIED​|IED|cmdb\_ci\_ot\_ied​|ied|eIED = 19​|
|eInfusionPump|\(Empty\)​|cmdb\_ci\_iot​| |eInfusionPump = 46|
|eMediaServer​|\(Empty\)​|cmdb\_ci\_server​| |eMediaServer = 54​|
|eMedicalDevice​|\(Empty\)​|cmdb\_ci\_iot​| |eMedicalDevice = 47​|
|eMicroscope​|\(Empty\)​|cmdb\_ci\_iot​| |eMicroscope = 49​|
|eModem​|\(Empty\)​|cmdb\_ci\_netgear​| |eModem = 27​|
|eMotorStarter​|Industrial Drive|cmdb\_ci\_ot\_industrial\_drive​|industrial\_drive​|eMotorStarter = 69​|
|eNetworkAccessStorage​|\(Empty\)​|cmdb\_ci\_server​| |eNetworkAccessStorage = 30​|
|eNetworking​|\(Empty\)​|cmdb\_ci\_netgear​| |eNetworking = 3​|
|eNTPServer​|\(Empty\)​|cmdb\_ci\_server​| |eNTPServer = 21​|
|eOPCServer​|OPC Server​|cmdb\_ci\_ot\_opc\_server​|opc\_server|eOPCServer = 16​|
|eOT​|Operational Technology Device​|cmdb\_ci\_ot​|ot\_base​|eOT = 17​|
|ePLC​|PLC|cmdb\_ci\_ot\_plc​|plc|ePLC = 0​|
|ePrinter​|\(Empty\)|cmdb\_ci\_printer​| |ePrinter = 6​|
|eProxyServer​|\(Empty\)|cmdb\_ci\_netgear​| |eProxyServer = 28​|
|eRemoteIO​|OT Field Device​|cmdb\_ci\_ot\_field\_device​|ot\_field\_device​|eRemoteIO = 13|
|eReverseProxyServer​|\(Empty\)​|cmdb\_ci\_netgear​| |eReverseProxyServer = 29​|
|eRobot​|Industrial Robot​|cmdb\_ci\_ot\_industrial\_robot​|industrial\_robot​|eRobot = 57​|
|eRouter​|Router|cmdb\_ci\_ip\_router​| |eRouter = 11​|
|eRTU​|RTU|cmdb\_ci\_ot\_rtu​|rtu​|eRTU = 18​|
|eSCADAClient​|SCADA Client​|cmdb\_ci\_ot\_scada\_client​|scada\_client​|eSCADAClient = 7​|
|eSCADAMaster​|SCADA Server​|cmdb\_ci\_ot\_scada\_server​|scada\_server​|eSCADAMaster = 38​|
|eSCADAServer​|SCADA Server​|cmdb\_ci\_ot\_scada\_server​|scada\_server​|eSCADAServer = 8​|
|eSensor​|Industrial Sensor​|cmdb\_ci\_ot\_industrial\_sensor​|industrial\_sensor​|eSensor = 67​|
|eSmartLight​|\(Empty\)​|cmdb\_ci\_iot​| |eSmartLight = 51​|
|eSmartPhone​|\(Empty\)​|cmdb\_ci\_iot​| |eSmartPhone = 44​|
|eSmartWatch​|\(Empty\)​|cmdb\_ci\_iot​| |eSmartWatch = 45​|
|eStorageArray​|\(Empty\)​|cmdb\_ci\_server​| |eStorageArray = 36​|
|eStreamer​|\(Empty\)​|cmdb\_ci\_iot​| |eStreamer = 52​|
|eSwitch​|\(Empty\)​|cmdb\_ci\_ip\_switch​| |eSwitch = 12​|
|eSyslogServer​|\(Empty\)​|cmdb\_ci\_server​| |eSyslogServer = 25​|
|eTerminalServer|\(Empty\)​|cmdb\_ci\_server​| |eTerminalServer = 24|
|eTVScreen​|\(Empty\)​|cmdb\_ci\_iot​| |eTVScreen = 40​|
|eUPS|\(Empty\)​|cmdb\_ci\_ups​| |eUPS = 63​|
|eUserConsole​|HMI|cmdb\_ci\_ot\_hmi​|hmi|eUserConsole = 22​|
|eUserWorkstation​|HMI|cmdb\_ci\_ot\_hmi​|hmi|eUserWorkstation = 23​|
|eVendingMachine​|\(Empty\)​|cmdb\_ci\_iot​| |eVendingMachine = 43​|
|eVideoRecorder​|\(Empty\)​|cmdb\_ci\_server​| |eVideoRecorder = 64​|
|eVirtualizationServer​|\(Empty\)​|cmdb\_ci\_server​| |eVirtualizationServer = 65​|
|eVoipPhone​|\(Empty\)​|cmdb\_ci\_comm\_hardware​| |eVoipPhone = 39​|
|eVoipServer​|\(Empty\)​|cmdb\_ci\_server​| |eVoipServer = 56​|
|eWebServer​|\(Empty\)​|cmdb\_ci\_server​| |eWebServer = 34​|
|eWirelessLanController​|\(Empty\)​|cmdb\_ci\_netgear​| |eWirelessLanController = 59​|
|eBarcodeReader​|\(Empty\)​|cmdb\_ci\_iot​| |eBarcodeReader = 77​|
|eBiometricScanner​|\(Empty\)​|cmdb\_ci\_iot​| |eBiometricScanner = 74​|
|eDNSServer​|\(Empty\)​|cmdb\_ci\_server​| |eDNSServer = 75​|
|eSNMPScanner​|\(Empty\)​|cmdb\_ci\_server​| |eSNMPScanner = 73​|
|eSNMPServer​|\(Empty\)​|cmdb\_ci\_server​| |eSNMPServer = 72​|
|eVisionCamera​|OT Field Device​|cmdb\_ci\_ot\_field\_device​|ot\_field\_device​|eVisionCamera = 76​|
|eVisionController​|OT Control System​|cmdb\_ci\_ot\_control​|ot\_control\_system​|eVisionController = 78​|
|eVisionSensor​|OT Field Device​|cmdb\_ci\_ot\_field\_device​|ot\_field\_device​|eVisionSensor = 79​|
|eVOIPAccessPoint​|\(Empty\)​|cmdb\_ci\_ip\_switch​| |eVOIPAccessPoint = 71​|
|eVulnerabilityScanner​|\(Empty\)​|cmdb\_ci\_server​| |eVulnerabilityScanner = 70​|

**Parent Topic:**[Service Graph Connector Integration for Claroty CTD](../concept/sgc-cmdb-integration-claroty-ctd.md)

