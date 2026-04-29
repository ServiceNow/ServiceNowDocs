---
title: Create a physical connection model
description: Create a physical connection model in the Telecommunications Network Inventory application to define the metadata for the different physical connections. In the physical connection model, you can import models, attach a file or an image, add or remove optional fields, and add compatibilities and substitutions.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create inventory models, Use, Telecommunications Network Inventory]
---

# Create a physical connection model

Create a physical connection model in the Telecommunications Network Inventory application to define the metadata for the different physical connections. In the physical connection model, you can import models, attach a file or an image, add or remove optional fields, and add compatibilities and substitutions.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

When you create a physical connection model record, it creates a model in the Physical Connection Models \[sn\_ent\_physical\_nw\_connection\_model\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory Models** &gt; **Physical Connection Models**.

3.  Select **New**.

4.  On the **Details** tab, fill in the common information for the physical connection model.

    The following table lists the fields that are unique to the Physical Connection form.

    |Field|Description|
    |-----|-----------|
    |Display name|Name that appears for the physical connection model. The **glide.cmdb\_model.display\_name.shorten** system property controls how display names are generated for the physical connection model.|
    |Manufacturer|Select the manufacturer name of the physical connection model.|
    |Name|Manufacturer-assigned name of the physical connection model that is specified by the model manager.|

5.  On the **Details** tab, fill in the general section of the form for the physical connection model.

    **Note:** To learn more about the fields, see [Inventory Model form - General](../reference/tni-model-form-general.md).

6.  On the **Details** tab, fill in the information section of the form for the physical connection model.

    To learn more about the fields, see [Inventory Model form - Information](../reference/tni-model-form-information.md).

7.  To add the compatible models, select **Add Compatible**.

    You can personalize the list of compatibles by using the gear icon \(![Gear icon.](../image/Personalize_1.png)\).

    **Note:** In the classic environment, this function is available only for administrators.

8.  To add the substitute physical connection models, select **Add Substitution**.

    You can track the network interface models that you use to substitute another network interface model with.

    **Note:** In the classic environment, this function is available only for administrators.

9.  To add the attachments, such as graphics or documents, select the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

10. Select **Save**.

    The related tabs appear on the form. You can view or modify the tabs information. To learn more about the related tabs, see [Inventory models additional tabs](../reference/additional-tabs-of-inventory-models.md).

11. To delete a model, select the options icon \(![Options icon.](../image/options-icon.png)\) next to the **Save** button, and click **Delete**.


**Parent Topic:**[Create inventory models](../concept/creating-your-inventory-models.md)

**Related topics**  


[Network inventory models](../concept/using-inventory-models-tni.md)

