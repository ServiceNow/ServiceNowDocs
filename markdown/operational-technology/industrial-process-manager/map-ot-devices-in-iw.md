---
title: Map OT devices to equipment model entities from the Equipment Model Manager
description: Map Operational Technology \(OT\) devices to equipment model entities from the Equipment Model Manager in the Industrial Workspace.
locale: en-US
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automatically map all OT devices, Automated Mapping Across Zone-based IP Network Groups, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Map OT devices to equipment model entities from the Equipment Model Manager

Map Operational Technology \(OT\) devices to equipment model entities from the Equipment Model Manager in the Industrial Workspace.

## Before you begin

Role required: cmdb\_ot\_isa\_editor and cmdb\_ot\_viewer

## Procedure

1.  Navigate to the Industrial Workspace.

2.  To open the Equipment Model Manager, select the **Equipment model** ![](../image/equip-model-manager-button.png)icon.

3.  Select the equipment model entity that contains the OT devices you want to map.

4.  In the equipment model entity record, select the **Mapped OT Devices** tab.

5.  Select the **Map OT devices** UI action.

6.  Using the **All devices** and **Unmapped devices** tabs, select the OT devices you want to map by clicking the check box in the first table column.

    The **All devices** tab shows all the OT devices available in your OT system, mapped or unmapped. The **Unmapped devices** tab shows the OT devices that aren't yet mapped to an equipment model entity. Using these 2 tabs to select OT devices gives you better visibility into which OT devices still need to be mapped to an equipment model entity.

    In the **All devices** tab, you can view the equipment model entities a device is already mapped to with the **Mapped Equipment Model Entity** column. In the **Unmapped devices** tab, the column is empty to show the device isn't mapped yet.

7.  Select **Map devices**.

8.  In the **Select equipment model entity to map devices** model, select the check box next to the equipment model entity or entities you want to map the devices to.

9.  Select **Confirm**.


## Result

Once you select **Confirm**, a message appears to notify you that the selected OT devices are being mapped and that the process may take a few minutes to complete.

## What to do next

To view the newly mapped devices, you can select the link provided in the message. The link takes you back to the equipment model entity record. You can then open the **Mapped OT devices** tab to see the devices added to the list.

**Parent Topic:**[Automatically map all OT devices to an equipment model entity](../../operational-technology-management/task/automatedly-map-all-ot-assets.md)

