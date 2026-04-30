---
title: Network Model Relationship fields
description: The Network Model Relationship form enables you to create a network model relationship.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Network Model Relationship fields

The Network Model Relationship form enables you to create a network model relationship.

<table id="table_xxp_hq1_dtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Manufacturer-assigned name of the network model relationship that is specified by the model manager.

</td></tr><tr><td>

Relationship type

</td><td>

Type of relationship. Select one of the following options:-   **--None--**

No network model relationship exists.

-   **Rack to Rack Slot**

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
-   **Slot to Card**

Relationship between a slot model and an interface card model. This relationship enforces the **Root product model** field where an equipment model or a card model should be selected.

**Note:**

    -   The **Root product model** field shows a list of all the equipment models related to the Telecommunications Network Inventory application.
    -   The **Parent product model** field shows the models of both the slots and subslots.
    -   The **Child product model** field shows a list of all the interface card models.
-   **Card to Slot**

Relationship between an interface card model and a slot model. This relationship indicates that the slot model is compatible with the interface card model.

**Note:**

    -   The **Parent product model** field shows a list of all the interface card models.
    -   The **Child product model** field shows only the models of the subslots.
-   **Card to Network interface**

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
-   **Rack/Cabinet to Rack/Cabinet Slot**

Reltionship between rack/cabinet and rack/cabinet slot.

**Note:**

    -   The **Parent product model** field shows a list of all the racks and cabinets.
    -   The **Child product model** field shows a list of all the slots and sub-slots.
-   **Rack/Cabinet Slot to Equipment**

Relationship between a rack slot and the equipment.

**Note:**

    -   The **Root product model** shows all equipment holder models having **Model category** as **Rack**.
    -   The **Parent product model** shows all equipment holder models having **Model category** as **Slot**.
    -   The **Child product model** shows all equipment models related to the Telecommunications Network Inventory application.
-   **Rack/Cabinet Slot to Container Shelf**

Relationship between a rack slot and the shelf.

**Note:**

    -   The **Root product model** shows all equipment holder models having **Model category** as **Rack**.
    -   The **Parent product model** shows all equipment holder models having **Model category** as **Slot**.
    -   The **Child product model** shows all equipment holder models that have **Model category** as **Shelf**.
-   **Interface to Interface**

Relationship between two interfaces.

**Note:** The **Parent product model** and **Child product model** field shows list of all the network interface models.

-   **Cabinet to Equipment**

Relationship between a cabinet and the equipment.

**Note:**

The **Child product model** field shows all equipment models related to the Telecommunications Network Inventory application.

-   **Logical Connection to Channel**

Relationship between a logical connection and the channel.

**Note:**

    -   The **Parent product model** field shows a list of all the logical connection models.
    -   The **Child product model** field shows a list of all the logical connection models that have **Behaviour** as **Channel**.
-   **Cable to Strand**

Relationship between a cable and the strand.

**Note:**

    -   The **Parent product model** field shows a list of all the cable models.
    -   The **Child product model** field shows a list of all the strand models.

</td></tr><tr><td>

Count

</td><td>

Numbers of child product models that can be created under a parent product model when a template is created.**Note:** This attribute is only for **Equipment to Slot**, **Rack to Slot**, **Equipment to Network Interface**, **Interface card to Slot**, **Interface card to Network Interface**, **Cable to Strand**, and **Logical Connection to Channel** relationship types.

</td></tr><tr><td>

Root product model

</td><td>

Grandparent model of the interface card for compatibility. Either select the equipment model or the interface card model. Then, select the search icon \(![Search icon.](../image/search.png)\) and select a model. **Note:** This attribute is only visible for the **Slot to Interface card** relationship type.

</td></tr><tr><td>

Parent product model

</td><td>

Product model that is the parent to the child product model. Select the search icon \(![Search icon.](../image/search.png)\) and select a model.**Note:** In the Rack-to-Slot relationship, the parent product model is the equipment holder model with the model category as Rack.

</td></tr><tr><td>

Child product model

</td><td>

Product model that is the child to the parent product model. Select the search icon \(![Search icon.](../image/search.png)\) and select a model.**Note:** In the Rack to Slot relationship, the child product model is the equipment holder with model category as Slot.

</td></tr><tr><td>

Sequence

</td><td>

Sequence number of the child entities for a model relationship. If you enter a number in the **Count** field, the **Sequence** field appears.

 The default value is 1. If the parent model has multiple relationships, the sequence number for the first relationship is set to 1 and the number following the highest value of the first relationship is set for the consecutive relationships. For example, let's say that your equipment has a model relationship with two slots and two ports. When the relationship is created, the sequence number of the slots and ports are set to 1 and 3.

 **Note:** This attribute is only for **Rack to Slot**, **Equipment to Slot**, **Equipment to Network Interface**, **Interface card to Slot**, **Interface card to Network Interface**, **Cable to Strand**, and **Logical Connection to Channel** relationship types.

</td></tr><tr><td>

Parent bandwidth

</td><td>

Bandwidth of the parent product model.**Note:** This attribute is only visible for the **Logical Connection to Channel** relationship type.

</td></tr><tr><td>

Child bandwidth

</td><td>

Bandwidth of the child product model.**Note:** This attribute is only visible for the **Logical Connection to Channel** relationship type.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Define a network model relationship](../task/create-network-model-relationships.md)

