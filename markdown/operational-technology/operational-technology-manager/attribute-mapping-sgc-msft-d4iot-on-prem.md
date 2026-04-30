---
title: Attribute mapping and classification for the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)
description: The following tables describe the attribute mapping and classification for sensors and devices.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\), Integrate, Operational Technology Manager, Operational Technology]
---

# Attribute mapping and classification for the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)

The following tables describe the attribute mapping and classification for sensors and devices.

<table id="table_qrd_gkf_d1c"><thead><tr><th>

Payload field name

</th><th>

Data type

</th><th>

Mapped to table

</th><th>

Mapped to field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

String format: /subscriptions/&lt;subscription-id&gt;/provider/&lt;provider&gt;/locations/&lt;location&gt;/sites/&lt;site&gt;/sensor/&lt;sensor-name&gt;

</td><td>

-   sys\_object\_source
-   cmdb\_ci\_nids

</td><td>

-   snk in sys\_object\_source
-   correlation\_id

</td><td>

Unique ID for the sensor.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

cmdb\_ci\_nids

</td><td>

name

</td><td>

Name of the sensor.

</td></tr><tr><td>

properties.hostname

</td><td>

String

</td><td>

cmdb\_ci\_nids

</td><td>

fqdn

</td><td>

Host name of the sensor.

</td></tr><tr><td>

properties.ip

</td><td>

String

</td><td>

cmdb\_ci\_ip\_address

</td><td>

ip\_address

</td><td>

IP address of the sensor.

</td></tr><tr><td>

properties.learningMode

</td><td>

Boolean

</td><td>

cmdb\_ci\_nids

</td><td>

False or unavailable:

 Life Cycle Stage \(life\_cycle\_stage\) : Operational Life Cycle Stage Status \(life\_cycle\_stage\_status\): In Use

 True:

 Life Cycle Stage \(life\_cycle\_stage\) : Operational Life Cycle Stage Status \(life\_cycle\_stage\_status\): Learning

</td><td>

Learning mode status of the IoT sensor.

</td></tr><tr><td>

properties.mac

</td><td>

String

</td><td>

cmdb\_ci\_network\_adapter

</td><td>

name, mac\_address

</td><td>

MAC address of the sensor.

</td></tr><tr><td>

properties.sensorStatus

</td><td>

String

</td><td>

cmdb\_ci\_nids

</td><td>

connection\_state

</td><td>

Status of the IoT sensor.

</td></tr><tr><td>

properties.sensorVersion

</td><td>

String

</td><td>

cmdb\_ci\_nids

</td><td>

firmware\_version

</td><td>

Version of the IoT sensor.

</td></tr><tr><td>

properties.upSince\_utc

</td><td>

Date and time as string

</td><td>

cmdb\_ci\_nids

</td><td>

first\_discovered

</td><td>

Startup time.

</td></tr><tr><td>

properties.zone

</td><td>

String

</td><td>

cmdb\_ci\_nids

</td><td>

zone

</td><td>

Zone of the IoT sensor.

</td></tr></tbody>
</table><table id="table_vxm_f4f_d1c"><thead><tr><th>

Payload field name

</th><th>

Data type

</th><th>

Mapped to table

</th><th>

Mapped to field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

String format: /subscriptions/subscription-id&gt;/providers/&lt;providers-id&gt;/location/&lt;location&gt;/deviceGroups/&lt;device-Group&gt;/devices/&lt;name-field&gt;

</td><td>

-   sys\_object\_source
-   cmdb\_ot\_entity
-   cmdb\_key\_value\_v2

</td><td>

-   snk in sys\_object\_source
-   discovery\_source\_id in cmdb\_ot\_entity

</td><td>

Unique ID for the device.

</td></tr><tr><td>

resourceGroup

</td><td>

\(Empty\)

</td><td>

cmdb\_key\_value\_v2

</td><td>

\(Empty\)

</td><td>

Resource group

</td></tr><tr><td>

tenantId

</td><td>

\(Empty\)

</td><td>

cmdb\_key\_value\_v2

</td><td>

\(Empty\)

</td><td>

Tenant ID

</td></tr><tr><td>

properties.authorizedState

</td><td>

String

</td><td>

cmdb\_key\_value\_v2

</td><td>

\(Empty\)

</td><td>

Authorized state of the device

</td></tr><tr><td>

properties.criticality

</td><td>

String

</td><td>

cmdb\_ot\_entity

</td><td>

business\_criticality

</td><td>

Criticality of the device

</td></tr><tr><td>

properties.deviceName

</td><td>

