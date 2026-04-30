---
title: SD-WAN data model
description: The ServiceNow AI Platform uses a custom data model that defines how SD-WAN connectors discover and retrieve device information.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [Telecom data model, Telecom Discovery, Telecom Visibility, Explore, Telecommunications Service Operations Management]
---

# SD-WAN data model

The ServiceNow AI Platform® uses a custom data model that defines how SD-WAN connectors discover and retrieve device information.

The ServiceNow AI Platform® integrates with three SD-WAN service providers: [Cisco Meraki](configuring-cisco-meraki-service-graph-connector.md), [Fortinet](configure-fortinet-service-graph-connector.md), and VeloCloud.

The SD-WAN data model defines the structure of an SD-WAN network by documenting classes, their relationships, and comprehensive details about network assets, including configuration data, available ports, and bandwidth allocations across sites and services. This enables centralized management of SD-WAN repositories, streamlined provisioning and monitoring, and efficient resource allocation for building and maintaining network infrastructure.

## ServiceNow AI Platform® SD-WAN data model architecture

The following table describes the entities used in the SD-WAN architecture and the classes to which they belong.

![SD-WAN class relationships](../images/sd-wan-architecture.svg)

<table id="table_sqw_123_1hc"><thead><tr><th>

Class

</th><th>

Entity class description

</th></tr></thead><tbody><tr><td>

Group

</td><td>

Discovered organizations or administrative domains \(ADOMs\) \(required\)

</td></tr><tr><td>

Company

</td><td>

Discovered organizations or administrative domains

</td></tr><tr><td>

Network site

</td><td>

Network site, including its geographical information

</td></tr><tr><td>

Network service instance

</td><td>

Logical grouping of devices and their associated configurations

</td></tr><tr><td>

Network equipment models

</td><td>

Product model of the equipment

</td></tr><tr><td>

IP router or any other supported equipment classes

</td><td>

Specific hardware classification, such as hardware or network gear, designated for storing information about network equipment

</td></tr><tr><td>

Key values

</td><td>

Table that stores additional attributes or fields related to a configuration item \(CI\) when those attributes aren’t covered by the existing predefined columns for CI

</td></tr><tr><td>

Network interface

</td><td>

Network interface on a piece of equipment

</td></tr><tr><td>

IP address

</td><td>

Stores the management IP address associated with a device

</td></tr><tr><td>

Per-device license

</td><td>

License assigned to a specific device \(optional\)

</td></tr><tr><td>

Location

</td><td>

Location of a network site

</td></tr></tbody>
</table>