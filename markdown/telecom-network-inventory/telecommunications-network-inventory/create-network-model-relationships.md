---
title: Define a network model relationship
description: Create a network model relationship in the Telecommunications Network Inventory application that captures the relationships between your network model entities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/create-network-model-relationships.html
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

For example, if you select **Equipment to Slot** in the **Relationship Type** field, you can define the relationship between a specific equipment inventory model and a specific slot inventory model. In this case, you would see that the number of slots in the specified slot model are compatible with the specified equipment model. To learn more, see [Modeling network inventory relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-modeling-process.md).

When you create a network model relationship, it creates a model in the Network Model \[sn\_ni\_core\_network\_model\_relationship\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Click the list icon \(\[Omitted image "ni-workspace-list-icon.png"\] Alt text: List icon.\), and then go to **Inventory Models** &gt; **Network Model Relationships**.

3.  Click **New**.

4.  Fill in the general information to create a network model relationship.

    **Note:** To learn more about the fields, see [Network Model Relationship fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/tni-network-model-relationship-form.md).

5.  To add attachments, such as graphics or documents, click the attachment icon \(\[Omitted image "attachments-icon.png"\] Alt text: Attachment icon.\) in the right panel.

6.  Click **Save**.

7.  To delete a model, click the options icon \(\[Omitted image "options-icon.png"\] Alt text: Options icon.\) next to the **Save** button, and click **Delete**.


**Parent Topic:**[Create inventory models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/creating-your-inventory-models.md)

**Related topics**  


[Network inventory models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/using-inventory-models-tni.md)

[Modeling network inventory relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-modeling-process.md)