String

</td><td>

cmdb\_ci

</td><td>

name

</td><td>

Name of the device.

</td></tr><tr><td>

properties.deviceSubTypeDisplayName

</td><td>

String

</td><td>

cmdb\_ci

</td><td>

sys\_class\_name

</td><td>

Device subtype display name.

</td></tr><tr><td>

properties.firstSeen

</td><td>

Date and time as string

</td><td>

-   cmdb\_ci
-   cmdb\_ci\_ot\_control\_module \(if control modules are present\)

</td><td>

first\_discovered

</td><td>

First time the device was seen.

</td></tr><tr><td>

properties.lastSeen

</td><td>

Date and time as string

</td><td>

-   cmdb\_ci
-   cmdb\_ci\_ot\_control\_module \(if control modules are present\)

</td><td>

most\_recent\_discovery

</td><td>

Last time the device was seen.

</td></tr><tr><td>

properties.purdueLevel

</td><td>

String

</td><td>

cmdb\_ot\_entity

</td><td>

purdue\_level

</td><td>

Purdue level of the device.

</td></tr><tr><td>

properties.operatingSystem.distribution

</td><td>

String

</td><td>

cmdb\_ci\_computer

</td><td>

os

</td><td>

OS distribution

</td></tr><tr><td>

properties.operatingSystem.version

</td><td>

String

</td><td>

cmdb\_ci\_computer

</td><td>

os\_version

</td><td>

OS version

</td></tr><tr><td>

properties.operatingSystem.platform

</td><td>

String

</td><td>

cmdb\_ci\_computer

</td><td>

os\_domain

</td><td>

OS platform

</td></tr><tr><td>

properties.operatingSystem.architecture

</td><td>

String

</td><td>

cmdb\_ci\_computer

</td><td>

os\_address\_width

</td><td>

OS architecture

</td></tr><tr><td>

properties.additionalFields.plcKeyState

</td><td>

\(Empty\)

</td><td>

cmdb\_ci\_ot\_plc

</td><td>

switch\_position

</td><td>

PLC key state

</td></tr><tr><td>

properties.additionalFields.plcRunState

</td><td>

\(Empty\)

</td><td>

cmdb\_ci\_ot\_plc

</td><td>

switch\_remote\_mode

</td><td>

PLC run state

</td></tr><tr><td>

properties.hardware

</td><td>

Object

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Device hardware data

</td></tr><tr><td>

properties.hardware.model

</td><td>

String

</td><td>

cmdb\_ci

</td><td>

\(Empty\)

</td><td>

Hardware model

</td></tr><tr><td>

properties.hardware.serialNumber

</td><td>

String

</td><td>

cmdb\_serial\_number

</td><td>

serial\_number

</td><td>

Hardware serial number

</td></tr><tr><td>

properties.hardware.vendor

</td><td>

String

</td><td>

cmdb\_ci

</td><td>

manufacturer

</td><td>

Hardware vendor

</td></tr><tr><td>

properties.nics

</td><td>

Array of Objects

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

List of the device network interface cards.

</td></tr><tr><td>

properties.nics\[\{\}\]

</td><td>

Object

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Network interface card properties

</td></tr><tr><td>

properties.nics\[\{\}\].ipv4Address

</td><td>

String

</td><td>

cmdb\_ci\_ip\_address

</td><td>

ip\_address

</td><td>

IPv4 address

</td></tr><tr><td>

properties.nics\[\{\}\].macAddress

</td><td>

String

</td><td>

cmdb\_ci\_network\_adapter

</td><td>

name, mac

</td><td>

MAC Address

</td></tr><tr><td>

properties.slots

</td><td>

Array of Objects

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

List of the device slot in the backplane.

</td></tr><tr><td>

properties.slots\[\{\}\]

</td><td>

Object

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Slot data in PLC backplane.

</td></tr><tr><td>

properties.slots\[\{\}\].firmwareVersion

</td><td>

String

</td><td>

cmdb\_ci\_ot\_control\_module

</td><td>

firmware\_version

</td><td>

Firmware version of the slot.

</td></tr><tr><td>

properties.slots\[\{\}\].model

</td><td>

String

</td><td>

cmdb\_ci\_ot\_control\_module

</td><td>

model\_id

</td><td>

Model of the slot.

</td></tr><tr><td>

properties.slots\[\{\}\].rackNumber

</td><td>

Integer

</td><td>

cmdb\_ci\_ot\_control\_module

</td><td>

rack\_number

</td><td>

Rack number in the backplane

</td></tr><tr><td>

