---
title: Add interface card templates to the slot templates
description: In the equipment inventory template that you created in the Network Inventory Workspace Lists view, use the Related Templates tab to add the interface cards to the selected slots.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create inventory template relationship, Use, Telecommunications Network Inventory]
---

# Add interface card templates to the slot templates

In the equipment inventory template that you created in the Network Inventory Workspace Lists view, use the Related Templates tab to add the interface cards to the selected slots.

## Procedure

In the **Related Templates** tab, select the slot that you want to add the interface card to.

![Related Template view of the 7450 ESS-1 template with list of slots.](../image/inventory-template-7450ESS1-slots.png "Equipment inventory template with all associated slots")

When the slot record appears, in the **Related Templates** tab, click **New**. Create an inventory template for the associated interface card.

![Details view of associated interface card template with field information.](../image/inventory-template-card-compatibilities-ess.png "Inventory template for the associated interface card")

1.  In the **Name** field, enter a name for the interface card.
2.  In the **Inventory model** field, the associated network interface cards according to the specified slot-to-interface card model relationship. If there is an associated inventory model, you can select one as needed.

    When you submit the form, the interface appears in the **Related Templates** tab for the associated slot. If there are associated interface cards, repeat this procedure until you've paired all slots in the equipment template.


The following example shows the inventory template for the slot with an associated interface card.

![Related Template view of slot 1 with the associated interface card.](../image/inventory-template-network-slot1-card-compatibilites-ess.png "Slot with associated interface card")

If the card model has a Slot Occupied attribute, and its value is greater than 1, a **Slot Occupied** field appears on the form. It ensures that you are able to identify that when this card is instantiated, other slots are also attached it. By using this field, you can indicate if the other slots that are attached to that piece of equipment are compatible to the network interface that you are selecting.

## What's next

Next, add subslots to the network interface template. To learn more, see [Add subslot templates to the interface card template](adding-subslots-network-interface-template.md).

**Parent Topic:**[Create inventory template relationship](creating-inventory-templates-telco-equipment.md)

**Previous topic:**[Add a network interface to the equipment template](adding-interface-cards-associated-equipment-model.md)

**Next topic:**[Add subslot templates to the interface card template](adding-subslots-network-interface-template.md)

**Related topics**  


[Create inventory template for network asset instantiation](preparing-inv-templates-network-asset-generation.md)

