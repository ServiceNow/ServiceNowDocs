---
title: Create device allocation
description: Create a device allocation for a software entitlement to specify devices that have been granted rights.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-10-06"
reading_time_minutes: 1
breadcrumb: [License operations view, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create device allocation

Create a device allocation for a software entitlement to specify devices that have been granted rights.

## Before you begin

Role required: sam\_admin or sam\_user

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations**.

2.  Select **Software entitlements**.

3.  Select a software entitlements record.

4.  Select the **Device Allocations** tab.

5.  Select **New**.

6.  On the form, fill in the fields.

    | | |
    |---|---|
    |Display name|Display name for device allocation. This field value is automatically set based on the selected **Allocated to** and **Entitlement** field value. This field value appears only when the allocation record is saved.|
    |Allocated to|The device to which the license is allocated.|
    |Entitlement|Automatically set to the selected software entitlement.|
    |Quantity|Quantity of licenses allocated to this device. Default is 1.|
    |License key|License key of the software.|

7.  Click **Save**.


## Result

-   Device allocation record is created for the device and listed in the **Device Allocations** tab.
-   The device allocation record is saved in the Device Allocations \[alm\_entitlement\_asset\] table.

**Related topics**  


[Copy user or device allocations](copy-allocations.md)

[Create entitlements in workspace](create-entitlements-workspace.md)

[Allocation management on Software Asset Management](../concept/allocation-management-sam.md)

