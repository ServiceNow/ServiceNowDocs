---
title: Add slots to the equipment inventory template
description: In the equipment inventory template that you created in the Network Inventory Workspace Lists view, use the Related Templates tab to create the associations for the slots. The following example shows how you add a related inventory template for an equipment model.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create inventory template relationship, Use, Telecommunications Network Inventory]
---

# Add slots to the equipment inventory template

In the equipment inventory template that you created in the Network Inventory Workspace Lists view, use the Related Templates tab to create the associations for the slots. The following example shows how you add a related inventory template for an equipment model.

## Procedure

1.  In the **Related Templates** tab, click **New**.

    ![Related Template view of the 7450 ESS-1 template.](../image/inventory-template-750ESS1-template-related-templates-new.png "Equipment model inventory template - related templates")

2.  In the **Name** field, enter a unique name for the slot. When you generate a network asset instance, the generation process assigns this name to the slot.
3.  In the **Inventory model** field, the equipment holder model that is associated with this equipment inventory template appears. If there is no existing relationship with an equipment holder relationship, you can select any slot model as needed.

    **Note:** While it appears that inventory templates are created for the slots that are attached to the **Related Templates** tab, only the default template values are created and stored for them. The records created for them are not considered formal inventory templates but are flagged internally with an attribute of Template=N.


![Details view of slot-1 template with field information.](../image/inventory-template-slot1.png "Adding an interface card to a slot")

After you create all the associated slots, they all appear in the **Related Templates** tab.

![Related Template view of the 7450 ESS-1 template with the list of associated slots. For the text description, refer to the information that follows.](../image/inventory-template-7450ESS1-slots.png "Equipment inventory template with all associated slots")

**Note:** If there are no inventory templates for the slots, you select a default template in the **Default Field Values** field to set the default attributes for the assigned slots.

## What's next

Next, add a network interface to the equipment template. To learn more, see [Add a network interface to the equipment template](adding-interface-cards-associated-equipment-model.md).

**Parent Topic:**[Create inventory template relationship](creating-inventory-templates-telco-equipment.md)

**Previous topic:**[Create inventory templates for related network interface models](creating-inventory-templates-related-network-interface-models.md)

**Next topic:**[Add a network interface to the equipment template](adding-interface-cards-associated-equipment-model.md)

**Related topics**  


[Create inventory template for network asset instantiation](preparing-inv-templates-network-asset-generation.md)

