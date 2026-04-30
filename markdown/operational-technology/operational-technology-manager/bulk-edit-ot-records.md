---
title: Convert your OT devices to IT hardware devices in a bulk edit
description: Bulk edit your Operational Technology \(OT\) devices to remove the OT device details. Then convert your OT devices to IT hardware devices.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-08-06"
reading_time_minutes: 1
breadcrumb: [OT device related items and related lists, Edit or view OT devices after import or discovery, Use, Operational Technology Manager, Operational Technology]
---

# Convert your OT devices to IT hardware devices in a bulk edit

Bulk edit your Operational Technology \(OT\) devices to remove the OT device details. Then convert your OT devices to IT hardware devices.

## Before you begin

Role required: cmdb\_ot\_admin or admin

## About this task

If you encounter OT devices that don't have an OT function and should be classified as IT hardware devices, you can select and edit multiple OT devices in a bulk edit to convert them to IT hardware devices.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Workspace.**

2.  In the list view, select one of the following lists.

    -   OT Computer and Servers
    -   OT Network Gear
    -   Industrial IoT \(IIoT\)
3.  Select the OT devices that you want to convert to IT hardware devices.

    If you want to select all OT devices in the list, select the check box next to the OT device column.

4.  Select the **Remove OT device details** button.

    A dialog box appears that asks you to confirm that you want to remove the OT device details but keep all the other configuration item details.

    **Note:** None of the CI details, network adapters, or IP addresses are removed. Only the OT-specific data is removed.

    ![Remove OT device details dialog box.](../image/remove-ot-asset-details.png)

5.  Select **Confirm**.


## Result

The OT device details are removed from the selected OT devices and the OT devices are converted to IT hardware devices. You can view these IT hardware devices in the IT Hardware list view on the Industrial Workspace.

**Parent Topic:**[OT device related items and related lists](../reference/ot-assets-related-links-and-lists.md)

