---
title: Create inventory models
description: As an inventory catalog manager, you can use a series of forms to define the metadata for each network model in the Telecommunications Network Inventory. During this process, you also specify the relationships between each of these models.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use, Telecommunications Network Inventory]
---

# Create inventory models

As an inventory catalog manager, you can use a series of forms to define the metadata for each network model in the Telecommunications Network Inventory. During this process, you also specify the relationships between each of these models.

## Inventory models overview

The metadata that you define in an inventory model serves an important purpose when you create an associated template or instantiate an instance of equipment. It ensures that you adhere to the validations put in place by the equipment vendor so that you don’t create a non-supported piece of equipment.

-   The metadata that the inventory models contain, such as the name, model number, height, and depth, remain consistent across all individual instances of that particular type of equipment.
-   When you generate the equipment instances for an inventory model, they all contain this standard manufacturer information.

**Note:** To learn more about creating templates and generating network assets from your model and template records, see

-   [Create inventory template for network asset instantiation](preparing-inv-templates-network-asset-generation.md)
-   [Instantiating your network inventory by using design and assign](instantiate-asset-using-template-relationship-model.md)

To create a comprehensive digital model of your telecommunications network, do the following tasks:

1.  In the Equipment Model form, create inventory models for your telecommunications equipment.
    -   Creating an equipment inventory model is the first requirement for setting up the process to generate network asset instances when using inventory templates.
    -   You create an equipment model record every time a vendor or original equipment manufacturer \(OEM\) introduces new equipment for your use. To learn more, see [Create an equipment model](../task/create-equipment-models.md).
2.  In the Equipment Holder Model form, create the inventory model records for your equipment holders. To learn more, see [Create an equipment holder model](../task/create-equipment-holder-models.md).
3.  In the Network Interface Model form, create the inventory model records for your network interfaces. To learn more, see [Create a card model](../task/create-interface-card-models.md).
4.  In the Interface Cards Model form, create the inventory model records for your network interface cards. To learn more, see [Create a network interface model](../task/create-network-interface-model.md).
5.  In the Physical Connection Model form, create the inventory model records for each physical or wired connection. To learn more, see [Create a physical connection model](../task/create-physical-connection-models.md).
6.  In the Logical Connection Model form, create inventory model records for each logical connection. To learn more, see [Create a logical connection model](../task/create-logical-connection-models.md).
7.  In the Network Model Relationship form, define the relationships between each model record in your network inventory. To learn more, see [Define a network model relationship](../task/create-network-model-relationships.md).

## Inventory model related tabs

After you create inventory models, the information in the following table appears on these tabs in each inventory model record.

<table id="table_ahq_ww4_jtb"><thead><tr><th>

Tab

</th><th>

Contains

</th></tr></thead><tbody><tr><td>

Bandwidth Capabilities

</td><td>

Relation between the bandwidth and the physical and logical connection models that need to be added.**Note:** The **Bandwidth Capabilities** tab is available only on the physical and logical models.

</td></tr><tr><td>

Assets

</td><td>

Network asset information.

</td></tr><tr><td>

Configuration Items

</td><td>

Configuration Item \(CI\) that is associated with the model.

</td></tr><tr><td>

Model Components

</td><td>

Components in the model.

</td></tr><tr><td>

Vendor Catalog Items

</td><td>

Available network assets from various vendors.

</td></tr><tr><td>

Hardware Model Lifecycles

</td><td>

Life cycle information about the network asset.

</td></tr><tr><td>

Network Model Relationships

</td><td>

Related network inventory models.

</td></tr></tbody>
</table>-   **[Create a facility model](../task/create-facility-model.md)**  
Create a facility model in the Telecommunications Network Inventory application to define the physical characteristics data of the facility record according to the product manufacturer's recommendations.
-   **[Create an equipment model](../task/create-equipment-models.md)**  
Create an equipment model in the Telecommunications Network Inventory application as the first requirement for setting up the process to generate your network asset instances. You create an equipment model record every time a vendor or original equipment manufacturer \(OEM\) introduces new equipment for your use.
-   **[Create an equipment holder model](../task/create-equipment-holder-models.md)**  
Create an equipment holder model in the Telecommunications Network Inventory application to define the physical characteristics data of the equipment holder according to the product manufacturer's recommendations. You create an equipment holder model every time a vendor or original equipment manufacturer \(OEM\) introduces a new equipment holder for your use.
-   **[Create a card model](../task/create-interface-card-models.md)**  
Create a card model in the Telecommunications Network Inventory application to define the physical characteristics data of the card as per the product manufacturer's recommendations.
-   **[Create a network interface model](../task/create-network-interface-model.md)**  
Create a network interface model in the Telecommunications Network Inventory application to define the physical characteristics data of the network interface as per the product recommendations of the manufacturer.
-   **[Create a cable model](../task/create-a-cable-model.md)**  
Create a cable model in the Telecommunications Network Inventory application to define the physical characteristics data of the cable according to the product recommendations of the manufacturer.
-   **[Create a strand model](../task/create-a-strand-model.md)**  
Create a strand model in the Telecommunications Network Inventory application to define the physical characteristics data of the strand according to the product recommendations of the manufacturer.
-   **[Create a physical connection model](../task/create-physical-connection-models.md)**  
Create a physical connection model in the Telecommunications Network Inventory application to define the metadata for the different physical connections. In the physical connection model, you can import models, attach a file or an image, add or remove optional fields, and add compatibilities and substitutions.
-   **[Create a logical connection model](../task/create-logical-connection-models.md)**  
Create a logical connection model in the ServiceNow Telecommunications Network Inventory application to define the metadata for the different logical connections. In the logical connection model, you can import models, attach a file or an image, add or remove optional fields, and add compatibilities and substitutions.
-   **[Create a network topology model](create-network-topology-model.md)**  
Create a network topology model in the Telecommunications Network Inventory application to define the metadata for the topology according to your recommendations. You can use a topology model to create a record by using the design and assign function.
-   **[Define a network model relationship](../task/create-network-model-relationships.md)**  
Create a network model relationship in the Telecommunications Network Inventory application that captures the relationships between your network model entities.

**Parent Topic:**[Using Telecommunications Network Inventory](using-telecom-network-inventory.md)

**Related topics**  


[Network inventory models](using-inventory-models-tni.md)