properties.slots\[\{\}\].serialNumber

</td><td>

String

</td><td>

cmdb\_ci\_ot\_control\_module

</td><td>

serial\_number

</td><td>

Serial number of the slot.

</td></tr><tr><td>

properties.slots\[\{\}\].slotNumber

</td><td>

Integer

</td><td>

cmdb\_ci\_ot\_control\_module

</td><td>

slot\_number

</td><td>

Slot number inside the rack.

</td></tr><tr><td>

properties.slots\[\{\}\].hardwareVendor

</td><td>

String

</td><td>

cmdb\_ci\_ot\_control\_module

</td><td>

vendor

</td><td>

Hardware vendor of the slot.

</td></tr></tbody>
</table><table id="table_gth_v4f_d1c"><thead><tr><th>

Microsoft Azure device sub type name

</th><th>

Microsoft Azure device type name

</th><th>

Operating system/firmware

</th><th>

NOW class

</th><th>

NOW table

</th><th>

NOW OT type

</th></tr></thead><tbody><tr><td>

Alarm Siren

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Alarm System

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

OT Control System

</td><td>

cmdb\_ci\_ot\_control

</td><td>

OT Control System

</td></tr><tr><td>

ATM

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Backup Server

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Server

</td><td>

cmdb\_ci\_server

</td><td>

NULL

</td></tr><tr><td>

Barcode Scanner

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

DB Server

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Server

</td><td>

cmdb\_ci\_server

</td><td>

NULL

</td></tr><tr><td>

DCS Controller

</td><td>

Industrial

</td><td>

\(Empty\)

</td><td>

DCS

</td><td>

cmdb\_ci\_ot\_dcs

</td><td>

NULL

</td></tr><tr><td>

Domain Controller

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Server

</td><td>

cmdb\_ci\_server

</td><td>

NULL

</td></tr><tr><td>

Door Control Panel

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

DVR

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Elevator

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Engineering Station

</td><td>

Industrial

</td><td>

\(Empty\)

</td><td>

EWS

</td><td>

cmdb\_ci\_ot\_ews

</td><td>

EWS

</td></tr><tr><td>

Fire Alarm

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Fire Detector

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Firewall

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IP Firewall

</td><td>

cmdb\_ci\_ip\_firewall

</td><td>

NULL

</td></tr><tr><td>

Game console

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Game Console

</td><td>

cmdb\_ci\_game\_console

</td><td>

NULL

</td></tr><tr><td>

Historian

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Historian

</td><td>

cmdb\_ci\_ot\_historian

</td><td>

Historian

</td></tr><tr><td>

HMI

</td><td>

Industrial

</td><td>

\(Empty\)

</td><td>

HMI

</td><td>

cmdb\_ci\_ot\_hmi

</td><td>

HMI

</td></tr><tr><td>

Humidity Sensor

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

HVAC

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

HVAC Equipment

</td><td>

cmdb\_ci\_hvac

</td><td>

NULL

</td></tr><tr><td>

I/O Adapter

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Network Adapter

</td><td>

\(Empty\)

</td><td>

NA

</td></tr><tr><td>

IED

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IED

</td><td>

cmdb\_ci\_ot\_ied

</td><td>

ied

</td></tr><tr><td>

Industrial Packaging System

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

OT Field Device

</td><td>

cmdb\_ci\_ot\_field\_device

</td><td>

OT Field Device

</td></tr><tr><td>

Industrial Robot

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Industrial Robot

</td><td>

cmdb\_ci\_ot\_industrial\_robot

</td><td>

Industrial Robot

</td></tr><tr><td>

Industrial Scale

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

OT Field Device

</td><td>

cmdb\_ci\_ot\_field\_device

</td><td>

OT Field Device

</td></tr><tr><td>

Intercom

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

IP Camera

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IP Camera

</td><td>

cmdb\_ci\_ip\_camera

</td><td>

NULL

</td></tr><tr><td>

IP Telephone

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IP phone

</td><td>

cmdb\_ci\_ip\_phone

</td><td>

NULL

</td></tr><tr><td>

Marquee

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Meter

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Industrial Sensor

</td><td>

cmdb\_ci\_ot\_industrial\_sensor

</td><td>

Industrial Sensor

</td></tr><tr><td>

Motion Detector

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Multicast/Broadcast

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Netgear

</td><td>

cmdb\_ci\_netgear

</td><td>

NULL

</td></tr><tr><td>

NTP Server

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Server

</td><td>

cmdb\_ci\_server

</td><td>

NULL

</td></tr><tr><td>

People Counter System

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Physical Location

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

