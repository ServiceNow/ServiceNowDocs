---
title: Create a facility model
description: Create a facility model in the Telecommunications Network Inventory application to define the physical characteristics data of the facility record according to the product manufacturer's recommendations.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-05-17"
reading_time_minutes: 2
breadcrumb: [Creating your inventory models, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create a facility model

Create a facility model in the Telecommunications Network Inventory application to define the physical characteristics data of the facility record according to the product manufacturer's recommendations.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

When you create a facility model, it creates the model record in the facility model \[sn\_ent\_facility\_model\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory Models** &gt; **Facility Models**.

3.  Select **New**.

4.  On the **Details** tab, fill in the fields.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name that appears for the facility model. The **glide.cmdb\_model.display\_name.shorten** system property controls how display names are generated for the equipment holder model.

</td></tr><tr><td>

Manufacturer

</td><td>

Name of the network asset's manufacturer. Select the search icon \(![Search icon.](../image/search.png)\) and select a manufacturer code. To learn more, see [Create manufacturer and vendor codes](add-company-designate-manufacturer-tni.md).

</td></tr><tr><td>

Name

</td><td>

Name of the facility model. The ServiceNow AI Platform uses this name to identify it in your network inventory.

</td></tr></tbody>
</table>5.  On the **Details** tab, fill in the General section.

    **Note:** To learn more about the fields, see [Inventory Model form - General](../reference/tni-model-form-general.md).

6.  On the **Details** tab, fill in the Information section.

    **Note:** To learn more about the fields, see [Inventory Model form - Information](../reference/tni-model-form-information.md).

7.  Select **Save**.


## Result

The related tabs appear on the form. You can view or modify the tabs information. To learn more about the related tabs, see [Inventory models additional tabs](../reference/additional-tabs-of-inventory-models.md).

**Parent Topic:**[Creating your inventory models](../concept/creating-your-inventory-models.md)

**Related topics**  


[Network inventory models](../concept/using-inventory-models-tni.md)

