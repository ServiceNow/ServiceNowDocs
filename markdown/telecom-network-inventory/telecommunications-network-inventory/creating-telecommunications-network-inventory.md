---
title: Manually create and review your network asset instances
description: A key function that you can perform in the network inventory workspace is to manually create your network assets and a digital model of your network in the Telecommunications Network Inventory application. With this information, you can provision new services, modify existing services, maintain the network, and plan the forecast for your network growth.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Defining inventory records, Use, Telecommunications Network Inventory]
---

# Manually create and review your network asset instances

A key function that you can perform in the network inventory workspace is to manually create your network assets and a digital model of your network in the Telecommunications Network Inventory application. With this information, you can provision new services, modify existing services, maintain the network, and plan the forecast for your network growth.

To manually create and to review your individual network inventory records, and define the relationships between each asset, you can easily access the appropriate forms from the workspace landing page. For example, you can select the **Interface cards** count in the Network entities by categories widget on the Network Inventory Workspace landing page to create an interface card instance.

**Note:** As an alternative to manually creating individual network asset instances, you can instead use a more automated, and potentially less labor-intensive method to do so. To learn more, see the following:

-   [Data model](uses-for-network-inventory-data.md)
-   [Manually create and review your network asset instances](creating-telecommunications-network-inventory.md)
-   [Create inventory models](creating-your-inventory-models.md)
-   [Create inventory template for network asset instantiation](preparing-inv-templates-network-asset-generation.md)
-   [Instantiating inventory using design and assign](instantiate-asset-using-template-relationship-model.md)

## Process

To manually create a comprehensive digital model of your telecommunications network, access the following forms from the Network Inventory Workspace landing page and the Lists view. To learn more, see [Reviewing and updating your network inventory with the Network Inventory Workspace](tni-workspace.md).

1.  In the Network Site or Data Center form, create the site records for the individual locations that house your network equipment. To learn more about network site, see [6ae017e0af7d4246ad6f9813addb0b7ccaa73376.dita](../task/define-tni-sites.md). To learn more about data centers, see [Define the datacenter details](../task/define-data-center-details.md).
2.  In the Telco Equipment form, create the individual network asset instances for your telecommunications equipment. To learn more, see [ba2dcf9259766c1056a6c37a7888bb630a54016d.dita](../task/define-tni-equipment.md).
3.  In the Equipment Holder form, create the individual network asset instances for your equipment holders. To learn more, see [f8a0c756b1889baba153d09c4a88b726cfd7dedf.dita](../task/define-tni-equipment-holders.md).
4.  In the Interface Cards form, create the individual network asset instances for your interface cards. To learn more, see [Define the card details](../task/define-tni-interface-cards.md).
5.  In the Network Interface form, create the individual network asset instances for your network interfaces. To learn more, see [Define the network interface details](../task/define-tni-interfaces.md).
6.  In the Physical connection form, create the individual network asset instances for each physical or wired connection. To learn more, see [Define the physical connection details](../task/define-tni-physical-connections.md).
7.  In the Logical connection form, create the individual network asset instances for each logical connection. To learn more, see [Define the logical connection details](../task/define-tni-logical-connections.md).
8.  Create the logical and physical relationships between each asset in your network inventory.
9.  Define the numbering for your virtual local-area network \(VLAN\) or link aggregation group \(LAG\) connections in the Telecommunications Network Inventory application. To learn more, see [Define your inventory numbering](../task/define-tni-inventory-numbers.md).

-   **[Define the network site details](../task/define-tni-sites.md)**  
Review, update, or create your network site records in the Telecommunications Network Inventory application. These records enable you to view the location-specific attributes for each network site, including the network centers, buildings, floors, and rooms where your equipment is located.
-   **[Define the datacenter details](../task/define-data-center-details.md)**  
Define your datacenter record in the Telecommunications Network Inventory application. These records enable you to view the location-specific attributes for each datacenter, including the network centers, buildings, floors, and rooms where your network assets are located.
-   **[Define the facility hardware details](../task/define-facility-hardware-details.md)**  
Define the facility hardware record to represent power, thermal, network components and their connectivity in a datacenter. By defining the facility records, you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Create a telecommunications equipment instance](../task/define-equipment-type.md)**  
Create a telecommunications equipment instance in your network. You define the equipment instances so that you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Define the equipment holders](../task/define-tni-equipment-holders.md)**  
Define the equipment holder that contains your telecommunications equipment, including the cabinets, racks, shelves, and slots. By defining the equipment holders, you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Create and maintain racks and cabinets](create-and-maintain-rack-and-cabinet.md)**  
Create and perform subsequent actions on the racks and cabinets using the Telecommunications Network Inventory application.
-   **[Create a slot for equipment](../task/create-a-slot.md)**  
Create a slot to provide a designated space for the equipment to maintain, update and access all types of equipment. You can route cables using the Telecommunications Network Inventory application.
-   **[Define the card details](../task/define-tni-interface-cards.md)**  
Review, update, or create a network asset instance for a card that you use in your telecommunications equipment. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Define the network interface details](../task/define-tni-interfaces.md)**  
Review, update, or create a network instance for a network interface that controls the signaling and management functions between your networks. You define these attributes so that you can track and manage your network instances in the Telecommunications Network Inventory application.
-   **[Define the cable details](../task/define-cable.md)**  
Review, update, or create a network asset instance for the cable connecting the various sites within your network. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Define the strand details](../task/define-strand.md)**  
Review, update, or create a network asset instance for a strand in the cable. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Define the physical connection details](../task/define-tni-physical-connections.md)**  
Review update, or create a network asset instance for the physical port connection on the interface cards in your networks. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Define the logical connection details](../task/define-tni-logical-connections.md)**  
Review, update, or create a network asset instance for a logical or virtual port connection on your network interface cards. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Define the power circuit details](../task/define-power-circuit-details.md)**  
Define the power circuit record to represent the electrical pathway that delivers power in a datacenter. By defining the power circuit records, you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Manually create a network topology](../task/create-netowrk-topology.md)**  
Create a topology record for the network that you want to visualize in the organization of its network elements. By creating the network topology, you can visualize how the network elements are organized and connected to one another in the Telecommunications Network Inventory application.
-   **[Define your inventory groups](../task/define-your-inventory-groups.md)**  
An inventory group is a collection of CIs that lets you apply CI actions collectively to all the CIs in Telecommunications Network Inventory application. By defining inventory groups, you can group different CIs, and apply actions to all CIs.
-   **[Decommission an inventory record](../task/decommision-an-inventory-record.md)**  
Decommission an inventory record that you want to remove from Telecommunications Network Inventory.

**Parent Topic:**[Reviewing and updating your network inventory with the Network Inventory Workspace](tni-workspace.md)

**Related topics**  


[Model your workflow](telecommunications-network-inventory-workflow.md)

