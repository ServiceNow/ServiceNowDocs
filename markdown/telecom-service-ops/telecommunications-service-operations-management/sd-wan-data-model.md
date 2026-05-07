---
title: SD-WAN data model
description: The ServiceNow AI Platform uses a custom data model that defines how SD-WAN connectors discover and retrieve device information.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Telecom data model, Explore, Telecommunications Service Operations Management]
---

# SD-WAN data model

The ServiceNow AI Platform® uses a custom data model that defines how SD-WAN connectors discover and retrieve device information.

The high-level Telecom Data Model, part of the Common Service Data Model \(CSDM\), does not define how specific technologies such as SD-WAN should be modeled. To address this gap, the SD-WAN data model provides a dedicated set of classes and relationships that define the structure of an SD-WAN network within the Configuration Management Database \(CMDB\).

The model documents comprehensive details about network assets, including configuration data, available ports, and bandwidth allocations across sites and services. This enables centralized management of SD-WAN repositories, streamlined provisioning and monitoring, and efficient resource allocation for building and maintaining network infrastructure.

The Discovery Builder framework supports the SD-WAN data model. You can use the framework to create and customize discovered objects that map directly to SD-WAN-specific classes and relationships, such as controllers, edge devices, tunnels, overlays, and underlays. Discovered data is mapped to the appropriate SD-WAN classes rather than to generic network CI types, supporting downstream assurance workflows such as fault management and performance monitoring."

## ServiceNow AI Platform® SD-WAN data model architecture

![SD-WAN architecture class relationships](../images/sd-wan-architecture.svg)

The following table describes the classes used in the SD-WAN data model and the type of data each class stores.

|Class|Description|
|-----|-----------|
|Group|Discovered organizations or administrative domains \(ADOMs\). Required|
|Company|Discovered organizations or administrative domains|
|Network site|Network site, including geographical information|
|Network service instance|Logical grouping of devices and their associated configurations|
|Network equipment models|Product model of the equipment|
|IP router or any other supported equipment classes|Hardware or network gear classification, used for storing information about network equipment|
|Key values|Additional attributes or fields related to a CI that aren't covered by predefined CI columns|
|Network interface|Network interface on a piece of equipment|
|Network adapter|Network adapter on a piece of equipment|
|IP address|Management IP address associated with a device|
|Per-device license|License assigned to a specific device. Optional|
|Location|Location of a network site|

