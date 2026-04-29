---
title: Data model
description: The data model for Telecommunications Network Inventory displays the relationships between your network assets, infrastructure, and services. With this information, you can provision new services, modify existing services, maintain the network, and plan the forecast for the network growth in your organization.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Explore, Telecommunications Network Inventory]
---

# Data model

The data model for Telecommunications Network Inventory displays the relationships between your network assets, infrastructure, and services. With this information, you can provision new services, modify existing services, maintain the network, and plan the forecast for the network growth in your organization.

The data model contains the details about your network assets, such as the telco equipment configuration data, port availability of a framework, and bandwidth allocations between your sites and services. This data model enables you to build, manage, maintain, and allocate the network infrastructure and services. Further, this data model provides a for the automation of design and creation of your network equipment and connections that support the customer service orders and internal network orders.

The assets, services, and the relationships of your network inventory defines the infrastructure of your telecommunications networks. With this information, you can plan and forecast your network. You can store the data of the asset in a network inventory record.

The Telecommunications Network Inventory application uses the Network Inventory extension classes that extend the Configuration Management Database \(CMDB\) Configuration Item \(CI\) class hierarchy. These extensions enable the CMDB to store your network inventory information. Also, these extension classes provide the standardization and consistency that are aligned with the telecommunications industry standards bodies such as TeleManagement \(TM\) Forum and Metro Ethernet Forum \(MEF\). To learn more about the Network Inventory \(NI\) extension classes, see [Telecommunications Network Inventory extension classes](uses-for-network-inventory-data.md#section_jdk_55v_nkb).

The following diagram shows the extension classes in the data model for the network inventory.

![Infographic for network Inventory extension classes. For the details of extension classes, refer to the Network Inventory extension classes section.](../image/MMASSET0021144-tni-data-model.png "Network Inventory data model")

## Network site and Network location

Network site records in the Telecommunications Network Inventory application provide information about the physical location of your network equipment and resources. You can use network site records to:

-   monitor from where your network connections originate and terminate
-   monitor the network centers, buildings, floors, and rooms where your network assets are located
-   track the operational status of your network sites
-   map your network sites in your service topology
-   link your physical locations to your network sites for a better visualization
-   Identify network faults and outages

A network site is a configuration item \(CI\) in the Telecommunications Network Inventory application that's derived from the equipment and connections within the network site, while a location is simply a physical address.

## Telecommunications Network Inventory extension classes

The Telecommunications Network Inventory application uses the generic configuration item \(CI\) classes that extend the CMDB class hierarchy as shown in the following table. The following table describes the classes that are used within the application.

<table id="table_kv4_rwq_zrb"><thead><tr><th>

Telecommunications Network Inventory class

</th><th>

Extends generic CI class

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TNI CI Attributes \[tni\_entity\]

</td><td>

Non-CI class

</td><td>

Represents a collection of the common Telecommunications Network Inventory attributes. Use the TNI CI Attribute record to create the relevant common attributes relevant for Telecommunications Network Inventory and makes a relationship with the CI record. To learn more, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

</td></tr><tr><td>

Network Site \[cmdb\_ci\_ni\_site\]

</td><td>

Site \[cmdb\_ci\_site\]

</td><td>

Captures and maintains the location-specific attributes for each network site, including the network centers, buildings, floors, and rooms where the equipment is located.

 The network site records enable you to view all the equipment at a location. You can filter the locations by the assigned type, role, or function categories. To learn more, see [153f0911a5303dc2d91ba071cdb03271e0039fd3.dita](../task/define-tni-sites.md).

</td></tr><tr><td>

Equipment Holder \[cmdb\_ci\_equipment\_holder\]

</td><td>

Hardware \[cmdb\_ci\_hardware\]

</td><td>

Represents the physical units that contain the telecommunications equipment, including the cages, bays, cabinets, slots, and relay racks. An equipment holder can contain the other equipment holders. For example, the line-ups contain the individual relay racks and each relay rack contains the equipment shelves.

 Use the equipment holder records to track and manage your network assets. To learn more, see [994adcaad828f977d9cc3746ca467b88e162a370.dita](../task/define-tni-equipment-holders.md).

 To learn more about the extension classes of the equipment holder, see [Equipment holder extension classes](../reference/equipment-holder-types.md).

</td></tr><tr><td>

Telco Equipment \[cmdb\_ci\_ni\_telco\_equipment\]

</td><td>

Network gear \[cmdb\_ci\_netgear\]

</td><td>

Represents a device that provides the technical functionality in a network. Examples include the routers, modems, mobile devices, optical cables,relays, and switches. The equipment can have slots, cards, or ports. The equipment can exist within an equipment holder or by itself because not all equipment is rack mounted.

 Use the equipment record to track and manage the details of your telco equipment. To learn more, see

 [Create a telecommunications equipment instance](../task/define-equipment-type.md).To learn more about the equipment extension classes, see [Equipment extension classes](../reference/equipment-extension-classes.md).

</td></tr><tr><td>

Network Interface \[cmdb\_ci\_ni\_interface\]

</td><td>

Network Port \[cmdb\_ci\_ni\_network\_port\]

</td><td>

Captures and maintains the equipment-specific attributes for the network interfaces. To learn more, see [Define the network interface details](../task/define-tni-interfaces.md).

</td></tr><tr><td>

Interface Card \[cmdb\_ci\_interface\_card\]

</td><td>

Network gear \[cmdb\_ci\_netgear\]

</td><td>

Represents the interface cards that are stored in a network. Cards can occupy more than one slot and can contain other cards. They can be the equipment ports that are physical or logical \(virtual\). Each port is assigned a bandwidth value. The bandwidths are consumed when you use the ports in the network design.

 To learn more, see [Define the card details](../task/define-tni-interface-cards.md).

</td></tr><tr><td>

Physical Connection \[cmdb\_ci\_ni\_physical\_link\]

</td><td>

Network Link \[cmdb\_ci\_network\_link\]

</td><td>

Represents the physical port connections on the interface cards in your network. To learn more, see [Define the physical connection details](../task/define-tni-physical-connections.md).

</td></tr><tr><td>

Logical Connection \[cmdb\_ci\_ni\_logical\_path\]

</td><td>

Network Circuit \[cmdb\_ci\_network\_circuit\]

</td><td>

Represents the logical or virtual port connections on the network interface cards. A logical connection typically represents the multiple physical connections on an interface card.

 To learn more, see [Define the logical connection details](../task/define-tni-logical-connections.md).

</td></tr><tr><td>

Power Circuit \(cmdb\_ci\_circuit\)

</td><td>

Configuration Item \[cmdb\_ci\]

</td><td>

Represents the electrical pathway that delivers power in a data center. To learn more, see [Define the power circuit details](../task/define-power-circuit-details.md).

</td></tr><tr><td>

Topology \[cmdb\_ci\_topology\]

</td><td>

Network Topology \[cmdb\_ci\_network\_topology\]

</td><td>

Represents the grouping of the network elements such as nodes \(equipment\), edges \(connections\), and termination points \(interfaces\), how they are organized and connected to each other.

 To learn more, see [Network topology](visualization-of-topology.md).

</td></tr><tr><td>

Facility Hardware

</td><td>

 

</td><td>

Represent power, HVAC, network, and their connectivity in a data center.To learn more, see [Network inventory facility classes](../reference/network-inventory-facility-classes.md).

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Telecommunications Network Inventory](exploring-telecommunicatons-network-inventory.md)

**Related topics**  


[Network Inventory \(NI\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-network-inventory&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

