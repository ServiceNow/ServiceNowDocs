---
title: Network Inventory \(NI\) extension classes
description: The CMDB CI Class Models store app adds or updates classes for the Telecommunications Network Inventory application. Telecommunications Network Inventory uses the Network Inventory \(NI\) extension classes to extend the Configuration Management Database \(CMDB\) Configuration Item \(CI\) class hierarchy.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Network Inventory \(NI\) extension classes

The CMDB CI Class Models store app adds or updates classes for the Telecommunications Network Inventory application. Telecommunications Network Inventory uses the Network Inventory \(NI\) extension classes to extend the Configuration Management Database \(CMDB\) Configuration Item \(CI\) class hierarchy.

These extensions enable the CMDB to store information about a service provider's network inventory. The store app adds class models that extend the CMDB class hierarchy, including:

-   Class descriptions
-   Identification rules
-   Identifier entries
-   Dependent relationships, if applicable.

With the ServiceNow Telecommunications Network Inventory application, you can build a digital representation of your physical and logical networks. This application uses the NI class extensions to populate CIs that form the basis of your digital network inventory model. To learn more, see [Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=telecom-network-inventory&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Telecommunications Network Inventory \(NI\) schema structure​

![Relationships and references in Network Inventory schema.](../image/network-inventory-CIs.png)

## Classes

This section lists the relevant classes that the CMDB CI Class Models store app adds or updates. See the class columns table for further details about the columns added for each class. For the list of CMDB classes in a base system, including ones that this store app might be extending, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

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

Network Interface \[cmdb\_ci\_ni\_interface\]

</td><td>

Network Port \[cmdb\_ci\_ni\_network\_port\]

</td><td>

Network Interface. Captures and maintain equipment-specific attributes for the network interfaces.

</td></tr><tr><td>

Interface Card \[cmdb\_ci\_interface\_card\]

</td><td>

Hardware \[cmdb\_ci\_hardware\]

</td><td>

Interface Card.Represents interface cards that are stored in a network. Cards can occupy more than one slot and can contain other cards. They can be the equipment ports that are physical or logical \(virtual\). Each port is assigned a bandwidth value. The bandwidths are consumed when used in network designs.

</td></tr><tr><td>

Physical Connection \[cmdb\_ci\_ni\_physical\_link\]

</td><td>

Network Link \[cmdb\_ci\_network\_link\]

</td><td>

Physical Connection. Represents the physical port connections on the interface cards in your networks.

</td></tr><tr><td>

Logical Connection \[cmdb\_ci\_ni\_logical\_path\]

</td><td>

Network Circuit \[cmdb\_ci\_network\_circuit\]

</td><td>

Logical Connection. Represents the logical or virtual port connections on the network interface cards. A logical connection typically represents the multiple physical connections on an interface card.

</td></tr></tbody>
</table>