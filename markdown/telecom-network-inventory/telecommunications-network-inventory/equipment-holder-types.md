---
title: Equipment holder extension classes
description: The Equipment Holder extension classes are the sub-classes that are extended from the Equipment Holder. You can define equipment holder records for these classes in the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Equipment holder extension classes

The Equipment Holder extension classes are the sub-classes that are extended from the Equipment Holder. You can define equipment holder records for these classes in the Telecommunications Network Inventory application.

<table id="table_xhx_nvs_4xb"><thead><tr><th>

Class Name

</th><th>

Table Name

</th><th>

Extends from

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cabinet

</td><td>

cmdb\_ci\_container\_cabinet

</td><td>

cmdb\_ci\_equipment\_holder

</td><td>

A telecommunications cabinet, also known as a telecom cabinet or equipment cabinet, is a physical enclosure used to house and protect various telecommunications and network equipment, such as switches, routers, patch panels, and power supplies. It provides a secure and organized environment for the installation, management, and interconnection of telecommunications infrastructure within a network or data center.

</td></tr><tr><td>

Multi Rack

</td><td>

cmdb\_ci\_container\_multi\_rack

</td><td>

cmdb\_ci\_equipment\_holder

</td><td>

A multi-rack, also referred to as a multi-rack system or multi-rack enclosure, is a configuration consisting of multiple interconnected equipment racks used for housing and organizing a large amount of telecommunications or network equipment in a centralized manner. It provides expanded capacity and scalability, allowing for efficient deployment and management of equipment within data centers or telecommunication facilities.

</td></tr><tr><td>

Rack

</td><td>

cmdb\_ci\_container\_rack

</td><td>

cmdb\_ci\_equipment\_holder

</td><td>

A rack, commonly known as a server rack or equipment rack, is a framework designed to securely hold and organize various IT and telecommunications equipment, such as servers, networking devices, and storage units. It provides a standardized form factor for easy installation, organization, and maintenance of equipment in data centers and other technology environments.

</td></tr><tr><td>

Shelf

</td><td>

cmdb\_ci\_container\_shelf

</td><td>

cmdb\_ci\_equipment\_holder

</td><td>

A shelf holder, also known as a rack shelf or equipment shelf, is a component designed to support and hold non-rackmount equipment or devices within a rack or equipment cabinet. It provides a stable platform for equipment that does not have built-in rackmount capabilities, allowing for efficient organization and integration of various devices within the rack infrastructure.

</td></tr><tr><td>

Slot

</td><td>

cmdb\_ci\_container\_slot

</td><td>

cmdb\_ci\_equipment\_holder

</td><td>

In the context of technology and hardware, a slot refers to a physical or virtual receptacle designed to hold and accommodate a specific type of component, such as an expansion card or memory module. It provides a standardized interface and location for inserting and connecting the component to the main system or device.Dependent on Hardware \(contains::contained by\).

Name is usually discoverable. If not available,use the name of the card that is contained in this slot.

</td></tr><tr><td>

Subslot

</td><td>

cmdb\_ci\_container\_subslot

</td><td>

cmdb\_ci\_equipment\_holder

</td><td>

In our context, a slot that is present on a Card and can accommodate child cards is considered a subslot.Dependent on Hardware \(contains::contained by\).

Identification: Name \(100\). Name is discovered from SNMP. If not available, use the name of the card that is contained in this subslot.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[f8a0c756b1889baba153d09c4a88b726cfd7dedf.dita](../task/define-tni-equipment-holders.md)

