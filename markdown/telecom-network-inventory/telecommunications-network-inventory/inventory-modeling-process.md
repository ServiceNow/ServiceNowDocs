---
title: Model relationships
description: You model your network inventory relationships in the Telecommunications Network Inventory application so that you can use them in the inventory template relationships to create your network inventory records.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Model your workflow, Explore, Telecommunications Network Inventory]
---

# Model relationships

You model your network inventory relationships in the Telecommunications Network Inventory application so that you can use them in the inventory template relationships to create your network inventory records.

## Network model relationship overview

A model relationship captures the relationships between the inventory models. By defining the relationships between the various network model entities, you can also define the compatibility between these entities. The inventory template uses the model relationships to create template relationships. The instantiation process uses the inventory template relationships that you create when it generates the network inventory records. For example, when you create an equipment or card template, the associated slots and interface templates are automatically created by using the data from the model relationship. If the model relationships aren’t made, the system doesn't create the associated templates.

## Inventory modeling process

When you create inventory models for your equipment inventory in the Telecommunications Network Inventory application, you can use either a bottom-to-top or a top-to-bottom approach. Either sequence is acceptable, and both yield the same result when you finish:

-   Bottom-to-top approach, where the modeling starts when you navigate to **Network interface model** &gt; **Interface Card Model** &gt; **Slot Model** &gt; **Equipment Model** &gt; **Equipment Holder Model \(Rack\)**.
-   Top-to-bottom approach, where the modeling starts when you navigate to **Equipment Holder Model \(Rack\)** &gt; **Equipment Model** &gt; **Slot Model** &gt; **Interface Card model** &gt; **Network Interface model**.

The following diagram shows a top-to-bottom approach for the inventory modeling process.

![Top-to-bottom inventory modeling. For a text description, refer to the modeling steps that follow.](../image/inventory-modeling-process.png "Top-to-bottom inventory modeling")

The steps for top-to-bottom modeling of an inventory are as follows:

1.  Check for any available rack models.
2.  Check for any model relationships if a rack model is available. If not, create an equipment holder model of rack.
3.  Check for any equipment models.
4.  Check for any model relationships if an equipment model is available. If not, create an equipment model.
5.  Check for the interface card model.
6.  Check for any model relationships if an interface card model is available. If not, create an interface card model.
7.  Check for the network interface model.
8.  Check for any model relationships, if the network interface model is available. If not, create a network interface model.
9.  Check for the model relationships after you create each inventory model. If not, create the model relationships.

This process ensures that all models and model relationships are created according to the manufacturer's recommendations.

**Related topics**  


[Create inventory models](creating-your-inventory-models.md)

[Define a network model relationship](../task/create-network-model-relationships.md)

