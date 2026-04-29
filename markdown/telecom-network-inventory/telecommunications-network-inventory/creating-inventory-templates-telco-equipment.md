---
title: Create inventory template relationship
description: Use this sequence as a guide when creating inventory templates for your equipment and establishing the proper template relationships in the Telecommunications Network Inventory application.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use, Telecommunications Network Inventory]
---

# Create inventory template relationship

Use this sequence as a guide when creating inventory templates for your equipment and establishing the proper template relationships in the Telecommunications Network Inventory application.

## Sequence for creating template relationships

Equipment instantiation, or the task of generating network asset instances from the inventory template relationships that you create, is a key function in the Telecommunications Network Inventory application. To operate properly, it depends on you creating accurate inventory models, default templates, and inventory templates, in a certain sequence, to establish proper equipment relationships.

**Note:** To learn more about equipment instantiation, see [Design and assign](telecommunications-circuit-design-resource-assignment.md).

When you create an equipment or card template, the associated slots and interface templates are automatically created by using the data from the model relationship. If the model relationships aren’t made, it doesn't create the associated templates. In this case, you must create the templates manually. To learn more about the model relationship, see [Create inventory template for network asset instantiation](preparing-inv-templates-network-asset-generation.md). For example, when you create a template for an equipment model, the associated templates, such as the Telco equipment holder \(slot\) and interface, are automatically created.

The names for these associated templates are mapped from the **Slot naming pattern** or **Interface naming pattern** fields in the **Information** tab of the Equipment Model or Interface Model forms.

-   To learn more about the **Slot naming pattern** or **Interface naming pattern** fields, see [Inventory Model form - Information](../reference/tni-model-form-information.md).
-   To learn more about the naming convention, see [Naming convention for associated templates](../reference/name-convention-templates.md).

To establish the proper relationships between these elements for your equipment, perform these tasks in the following order.

## Establishing a default template

The first step in this process is to create an appropriate default template for use in your inventory template relationship sequence.

Default templates capture the default attribute values for a configuration item \(CI\) class. A template defines the set of attribute values for any resource \(equipment, card, and so on\). When this default template is associated with an inventory template, it adds these attribute values to the resource that is instantiated using that template.

To learn more, see [Create a default template](../task/create-default-templates.md).

## What's next

After establishing a default template, begin the sequence by creating an inventory template for the equipment model. To learn more, see [Create an inventory template for the equipment model](creating-an-inventory-template-for-the-equipment-model.md).

1.  [Create an inventory template for the equipment model](creating-an-inventory-template-for-the-equipment-model.md)  
In the Inventory Template form in the Network Inventory Workspace Lists view, you can create an inventory template for the equipment model.
2.  [Create inventory templates for related interface card models](creating-inventory-templates-for-related-interface-card-models.md)  
In the Inventory Template form in the Network Inventory Workspace Lists view, you can create inventory templates for the interface card models that are associated with the equipment inventory template.
3.  [Create inventory templates for related network interface models](creating-inventory-templates-related-network-interface-models.md)  
In the Inventory Template form in the Network Inventory Workspace Lists view, you can create inventory templates for the network interface models that are associated with the equipment inventory template.
4.  [Add slots to the equipment inventory template](adding-slot-equipment-model.md)  
In the equipment inventory template that you created in the Network Inventory Workspace Lists view, use the Related Templates tab to create the associations for the slots. The following example shows how you add a related inventory template for an equipment model.
5.  [Add a network interface to the equipment template](adding-interface-cards-associated-equipment-model.md)  
In the equipment inventory template that you created in the Network Inventory Workspace Lists view, use the Related Templates tab to add the associated network interface.
6.  [Add interface card templates to the slot templates](adding-interface-card-slots.md)  
In the equipment inventory template that you created in the Network Inventory Workspace Lists view, use the Related Templates tab to add the interface cards to the selected slots.
7.  [Add subslot templates to the interface card template](adding-subslots-network-interface-template.md)  
In the Inventory Template form in the Network Inventory Workspace Lists view, you can add subslots to the interface card template that you created. You perform this procedure any time that you add a new card model to an existing equipment inventory template.
8.  [Add a network interface template to an interface card template](adding-interfaces-interface-card-template.md)  
If the interface card supports network interfaces directly to it, create an interface template relationship between the two interfaces in the Network Inventory Workspace Lists view.
9.  [Add an interface card template to the subslot templates](adding-interface-card-sub-slots.md)  
Add an interface card to the subslots that are associated with a piece of equipment in the Network Inventory Workspace Lists view.
10. [Add a network interface template to a child or daughter card template](adding-network-interface-template-child-daughter-card.md)  
As a last step, you can optionally add a network interface template to a child and daughter card template in the Network Inventory Workspace Lists view.
11. [Create an inventory template for cable models](create-inventory-tenplate-cable-models.md)  
Create an inventory template for the cable models in the Telecommunications Network Inventory application. You can use this template to instantiate a cable record and related stand records.
12. [Create an inventory template for a logical composite](creating-inventory-template-logical-composite.md)  
Create an inventory template for the logical composite in the Telecommunications Network Inventory application. You can use this template to instantiate a logical composite record and its related equipment and rack records.

**Parent Topic:**[Using Telecommunications Network Inventory](using-telecom-network-inventory.md)

**Related topics**  


[Create inventory template for network asset instantiation](preparing-inv-templates-network-asset-generation.md)

