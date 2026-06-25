---
title: Add interface card templates to the slot templates
description: In the equipment inventory template that you created in the Network Inventory Workspace Lists view, use the Related Templates tab to add the interface cards to the selected slots.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/adding-interface-card-slots.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create inventory template relationship, Use, Telecommunications Network Inventory]
---

# Add interface card templates to the slot templates

In the equipment inventory template that you created in the Network Inventory Workspace Lists view, use the Related Templates tab to add the interface cards to the selected slots.

## Procedure

In the **Related Templates** tab, select the slot that you want to add the interface card to.

\[Omitted image "inventory-template-7450ESS1-slots.png"\] Alt text: Related Template view of the 7450 ESS-1 template with list of slots.

When the slot record appears, in the **Related Templates** tab, click **New**. Create an inventory template for the associated interface card.

\[Omitted image "inventory-template-card-compatibilities-ess.png"\] Alt text: Details view of associated interface card template with field information.

1.  In the **Name** field, enter a name for the interface card.
2.  In the **Inventory model** field, the associated network interface cards according to the specified slot-to-interface card model relationship. If there is an associated inventory model, you can select one as needed.

    When you submit the form, the interface appears in the **Related Templates** tab for the associated slot. If there are associated interface cards, repeat this procedure until you've paired all slots in the equipment template.


The following example shows the inventory template for the slot with an associated interface card.

\[Omitted image "inventory-template-network-slot1-card-compatibilites-ess.png"\] Alt text: Related Template view of slot 1 with the associated interface card.

If the card model has a Slot Occupied attribute, and its value is greater than 1, a **Slot Occupied** field appears on the form. It ensures that you are able to identify that when this card is instantiated, other slots are also attached it. By using this field, you can indicate if the other slots that are attached to that piece of equipment are compatible to the network interface that you are selecting.

## What's next

Next, add subslots to the network interface template. To learn more, see [Add subslot templates to the interface card template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/adding-subslots-network-interface-template.md).

**Parent Topic:**[Create inventory template relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/creating-inventory-templates-telco-equipment.md)

**Previous topic:**[Add a network interface to the equipment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/adding-interface-cards-associated-equipment-model.md)

**Next topic:**[Add subslot templates to the interface card template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/adding-subslots-network-interface-template.md)

**Related topics**  


[Create inventory template for network asset instantiation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/preparing-inv-templates-network-asset-generation.md)

