---
title: Define a network model relationship
description: Create a network model relationship in the Telecommunications Network Inventory application that captures the relationships between your network model entities.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create inventory models, Use, Telecommunications Network Inventory]
---

# Define a network model relationship

Create a network model relationship in the Telecommunications Network Inventory application that captures the relationships between your network model entities.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

A model relationship captures the relationships between the inventory models. By defining the relationships between the various network model entities, you can also define the compatibility between these entities.

For example, if you select **Equipment to Slot** in the **Relationship Type** field, you can define the relationship between a specific equipment inventory model and a specific slot inventory model. In this case, you would see that the number of slots in the specified slot model are compatible with the specified equipment model. To learn more, see [Model relationships](../concept/inventory-modeling-process.md).

When you create a network model relationship, it creates a model in the Network Model \[sn\_ni\_core\_network\_model\_relationship\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Click the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory Models** &gt; **Network Model Relationships**.

3.  Click **New**.

4.  Fill in the general information to create a network model relationship.

    **Note:** To learn more about the fields, see [Network Model Relationship fields](../reference/tni-network-model-relationship-form.md).

5.  To add attachments, such as graphics or documents, click the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

6.  Click **Save**.

7.  To delete a model, click the options icon \(![Options icon.](../image/options-icon.png)\) next to the **Save** button, and click **Delete**.


**Parent Topic:**[Create inventory models](../concept/creating-your-inventory-models.md)

**Related topics**  


[Network inventory models](../concept/using-inventory-models-tni.md)

[Model relationships](../concept/inventory-modeling-process.md)

