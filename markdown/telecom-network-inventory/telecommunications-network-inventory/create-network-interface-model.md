---
title: Create a network interface model
description: Create a network interface model in the Telecommunications Network Inventory application to define the physical characteristics data of the network interface as per the product recommendations of the manufacturer.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create inventory models, Use, Telecommunications Network Inventory]
---

# Create a network interface model

Create a network interface model in the Telecommunications Network Inventory application to define the physical characteristics data of the network interface as per the product recommendations of the manufacturer.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

When you create a network interface model, it creates the model record in the Network Interface Model \[sn\_ent\_nw\_interface\_model\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon..](../image/ni-workspace-list-icon.png)\), and then go to **Inventory Models** &gt; **Interface Models**.

3.  Select **New**.

4.  On the **Details** tab, fill in the fields.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name that appears for the network interface model. The **glide.cmdb\_model.display\_name.shorten** system property controls how display names are generated for the network interface model.

</td></tr><tr><td>

Manufacturer

</td><td>

Name of the network asset's manufacturer. Select the search icon \(![Search icon.](../image/search.png)\) and select a manufacturer code. To learn more, see [Create manufacturer and vendor codes](add-company-designate-manufacturer-tni.md).

</td></tr><tr><td>

Name

</td><td>

Name of the network interface model. The ServiceNow AI Platform uses this name to identify it in your network inventory.

</td></tr></tbody>
</table>5.  On the **Details** tab, fill in the General section.

    **Note:** To learn more about the fields, see [Inventory Model form - General](../reference/tni-model-form-general.md).

6.  Under the **Details** tab, on the form, fill in the fields.

    **Note:** To learn more about the fields, see [Network Interface Model form - Information tab](../reference/network-interface-model-form-information-tab.md).

7.  To add the compatible network interface models, select **Add Compatible**.

    You can track the network assets that work with the network interface model.

    **Note:** In the classic environment, this function is available only for administrators.

8.  To add the substitute network interface models, select **Add Substitutions**.

    You can track the network interface models that you use to substitute another network interface model with.

    **Note:** In the classic environment, this function is available only for administrators.

9.  To add the attachments, such as graphics or documents, select the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

10. Select **Save**.

    The related tabs appear on the form. You can view or modify the tabs information. To learn more about the related tabs, see [Inventory models additional tabs](../reference/additional-tabs-of-inventory-models.md).

11. To delete a model, select the options icon \(![Options icon.](../image/options-icon.png)\) next to the **Save** button, and select **Delete**.


**Parent Topic:**[Create inventory models](../concept/creating-your-inventory-models.md)

**Related topics**  


[Network inventory models](../concept/using-inventory-models-tni.md)

