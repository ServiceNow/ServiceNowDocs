---
title: Create an inventory template for a logical composite
description: Create an inventory template for the logical composite in the Telecommunications Network Inventory application. You can use this template to instantiate a logical composite record and its related equipment and rack records.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create inventory template relationship, Use, Telecommunications Network Inventory]
---

# Create an inventory template for a logical composite

Create an inventory template for the logical composite in the Telecommunications Network Inventory application. You can use this template to instantiate a logical composite record and its related equipment and rack records.

## Use case

The following example shows an inventory template for a logical composite.

![Details view of a logical composite template with field information.](../image/logical-composite-template.png "Inventory template for a logical composite")

The inventory model has inventory relationships such as **Multi Chassis to Equipment** and **Multi Chassis to Rack** attached to it.

![Details of the network relationship with field information.](../image/logical-composite-model-relationship.png "Example of the network relationship")

After saving the inventory template, it creates the related equipment and rack templates depending on the count mentioned in the network model relationship.

![Related template view of the logical composite template with list information.](../image/logical-composite-related-template-view.png "Related templates of a logical composite template")

![Details view of a related template with field information.](../image/related-template-logical-composite.png "Details of a logical composite related template")

The default naming patterns of slot, subslot, and port records that are created under the equipment are as follows:

|Inventory record|Naming pattern|
|----------------|--------------|
|Slot|"slot-”+"chassis\_position+”/“+position"|
|Subslot|"subslot-”+"chassis\_position+”/“+equipment\_slot\_position+”/“+position"|
|Port|"port-”+chassis\_position+”/“+equipment\_slot\_position+”/“+parent\_slot\_position+”/“+position"|

You can edit the **Name Pattern** field.

## What's next

Use a this template to instantiate logical composites and related equipment and rack records using design and assign. To learn more, see [Create an equipment record by using design and assign](../task/create-equipment-record-design-and-assign.md).

**Parent Topic:**[Create inventory template relationship](creating-inventory-templates-telco-equipment.md)

**Previous topic:**[Create an inventory template for cable models](create-inventory-tenplate-cable-models.md)

**Next topic:**[Import models and templates](import-models-and-templates.md)

**Related topics**  


[Define a network model relationship](../task/create-network-model-relationships.md)

[Create an equipment record by using design and assign](../task/create-equipment-record-design-and-assign.md)

[Equipment extension classes](../reference/equipment-extension-classes.md)

