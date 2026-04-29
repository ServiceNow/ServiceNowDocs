---
title: Serial number types for identification
description: As Discovery finds CIs, their serial numbers are listed in the Serial Number \[cmdb\_serial\_number\] table so they are easy to identify. Serial number types vary depending on the CI, as described in the following examples.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Discovery identifiers, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Serial number types for identification

As Discovery finds CIs, their serial numbers are listed in the Serial Number \[cmdb\_serial\_number\] table so they are easy to identify. Serial number types vary depending on the CI, as described in the following examples.

**Important:** Serial numbers are necessary for accurate asset tracking. If you modified baseline probes, sensors, or patterns, verify that they still discover serial numbers. In addition, do not configure sensors or patterns to modify the serial number syntax, such as adding a custom prefix. Non-standard serial numbers can lead to inaccurate asset tracking.

## Linux

In the result of dmidecode \| cat, the value on the left side is what Discovery looks for. The value on the right side is how it is stored in the Serial Number \[cmdb\_serial\_number\] table.

```
Serial Number : system_serial_number
 
UUID : uuid_serial
 
Serial Number : baseboard_serial
 
Serial Number : chassis_serial
```

## Windows

For Win32 WMI classes, the value on the left is the name by which it is stored in the Serial Number \[cmdb\_serial\_number\] table. The value on the right is the WMI value.

```
('system' : Win32_ComputerSystemProduct.IdentifyingNumber);
 
('uuid' : Win32_ComputerSystemProduct.UUID);
 
('chassis' : Win32_SystemEnclosure.SerialNumber);
 
('bios' : Win32_BIOS.SerialNumber);
 
('baseboard' : Win32_BaseBoard.SerialNumber);
```

## SNMP

For SNMP, the mapping below is based on the code. Physical types of serial numbers are from all instances of iso.org.dod.internet.mgmt.mib-2.entityMIB.

```
'cisco_stack' : 'iso.org.dod.internet.private.enterprises.cisco.workgroup.ciscoStackMIB.chassisGrp.chassisSerialNumberString'
 
'cisco_chassis' : 'iso.org.dod.internet.private.enterprises.cisco.temporary.chassis.chassisId'
 
'foundry' : 'iso.org.dod.internet.private.enterprises.foundry.products.switch.snChassis.snChasGen.snChasSerNum'
 
'apc_pdu' : 'iso.org.dod.internet.private.enterprises.apc.products.hardware.masterswitch.sPDUIdent.sPDUIdentSerialNumber'
 
'printer' : 'iso.org.dod.internet.mgmt.mib-2.printmib.prtGeneral.prtGeneralEntry'
 
'standard' : 'iso.org.dod.internet.private.enterprises.apc.products.hardware.ups.upsIdent.upsAdvIdent.upsAdvIdentSerialNumber'
```

**Parent Topic:**[Discovery identifiers](../concept/c_DiscoveryIdentifiers.md)

