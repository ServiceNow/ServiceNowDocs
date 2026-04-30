---
title: Create a card model
description: Create a card model in the Telecommunications Network Inventory application to define the physical characteristics data of the card as per the product manufacturer's recommendations.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Creating your inventory models, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create a card model

Create a card model in the Telecommunications Network Inventory application to define the physical characteristics data of the card as per the product manufacturer's recommendations.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

A card model defines the card's metadata, which are the attributes that are consistent across the various instantiated cards of that model. When you create a card model, it creates the model record in the card model \[sn\_ent\_nw\_card\_model\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory Models** &gt; **Card Models**.

3.  Select **New**.

4.  On the **Details** tab, fill in the fields.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name that appears for the card model. The **glide.cmdb\_model.display\_name.shorten** system property controls how display names are generated for the interface card model.

</td></tr><tr><td>

Manufacturer

</td><td>

Name of the network asset's manufacturer. Select the search icon \(![Search icon.](../image/search.png)\) and select a manufacturer code. To learn more, see [Create manufacturer and vendor codes](add-company-designate-manufacturer-tni.md).

</td></tr><tr><td>

Name

</td><td>

Name of the card model. The ServiceNow AI Platform uses this name to identify it in your network inventory.

</td></tr></tbody>
</table>5.  On the **Details** tab, fill in the General section.

    **Note:** To learn more about the fields, see [Inventory Model form - General](../reference/tni-model-form-general.md).

6.  On the **Details** tab, fill in the Information section.

    **Note:** To learn more about the fields, see [Inventory Model form - Information](../reference/tni-model-form-information.md).

7.  To add the compatible card models, select **Add Compatible**.

    You can track the network assets that work with the card model.

    **Note:** In the classic environment, this function is available only for administrators.

8.  To add the substitute card models, select **Add Substitutions**.

    You can track the card models that you use to substitute another card model with.

    **Note:** In the classic environment, this function is available only for administrators.

9.  To add the attachments, such as graphics or documents, select the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

10. Select **Save**.

    The related tabs appear on the form. You can view or modify the tabs information. To learn more about the related tabs, see [Inventory models additional tabs](../reference/additional-tabs-of-inventory-models.md).

11. To delete a model, select the options icon \(![Options icon.](../image/options-icon.png)\) next to the **Save** button, and click **Delete**.


**Parent Topic:**[Creating your inventory models](../concept/creating-your-inventory-models.md)

**Related topics**  


[Network inventory models](../concept/using-inventory-models-tni.md)

