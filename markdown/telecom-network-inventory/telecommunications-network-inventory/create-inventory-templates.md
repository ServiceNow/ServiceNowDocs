---
title: Create an inventory template
description: Create an inventory template in the Telecommunications Network Inventory application to represent a configuration of the created inventory model.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Creating inventory template for network asset instantiation, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create an inventory template

Create an inventory template in the Telecommunications Network Inventory application to represent a configuration of the created inventory model.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, and sn\_ni\_core.inventory\_template\_manager

## About this task

A network inventory template contains a set of detailed business guidance rules from a telecommunications provider. These rules state how the equipment configurations should be generated, based on certain operating requirements. When you create an inventory template, it creates a template in the Inventory Templates \[sn\_ni\_core\_inventory\_template\] table. To learn more about inventory templates, see the following topics:

-   [Network inventory templates](../concept/using-templates-tni.md)
-   [Creating inventory template relationship](../concept/creating-inventory-templates-telco-equipment.md)

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Network Inventory Templates** &gt; **Inventory Templates**.

3.  Select **New**.

4.  On the **Details** tab, fill in the general information to create an inventory template.

    The following table lists the fields that are unique to the inventory template.

<table id="table_xxp_hq1_dtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Manufacturer-assigned name for this inventory template, as specified by the model manager.

</td></tr><tr><td>

Inventory model

</td><td>

List of all product models related to the Telecommunications Network Inventory. Select the search icon \(![Search icon.](../image/search.png)\) and select a model. To learn more, see [Creating your inventory models](../concept/creating-your-inventory-models.md).

</td></tr><tr><td>

Default field values

</td><td>

Default template where the default CI attribute values can be defined. The values in the list depend on the selected inventory model. Select the search icon \(![Search icon.](../image/search.png)\) and select a type code. To learn more, see [Create a default template](create-default-templates.md).

</td></tr><tr><td>

Version

</td><td>

Version of the template

</td></tr><tr><td>

Parent bandwidth

</td><td>

Bandwidth of the parent product model.**Note:** This attribute is only visible when you select a logical connection model and that has a relationship type as **Logical Connection to Channel**.

</td></tr><tr><td>

Child bandwidth

</td><td>

Bandwidth of the child product model.**Note:** This attribute is only visible when you select a logical connection model and that has a relationship type as **Logical Connection to Channel**.

</td></tr></tbody>
</table>5.  To add attachments, such as graphics or documents, select the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\).

6.  Select **Save**.

    The **Related Templates** tabs appear next to the **Details** tab where you can view, add, update, and delete the related templates. You can also add a related template under a related template.

    **Note:**

    1.  If you’ve defined the network model relationship between the rack and slot, equipment and slot, equipment and interface, interface card and slot, or interface card and interface,the slots and interfaces are automatically created under the **Related Templates** for the equipment or interface cards. Otherwise, manually add using **New**.
    2.  Add shelves/equipment to racks or shelves in the **Related Templates**tab of each created rack unit or slots. You can also add equipment to each shelf. To learn more, see [Related templates form](../reference/related-templates-form.md).
    3.  You can update the naming pattern of each template directly from the Name Pattern column under the related templates. The name pattern of the created slots or interfaces is fetched from the default pattern of the models. To learn more, see [Inventory Model form - Information](../reference/tni-model-form-information.md).
    4.  To add an interface card in a slot, navigate to **slot** &gt; **Related Templates** &gt; **New** and fill in the required details.

## What to do next

To delete a template, select the options icon \(![Options icon.](../image/options-icon.png)\), and then select **Delete**.

**Parent Topic:**[Creating inventory template for network asset instantiation](../concept/preparing-inv-templates-network-asset-generation.md)

