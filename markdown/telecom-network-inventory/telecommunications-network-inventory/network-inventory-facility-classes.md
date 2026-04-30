---
title: Network inventory facility classes
description: The facility classes are used to represent power, HVAC, network, and their connectivity in a data center. You can define facility hardware records for these classes in the Telecommunications Network Inventory application.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-05-17"
reading_time_minutes: 3
breadcrumb: [Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Network inventory facility classes

The facility classes are used to represent power, HVAC, network, and their connectivity in a data center. You can define facility hardware records for these classes in the Telecommunications Network Inventory application.

|Class Name|Table Name|Extends from|Description|
|----------|----------|------------|-----------|
|Transformer|cmdb\_ci\_transformer|Power Equipment|Transformers change the voltage of alternating current \(AC\) in a power distribution system. You will find them in data centers and other power generation, transmission, and distribution networks. They either increase or decrease voltage levels for efficient transmission and safe power distribution.|
|Switch Gear|cmdb\_ci\_switch\_gear|Power Equipment|Switchgear helps manage and protect your electrical circuits in a telecom data center. It's key for safe, reliable power distribution.|
|Power Panel|cmdb\_ci\_power\_panel|Power Equipment|A Power Panel, often referred to as a power distribution panel or electrical panel. Power panels efficiently and safely manage and distribute electrical power to circuits and devices.|
|Rectifier|cmdb\_ci\_rectifier|Power Equipment|Rectifiers are essential for converting AC power to DC power. Your telecom and networking equipment rely on stable DC electricity.|
|Maintenance Bypass Panel|cmdb\_ci\_maintenance\_bypass\_panel|Power Equipment|A maintenance bypass panel \(MBP\) is an important part of your electrical power system, especially if you work with data centers. It lets you maintain or replace power equipment, like a UPS, without turning off power to other equipment. This is important to keep things running smoothly when you make updates.|
|Remote Power Panel|cmdb\_ci\_remote\_power\_panel|Power Equipment|A Remote Power Panel \(RPP\) distributes power in data centers to devices or other loads from a central source like a UPS or generator. They're useful for managing power in server racks and IT equipment.|
|Inverter|cmdb\_ci\_inverter|Power Equipment|An inverter takes the DC power from your telecom data center and changes it to AC power. While most telecom equipment uses DC power, you will need AC power for systems like air conditioning, lights, servers, and some monitoring devices.|
|Circuit Breaker|cmdb\_ci\_circuit\_breaker|Power Equipment|Circuit breakers protect your telecom data center from overloads, short circuits, and equipment failures. They automatically disconnect the power supply when something goes wrong to prevent damage, fire, or downtime.|
|Fuse Alarm Panel|cmdb\_ci\_fuse\_alarm\_panel\_function|Power Equipment|A Fuse Alarm Panel is a critical component in a telecom data center’s DC power distribution system. It serves two main purposes: Distributes DC power to various telecom loads \(like routers, switches, and other network equipment\). Monitors fuse status and triggers alarms when a fuse blows, enabling quick fault detection and response.|
|Rack Rail|cmdb\_ci\_rack\_rail|Hardware|A **rack rail** is a **mounting structure** inside a telecom or server rack that allows you to **securely install, support, and slide** equipment such as servers, switches, power supplies, and other hardware into place.|
|Wire Manager|cmdb\_ci\_wire\_manager|Hardware|A wire manager \(also called a cable manager or cable management system\) is a device or accessory used to organize, guide, protect, and secure network and power cables within telecom racks and data center infrastructure.|
|Cage|cmdb\_ci\_cage|Facility Hardware|A cage in a telecom data center is a secure, enclosed physical space within a larger data hall or colocation facility, built using metal mesh panels and lockable doors. It is used to isolate and protect a customer’s or department’s servers, telecom gear, and networking equipment from unauthorized access.|
|Rack PDU|cmdb\_ci\_rack\_pdu|PDU|A Rack PDU \(Power Distribution Unit\) is a critical component used in data centers and server rooms to distribute electrical power to multiple devices housed within a server rack. It serves as a centralized power management solution, ensuring reliable and efficient power delivery to IT equipment such as servers, switches, routers, and storage systems.|

**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

