---
title: Network Inventory \(NI\) extension classes
description: The CMDB CI Class Models app adds or updates classes for the Telecommunications Network Inventory application. Telecommunications Network Inventory uses the Network Inventory \(NI\) extension classes to extend the Configuration Management Database \(CMDB\) Configuration item \(CI\) class hierarchy.
locale: en-US
release: australia
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [CMDB CI class models, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Network Inventory \(NI\) extension classes

The CMDB CI Class Models app adds or updates classes for the Telecommunications Network Inventory application. Telecommunications Network Inventory uses the Network Inventory \(NI\) extension classes to extend the Configuration Management Database \(CMDB\) Configuration item \(CI\) class hierarchy.

CMDB CI Class Models is a ServiceNow Store app that adds class models that extend the CMDB class hierarchy. The new or updated classes include class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

The extensions enable the CMDB to store information about a service provider's network inventory.

-   Class descriptions
-   Identification rules
-   Identifier entries
-   Dependent relationships, if applicable.

With the ServiceNow Telecommunications Network Inventory application, you can build a digital representation of your physical and logical networks. This application uses the NI class extensions to populate CIs that form the basis of your digital network inventory model. To learn more, see [Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecom-network-inventory.md).

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Telecommunications Network Inventory \(NI\) schema structure​

![Relationships and references in Network Inventory schema.](../image/network-inventory-CIs.png)

## Classes

This section lists the classes that the CMDB CI Class Models app adds or updates. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

<table id="table_kv4_rwq_zrb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Network Site \[cmdb\_ci\_ni\_site\]

</td><td>

Site \[cmdb\_ci\_site\]

</td><td>

Network Site. Captures and maintains the location-specific attributes for each network site, including the network centers, buildings, floors, and rooms where equipment is located.

The network site records enable you to view all the equipment at a location. You can filter the locations by the assigned type, role, or function categories.

</td></tr><tr><td>

Telco Equipment Holder \[cmdb\_ci\_ni\_equipment\_holder\]

</td><td>

Equipment Holder \[cmdb\_ci\_equipment\_holder\]

</td><td>

Telco Equipment Holder. Represents the physical units that contain the telecommunications equipment, including the cages, bays, cabinets, slots, relay racks, and line ups. The line ups contain the individual relay racks. Each relay rack contains the equipment shelves. The equipment holders can contain the other equipment holders.

The equipment holder records enable you to track and manage your network assets.

</td></tr><tr><td>

Telco Equipment \[cmdb\_ci\_ni\_telco\_equipment\]

</td><td>

Network gear \[cmdb\_ci\_netgear\]

</td><td>

Telco Equipment. Represents a shelf or device that provides the technical functionality in a network. Examples include the routers, modems, mobile devices, optical cables, relays, and switches. The equipment can have slots, cards, or ports. The equipment can exist within an equipment holder or by itself because not all equipment is rack mounted.

 The equipment records enable you to track and manage your network assets.

</td></tr><tr><td>

Telco Filler Component \[cmdb\_ci\_filler\_component\]

</td><td>

Hardware \[cmdb\_ci\_hardware\]

</td><td>

Filler Component.

 Represents a cover for empty spots/slots in a rack or device. Often made of flat metallic or plastic materials, helps separate cold and hot air zones, helps prevent dust from entering the chassis, and ensures proper airflow through the chassis or rack.

</td></tr><tr><td>

Telco Heat Baffle \[cmdb\_ci\_heat\_baffle\]

</td><td>

Filler Component \[cmdb\_ci\_filler\_component\]

</td><td>

Heat Baffle.

 Represents hardware used to help direct rising hot air away from equipment.

</td></tr><tr><td>

Telco Service Switching Point \(SSP\) \[cmdb\_ci\_service\_switching\_point\]

</td><td>

Telco Equipment \[cmdb\_ci\_ni\_telco\_equipment\]

</td><td>

Service Switching Point \(SSP\).

 Switch in a telecommunications network that sends a query to a central database called a service control point \(SCP\) via the SS7 network to determine how a TDM call can be routed. SSPs can be part of a voice switch or a separate computer connected to it.

</td></tr><tr><td>

Telco Service Control Point \(SCP\) \[cmdb\_ci\_service\_control\_point\]

</td><td>

Telco Equipment \[cmdb\_ci\_ni\_telco\_equipment\]

</td><td>

Service Control Point \(SCP\).

 Represents service control points \(SCPs\) in the Signaling System 7 \(SS7\) network responsible for routing calls and managing special features.

</td></tr><tr><td>

Telco Control Component \[cmdb\_ci\_telco\_control\_component\]

</td><td>

Telco Equipment \[cmdb\_ci\_ni\_telco\_equipment\]

</td><td>

Control Component.

 Device in a computer hardware component that creates an interface between a computer’s main system motherboard and other hardware components. Some will be integrated directly into the motherboard, while others may be added on as expansion devices.

</td></tr><tr><td>

Network Interface \[cmdb\_ci\_ni\_interface\]

</td><td>

Network Port \[cmdb\_ci\_ni\_network\_port\]

</td><td>

Network Interface. Captures and maintain equipment-specific attributes for the network interfaces.

Identification: Serial Number \(100\) Name \(200\)

Dependent on

-   Hardware \(contains::contained by\)
-   Logical Composite \(contains::contained by\)
-   Network Port \(contains::contained by\)
-   Virtual Machine Object \(contains::contained by\)
-   Kubernetes Component \(contains::contained by\)
-   Application Service \(contains::contained by\)

Attribute of Network Port: MTU Size \[mtu\_size\]

In networking, maximum transmission unit \(MTU\) is a measurement representing the largest data packet that a network-connected device will accept. Measured in integer bytes.

Use cases:-   Optimizing network performance: Setting the right MTU size can reduce overhead and maximize data throughput.
-   Avoiding fragmentation: A properly configured MTU helps prevent packet fragmentation, reducing processing load and transmission delays.
-   Tuning for network type: Different networks \(for example, VPNs, WANs\) may require specific MTU sizes to promote compatibility and optimal performance.

</td></tr><tr><td>

Network Interface Card \(formerly Interface Card\) \[cmdb\_ci\_interface\_card\]

</td><td>

Hardware \[cmdb\_ci\_hardware\]

</td><td>

Network Interface Card.Represents interface cards that are stored in a network. Cards can occupy more than one slot and can contain other cards. They can be the equipment ports that are physical or logical \(virtual\). Each port is assigned a bandwidth value. The bandwidths are consumed when used in network designs.

</td></tr><tr><td>

Network Service Instance \[cmdb\_ci\_network\_service\_instance\]

</td><td>

 

</td><td>

Network Service Instance represents a specific deployed, provisioned, and configured instance of a set of network services that, in turn, are based on network functions.

</td></tr><tr><td>

Physical Connection \[cmdb\_ci\_ni\_physical\_link\]

</td><td>

Network Link \[cmdb\_ci\_network\_link\]

</td><td>

Physical Connection. Represents the physical port connections on the network interface cards in your networks.

</td></tr><tr><td>

Logical Connection \[cmdb\_ci\_ni\_logical\_path\]

</td><td>

Network Circuit \[cmdb\_ci\_network\_circuit\]

</td><td>

Logical Connection. Represents the logical or virtual port connections on the network interface cards. A logical connection typically represents the multiple physical connections on an interface card.

</td></tr></tbody>
</table>