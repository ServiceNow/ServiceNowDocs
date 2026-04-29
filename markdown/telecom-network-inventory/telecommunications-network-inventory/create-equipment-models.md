---
title: Create an equipment model
description: Create an equipment model in the Telecommunications Network Inventory application as the first requirement for setting up the process to generate your network asset instances. You create an equipment model record every time a vendor or original equipment manufacturer \(OEM\) introduces new equipment for your use.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create inventory models, Use, Telecommunications Network Inventory]
---

# Create an equipment model

Create an equipment model in the Telecommunications Network Inventory application as the first requirement for setting up the process to generate your network asset instances. You create an equipment model record every time a vendor or original equipment manufacturer \(OEM\) introduces new equipment for your use.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

An equipment model represents the metadata that is provided by a vendor or manufacturer for the equipment. It defines the consistent characteristics across the various instances that are created for the equipment. An instance is an individual occurrence of a network asset at a site or datacenter. With this application, you define the physical characteristics data of the network equipment per the product manufacturer's recommendations. When you create an equipment model record, it creates the model record in the Equipment Model \[sn\_ent\_nw\_equipment\_model\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory Models** &gt; **Equipment Models**.

3.  Select **New**.

4.  On the **Details** tab, fill in the fields.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name that appears for the equipment model. The **glide.cmdb\_model.display\_name.shorten** system property controls how display names are generated for the equipment model.

</td></tr><tr><td>

Manufacturer

</td><td>

Name of the network asset's manufacturer. Select the search icon \(![Search icon.](../image/search.png)\) and select a manufacturer code. To learn more, see [Create manufacturer and vendor codes](add-company-designate-manufacturer-tni.md).

</td></tr><tr><td>

Name

</td><td>

Name of the equipment model. The ServiceNow AI Platform uses this name to identify it in your network inventory.

</td></tr></tbody>
</table>5.  On the **Details** tab, fill in the Information section.

    **Note:** To learn more about the fields, see [Inventory Model form - Information](../reference/tni-model-form-information.md).

6.  On the **Details** tab, fill in the General section.

    **Note:** To learn more about the fields, see [Inventory Model form - General](../reference/tni-model-form-general.md).

7.  To add the compatible equipment models, select **Add Compatible**.

    You can track the network assets that work with the equipment model.

    **Note:** In the classic environment, this function is available only for administrators.

8.  To add the substitute equipment models, select **Add Substitutions**.

    You can track the equipment models that you can use to substitute another equipment model with.

    **Note:** In the classic environment, this function is available only for administrators.

9.  To add the attachments, such as graphics or documents, select the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

10. Select **Save**.

    The related tabs appear on the form. You can view or modify information in these tabs. To learn more about the related tabs, see [Inventory models additional tabs](../reference/additional-tabs-of-inventory-models.md).

11. To delete a model, select the options icon \(![Options icon.](../image/options-icon.png)\) next to the **Save** button, and select **Delete**.


**Parent Topic:**[Create inventory models](../concept/creating-your-inventory-models.md)

**Related topics**  


[Network inventory models](../concept/using-inventory-models-tni.md)

