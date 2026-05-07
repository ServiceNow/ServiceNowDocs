---
title: Network inventory models
description: You define an inventory model in the Telecommunications Network Inventory application so that you can track the technical information from the manufacturer about a network asset such as the telco equipment or a network interface.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Modeling your workflow, Explore, Telecommunications Network Inventory]
---

# Network inventory models

You define an inventory model in the Telecommunications Network Inventory application so that you can track the technical information from the manufacturer about a network asset such as the telco equipment or a network interface.

## Inventory models overview

A network inventory model contains the assets, services, and the relationships that define the infrastructure of your telecommunications networks. An inventory model contains the metadata for the name, number, dimensions, compatible interface cards, and configurations from the manufacturer. When you instantiate an inventory record by using the design and assign function, your inventory record contains this standard manufacturer information. To learn more about how to create an inventory model record, see [Create inventory models](creating-your-inventory-models.md).

After you create the inventory models, you can then define the relationships between the various network model entities. You can also define the compatibility between these entities. To learn more about model relationships, see [Network model relationships](using-inventory-models-tni.md#section_yps_kn2_cyb).

## Types of inventory models

You can create the following types of inventory models:

-   **Facility Models**

    A network interface model captures the physical characteristics and data about the behavior of a facility hardware, as designated by the product manufacturer. Facility hardware represents the power, HVAC, network, and their connectivity in a data center.

-   **Equipment Models**

    An equipment model represents the metadata that is provided by a vendor or manufacturer for the equipment. It defines the consistent characteristics across the various instances that are created for the equipment. An instance is an individual occurrence of a network asset at a site or datacenter. To learn more, see [Create an equipment model](../task/create-equipment-models.md).

-   **Equipment holder models**

    An equipment holder model represents the metadata for the representation of containers, including the bays, cabinets, cages, line ups, relay racks, and slots. A **Container Type** field refers to the type of container that the equipment model represents To learn more, see [Create an equipment holder model](../task/create-equipment-holder-models.md).

    The modeling guidelines for the slots vary according to the telecommunications service provider. The individual slot models are represented by the types of slots. Examples are a route processor slot, power slot, fan slot, or a generic slot model.. To learn more, see [Create an equipment holder model](../task/create-equipment-holder-models.md).

-   **Interface card models**

    A card model defines the card's metadata, which are the attributes that are consistent across the various instantiated cards of that model.. To learn more, see [Create a card model](../task/create-interface-card-models.md).

-   **Network interface models**

    A network interface model captures the physical characteristics and data about the behavior of a network interface, as designated by the product manufacturer. To learn more, see [Create a network interface model](../task/create-network-interface-model.md).

-   **Physical connection model**

    A physical connection model captures the metadata for the physical connection. To learn more, see [Create a physical connection model](../task/create-physical-connection-models.md).

-   **Logical connection model**

    A logical connection model captures the metadata for the logical connections. To learn more, see [Create a logical connection model](../task/create-logical-connection-models.md).

-   **Cable model**

    A cable model captures the metadata for the cable. To learn more, see [Create a cable model](../task/create-a-cable-model.md).

-   **Strand model**

    A strand model captures the metadata for the strand. To learn more, see [Create a strand model](../task/create-a-strand-model.md).

-   **Network topology model**

    A network topology model captures the metadata for the topology. To learn more, see [Create a network topology model](create-network-topology-model.md).


## Network model relationships

A model relationship captures the relationships between the inventory models. By defining the relationships between the various network model entities, you can also define the compatibility between these entities.

When setting up model relationships, you select one of the following options in the **Relationship Type** field:

-   **--None--**

    No network model relationship exists.

-   **Rack to Slot**

    Relationship between a rack model and a slot model. This relationship indicates that the rack and the slot models are compatible with the equipment model.

-   **Equipment to Slot**

    Relationship between an equipment model and a slot model. This relationship indicates that the number of slots and the slot models are compatible with the equipment model.

    **Note:**

    -   The **Parent product model** field shows a list of all the equipment models related to the Telecommunications Network Inventory application.
    -   The **Child product model** field shows only the slot models.
-   **Equipment to Network interface**

    Relationship between an equipment model and a network interface model. This relationship indicates the interface model and the number of interfaces that are compatible and supported with the equipment model.

    **Note:**

    -   The **Parent product model** field shows a list of all the equipment models related to the Telecommunications Network Inventory application.
    -   The **Child product model** field shows a list of all the network interface models related to the Telecommunications Network Inventory application.
-   **Slot to Interface Card**

    Relationship between a slot model and an interface card model. This relationship enforces the **Root product model** field where an equipment model or a card model should be selected.

    **Note:**

    -   The **Root product model** field shows a list of all the equipment models related to the Telecommunications Network Inventory application.
    -   The **Parent product model** field shows the models of both the slots and subslots.
    -   The **Child product model** field shows a list of all the interface card models.
-   **Interface card to Slot**

    Relationship between an interface card model and a slot model. This relationship indicates that the slot model is compatible with the interface card model.

    **Note:**

    -   The **Parent product model** field shows a list of all the interface card models.
    -   The **Child product model** field shows only the models of the subslots.
-   **Interface Card to Network interface**

    Relationship between an interface card model and a network interface model. This relationship indicates that the number of interfaces in the network interface model are compatible with the interface card model.

    **Note:**

    -   The **Parent product model** field shows a list of all the interface card models.
    -   The **Child product model** field shows a list of all the network interface models.
-   **Physical Connection to Logical Connection**

    Relationship between the models of a physical connection to a logical connection.

    **Note:**

    -   The **Parent product model** field shows a list of all the physical connection models.
    -   The **Child product model** field shows a list of all the logical connection models.
-   **Logical Connection to Logical Connection**

    Relationship between one logical connection model to another logical connection model.

    **Note:**

    -   The **Parent product model** field shows a list of all the logical connection models.
    -   The **Child product model** field shows a list of all the logical connection models.
-   **Physical Connection to Network Interface**

    Relationship between a physical connection to a network interface.

    **Note:**

    -   The **Parent product model** field shows a list of all the physical connection models.
    -   The **Child product model** field shows a list of all the network interface models.
-   **Logical Connection to Network Interface**

    Relationship between a logical connection to a network interface.

    **Note:**

    -   The **Parent product model** field shows a list of all the logical connection models.
    -   The **Child product model** field shows a list of all the network interface models.
-   **Rack to Equipment**

    Relationship between a rack and the equipment.

    **Note:**

    -   The **Parent product model** field shows all equipment holders that have **Container type** as **Rack**.
    -   The **Child product model** field shows all equipment models related to the Telecommunications Network Inventory application.
-   **Cabinet to Equipment**

    Relationship between a cabinet and the equipment.

    **Note:**

    -   The **Parent product model** field shows all equipment holders that have **Container type** as **Cabinet**.
    -   The **Child product model** field shows all equipment models related to the Telecommunications Network Inventory application.
-   **Logical Connection to Channel**

    Relationship between a logical connection and the channel.

    **Note:**

    -   The **Parent product model** field shows a list of all the logical connection models.
    -   The **Child product model** field shows a list of all the channel models that have **Behaviour** as **Channel**.

To learn more about how to model your network inventory relationships, see [Model relationships](inventory-modeling-process.md).

## Accessing Inventory Model forms

You can access the inventory model forms in the Inventory Models node in the Network Inventory Workspace List view.

