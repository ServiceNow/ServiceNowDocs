---
title: Manually creating and reviewing your network asset instances
description: A key function that you can perform in the network inventory workspace is to manually create your network assets and a digital model of your network in the Telecommunications Network Inventory application. With this information, you can provision new services, modify existing services, maintain the network, and plan the forecast for your network growth.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/creating-telecommunications-network-inventory.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Define inventory records, Use, Telecommunications Network Inventory]
---

# Manually creating and reviewing your network asset instances

A key function that you can perform in the network inventory workspace is to manually create your network assets and a digital model of your network in the Telecommunications Network Inventory application. With this information, you can provision new services, modify existing services, maintain the network, and plan the forecast for your network growth.

To manually create and to review your individual network inventory records, and define the relationships between each asset, you can easily access the appropriate forms from the workspace landing page. For example, you can select the **Interface cards** count in the Network entities by categories widget on the Network Inventory Workspace landing page to create an interface card instance.

**Note:** As an alternative to manually creating individual network asset instances, you can instead use a more automated, and potentially less labor-intensive method to do so. To learn more, see the following:

-   [Data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/uses-for-network-inventory-data.md)
-   [Manually creating and reviewing your network asset instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/creating-telecommunications-network-inventory.md)
-   [Create inventory models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/creating-your-inventory-models.md)
-   [Create inventory template for network asset instantiation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/preparing-inv-templates-network-asset-generation.md)
-   [Instantiating your network inventory by using design and assign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/instantiate-asset-using-template-relationship-model.md)

## Process

To manually create a comprehensive digital model of your telecommunications network, access the following forms from the Network Inventory Workspace landing page and the Lists view. To learn more, see [Reviewing and updating your network inventory with the Network Inventory Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/tni-workspace.md).

1.  In the Network Site or Data Center form, create the site records for the individual locations that house your network equipment. To learn more about network site, see [febcfe12194eeb91c09e3996e78edd4ed1efeb0b.dita](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-sites.md). To learn more about data centers, see [Define the datacenter details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-data-center-details.md).
2.  In the Telco Equipment form, create the individual network asset instances for your telecommunications equipment. To learn more, see [ee9363b19ca20d3f5503d82662539f1c1d1d3c8f.dita](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-equipment.md).
3.  In the Equipment Holder form, create the individual network asset instances for your equipment holders. To learn more, see [49fbb00d55deb1d629af60c609556de00b5cd94c.dita](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-equipment-holders.md).
4.  In the Interface Cards form, create the individual network asset instances for your interface cards. To learn more, see [Define the card details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-interface-cards.md).
5.  In the Network Interface form, create the individual network asset instances for your network interfaces. To learn more, see [Define the network interface details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-interfaces.md).
6.  In the Physical connection form, create the individual network asset instances for each physical or wired connection. To learn more, see [Define the physical connection details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-physical-connections.md).
7.  In the Logical connection form, create the individual network asset instances for each logical connection. To learn more, see [Define the logical connection details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-logical-connections.md).
8.  Create the logical and physical relationships between each asset in your network inventory.
9.  Define the numbering for your virtual local-area network \(VLAN\) or link aggregation group \(LAG\) connections in the Telecommunications Network Inventory application. To learn more, see [Define your inventory numbering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-inventory-numbers.md).

-   **[Define the network site details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-sites.md)**  
Review, update, or create your network site records in the Telecommunications Network Inventory application. These records enable you to view the location-specific attributes for each network site, including the network centers, buildings, floors, and rooms where your equipment is located.
-   **[Define the datacenter details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-data-center-details.md)**  
Define your datacenter record in the Telecommunications Network Inventory application. These records enable you to view the location-specific attributes for each datacenter, including the network centers, buildings, floors, and rooms where your network assets are located.
-   **[Define the facility hardware details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-facility-hardware-details.md)**  
Define the facility hardware record to represent power, thermal, network components and their connectivity in a datacenter. By defining the facility records, you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Create a telecommunications equipment instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-equipment-type.md)**  
Create a telecommunications equipment instance in your network. You define the equipment instances so that you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Define the equipment holders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-equipment-holders.md)**  
Define the equipment holder that contains your telecommunications equipment, including the cabinets, racks, shelves, and slots. By defining the equipment holders, you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Create and maintain racks and cabinets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-and-maintain-rack-and-cabinet.md)**  
Create and perform subsequent actions on the racks and cabinets using the Telecommunications Network Inventory application.
-   **[Create a slot for equipment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-a-slot.md)**  
Create a slot to provide a designated space for the equipment to maintain, update and access all types of equipment. You can route cables using the Telecommunications Network Inventory application.
-   **[Define the card details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-interface-cards.md)**  
Review, update, or create a network asset instance for a card that you use in your telecommunications equipment. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Define the network interface details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-interfaces.md)**  
Review, update, or create a network instance for a network interface that controls the signaling and management functions between your networks. You define these attributes so that you can track and manage your network instances in the Telecommunications Network Inventory application.
-   **[Define the cable details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-cable.md)**  
Review, update, or create a network asset instance for the cable connecting the various sites within your network. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Define the strand details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-strand.md)**  
Review, update, or create a network asset instance for a strand in the cable. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Define the physical connection details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-physical-connections.md)**  
Review update, or create a network asset instance for the physical port connection on the interface cards in your networks. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Define the logical connection details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-tni-logical-connections.md)**  
Review, update, or create a network asset instance for a logical or virtual port connection on your network interface cards. You define these attributes so that you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Define the power circuit details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-power-circuit-details.md)**  
Define the power circuit record to represent the electrical pathway that delivers power in a datacenter. By defining the power circuit records, you can track and manage your network assets in the Telecommunications Network Inventory application.
-   **[Manually create a network topology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-netowrk-topology.md)**  
Create a topology record for the network that you want to visualize in the organization of its network elements. By creating the network topology, you can visualize how the network elements are organized and connected to one another in the Telecommunications Network Inventory application.
-   **[Define your inventory groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-your-inventory-groups.md)**  
An inventory group is a collection of CIs that lets you apply CI actions collectively to all the CIs in Telecommunications Network Inventory application. By defining inventory groups, you can group different CIs, and apply actions to all CIs.
-   **[Decommission an inventory record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/decommision-an-inventory-record.md)**  
Decommission an inventory record that you want to remove from Telecommunications Network Inventory.

**Parent Topic:**[Reviewing and updating your network inventory with the Network Inventory Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/tni-workspace.md)

**Related topics**  


[Modeling your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-workflow.md)