NULL

</td></tr><tr><td>

PLC

</td><td>

Industrial

</td><td>

\(Empty\)

</td><td>

PLC

</td><td>

cmdb\_ci\_ot\_plc

</td><td>

PLC

</td></tr><tr><td>

Pneumatic Device

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Industrial Actuator

</td><td>

cmdb\_ci\_ot\_industrial\_actuator

</td><td>

Industrial Actuator

</td></tr><tr><td>

Printer

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Printer

</td><td>

cmdb\_ci\_printer

</td><td>

NULL

</td></tr><tr><td>

Protocol Converter

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Netgear

</td><td>

cmdb\_ci\_netgear

</td><td>

NULL

</td></tr><tr><td>

Punch Clock

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Robot Controller

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

OT Control System

</td><td>

cmdb\_ci\_ot\_control

</td><td>

OT Control System

</td></tr><tr><td>

Router

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IP Router

</td><td>

cmdb\_ci\_ip\_router

</td><td>

NULL

</td></tr><tr><td>

RTU

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

RTU

</td><td>

cmdb\_ci\_ot\_rtu

</td><td>

NULL

</td></tr><tr><td>

Server

</td><td>

Server

</td><td>

\(Empty\)

</td><td>

Server

</td><td>

cmdb\_ci\_server

</td><td>

NULL

</td></tr><tr><td>

Servo Drive

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Industrial Actuator

</td><td>

cmdb\_ci\_ot\_industrial\_actuator

</td><td>

Industrial Actuator

</td></tr><tr><td>

Slot

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

OT Control Module

</td><td>

cmdb\_ci\_ot\_control\_module

</td><td>

OT Control Module

</td></tr><tr><td>

Smart Light

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Smart Phone

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Handheld Computing Device

</td><td>

cmdb\_ci\_handheld\_computing

</td><td>

NULL

</td></tr><tr><td>

Smart Switch

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Smart TV

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Smart Television

</td><td>

cmdb\_ci\_stv

</td><td>

NULL

</td></tr><tr><td>

Storage

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Server

</td><td>

cmdb\_ci\_server

</td><td>

NULL

</td></tr><tr><td>

Switch

</td><td>

Network Device

</td><td>

\(Empty\)

</td><td>

IP Switch

</td><td>

cmdb\_ci\_ip\_switch

</td><td>

NULL

</td></tr><tr><td>

Tablet

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Handheld Computing Device

</td><td>

cmdb\_ci\_handheld\_computing

</td><td>

NULL

</td></tr><tr><td>

Terminal Station

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Computer

</td><td>

cmdb\_ci\_computer

</td><td>

NULL

</td></tr><tr><td>

Thermostat

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

NULL

</td></tr><tr><td>

Turnstile

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

IoT device

</td><td>

cmdb\_ci\_iot

</td><td>

 

</td></tr><tr><td>

Uninterruptable Power Supply

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

UPS

</td><td>

cmdb\_ci\_ups

</td><td>

NULL

</td></tr><tr><td>

Variable Frequency Drive

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Industrial Drive

</td><td>

cmdb\_ci\_ot\_industrial\_drive

</td><td>

Industrial Drive

</td></tr><tr><td>

VPN Gateway

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Netgear

</td><td>

cmdb\_ci\_netgear

</td><td>

NULL

</td></tr><tr><td>

Wifi Pineapple

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Netgear

</td><td>

cmdb\_ci\_netgear

</td><td>

NULL

</td></tr><tr><td>

Wireless Access Point

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Wireless Access Point

</td><td>

cmdb\_ci\_wap\_network

</td><td>

NULL

</td></tr><tr><td>

WLAN access point

</td><td>

Network Device

</td><td>

\(Empty\)

</td><td>

Wireless Access Point

</td><td>

cmdb\_ci\_wap\_network

</td><td>

NULL

</td></tr><tr><td>

Workstation

</td><td>

Workstation

</td><td>

\(Empty\)

</td><td>

Computer

</td><td>

cmdb\_ci\_computer

</td><td>

NULL

</td></tr><tr><td>

Unknown

</td><td>

All

</td><td>

\(Empty\)

</td><td>

Operational Technology \(OT\)

</td><td>

cmdb\_ci\_ot

</td><td>

Operational Technology \(OT\)

</td></tr><tr><td>

Unclassified

</td><td>

Unclassified or All

</td><td>

\(Empty\)

</td><td>

Operational Technology \(OT\)

</td><td>

cmdb\_ci\_ot

</td><td>

Operational Technology \(OT\)

