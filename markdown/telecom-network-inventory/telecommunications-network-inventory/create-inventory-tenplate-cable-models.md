---
title: Create an inventory template for cable models
description: Create an inventory template for the cable models in the Telecommunications Network Inventory application. You can use this template to instantiate a cable record and related stand records.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create inventory template relationship, Use, Telecommunications Network Inventory]
---

# Create an inventory template for cable models

Create an inventory template for the cable models in the Telecommunications Network Inventory application. You can use this template to instantiate a cable record and related stand records.

## Use case

The following example shows an inventory template for a cable model.

![Details view of a cable template with field information.](../image/cable-template.png "Inventory template for the card model")

After saving the inventory record, it creates the related strand templates depending on the count mentioned in the network model relationship.

![Related template view of ta cable template with field information.](../image/cable-template-related-template.png "Related strand templates of a cable template")

The default naming pattern of a strand record is "Strand-+position". You can edit the **Name Pattern** field.

![Details view of a strand template with field information.](../image/strand-template.png "Details of a strand template")

## What's next

Use a cable template to instantiate cable and strand records using design and assign. To learn more, see [Create a cable record by using design and assign](../task/create-cable-record-using-design-assign.md).

**Parent Topic:**[Create inventory template relationship](creating-inventory-templates-telco-equipment.md)

**Previous topic:**[Add a network interface template to a child or daughter card template](adding-network-interface-template-child-daughter-card.md)

**Next topic:**[Create an inventory template for a logical composite](creating-inventory-template-logical-composite.md)

**Related topics**  


[Create a cable model](../task/create-a-cable-model.md)

[Network inventory templates](using-templates-tni.md)

[Model your workflow](telecommunications-network-inventory-workflow.md)