</td></tr><tr><td>

Any other type

</td><td>

\(Empty\)

</td><td>

\(Empty\)

</td><td>

Operational Technology \(OT\)

</td><td>

cmdb\_ci\_ot

</td><td>

Operational Technology \(OT\)

</td></tr><tr><td>

Any above type value except with designation Network and IoT

</td><td>

\(Empty\)

</td><td>

-   windows server
-   windows server, version 2004\[8\]
-   windows server, version 1909\[9\]
-   windows server, version 1903\[9\]
-   windows server 2019
-   windows server 2016
-   windows server 2012 r2
-   windows server 2012
-   windows server 2008 r2
-   windows server 2008
-   windows server 2003 r2
-   windows server 2003
-   windows 2000 server
-   windows nt 4.0 server
-   windows nt 3.51 server
-   windows nt 3.5 server
-   windows nt 3.1 server

</td><td>

Windows Server

</td><td>

cmdb\_ci\_linux\_server

</td><td>

Same as when the operating system isn't present.

</td></tr><tr><td>

Any above type value except with designation Network and IoT

</td><td>

\(Empty\)

</td><td>

-   linux
-   arch
-   centos
-   debian
-   fedora
-   suse
-   red hat
-   rhel
-   ubuntu
-   oracle

</td><td>

Linux Server

</td><td>

cmdb\_ci\_linux\_server

</td><td>

Same as when the operating system isn't present.

</td></tr><tr><td>

Any above type value except with designation Network and IoT

</td><td>

\(Empty\)

</td><td>

aix

</td><td>

AIX Server

</td><td>

cmdb\_ci\_aix\_server

</td><td>

Same as when the operating system isn't present.

</td></tr><tr><td>

Any above type value except with designation Network and IoT

</td><td>

\(Empty\)

</td><td>

esx

</td><td>

ESX Server

</td><td>

cmdb\_ci\_esx\_server

</td><td>

Same as when the operating system isn't present.

</td></tr><tr><td>

Any above type value except with designation Network and IoT

</td><td>

\(Empty\)

</td><td>

-   hp/ux
-   hpux

</td><td>

HP-UX Server

</td><td>

cmdb\_ci\_hpux\_server

</td><td>

Same as when the operating system isn't present.

</td></tr><tr><td>

Any above type value except with designation Network and IoT

</td><td>

\(Empty\)

</td><td>

-   hyper-v
-   hyperv
-   hyper

</td><td>

HypverV Server

</td><td>

cmdb\_ci\_hyper\_v\_server

</td><td>

Same as when the operating system isn't present.

</td></tr><tr><td>

Any above type value except with designation Network and IoT

</td><td>

\(Empty\)

</td><td>

-   solaris
-   sunos
-   sun os

</td><td>

Solaris Server

</td><td>

cmdb\_ci\_solaris\_server

</td><td>

Same as when the operating system isn't present.

</td></tr><tr><td>

Any above type value except with designation Network and IoT

</td><td>

\(Empty\)

</td><td>

-   macos x server
-   macos server
-   os x
-   osx

</td><td>

OSX Server

</td><td>

cmdb\_ci\_osx\_server

</td><td>

Same as when the operating system isn't present.

</td></tr><tr><td>

Any above type value except with designation Network and IoT

</td><td>

\(Empty\)

</td><td>

-   unix
-   gnu

</td><td>

Unix Server

</td><td>

cmdb\_ci\_unix\_server

</td><td>

Same as when the operating system isn't present.

</td></tr><tr><td>

Any above type value except with designation Network and IoT

</td><td>

\(Empty\)

</td><td>

-   win
-   windows
-   Microsoft
-   windows 1.0, 1.02, 1.03, 1.04, 2.03, 2.10, 2.11, 3.0, 3.1, 3.2, 7, 8, 8.1, 10, 98, 95
-   windows 2000
-   windows for workgroups 3.11
-   windows me
-   windows nt 3.1, 3.5, 3.51, 4.0
-   windows vista
-   windows xp
-   windows xp professional x64 edition

</td><td>

Base Computer class

</td><td>

cmdb\_ci\_computer

</td><td>

Same as when the operating system isn't present.

</td></tr><tr><td>

Any above type value except with designation Network and IoT

</td><td>

\(Empty\)

</td><td>

server

</td><td>

Base Server Class

</td><td>

cmdb\_ci\_server

</td><td>

Same as when the operating system isn't present.

</td></tr></tbody>
</table>**Parent Topic:**[Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)](../concept/integration-sgc-microsoft-defender-iot-on-prem.md)

