---
title: Create a Software Asset Management Foundation plugin entitlement allocation in classic
description: A user or device allocation can be added to a software entitlement to specify a user or device to which rights have been allocated.
locale: en-US
release: yokohama
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Create a Software Asset Management Foundation plugin entitlement in classic, Configuring Software Asset Management Foundation plugin classic, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Create a Software Asset Management Foundation plugin entitlement allocation in classic

A user or device allocation can be added to a software entitlement to specify a user or device to which rights have been allocated.

## Before you begin

Role required: sam\_user

## About this task

User allocations are stored in the User Allocations \[alm\_entitlement\_user\] table. Device allocations are stored in the Device Allocations \[alm\_entitlement\_asset\] table.

**Note:** The total of all allocation quantities cannot exceed the total number of rights for the entitlement.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Licensing** &gt; **Software Entitlements** and open the software entitlement record to add allocations to.

2.  Click the applicable allocations related list \(**User Allocations** or **Device Allocations**\) to configure \(see table for field descriptions\).

    **Note:** The allocations related list that is shown pertains to the license metric that you chose. Only one related list for allocations is shown.

<table id="table_wzq_51x_dp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

User Allocations

</td></tr><tr><td>

Assigned to

</td><td>

The user to which the license is allocated.

</td></tr><tr><td>

Software Model

</td><td>

Automatically set based on entitlements software model.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of rights allocated to this user. Default is 1.Multiple rights come into play in the case where many rights are needed to fully license a device or user, such as with per core.

</td></tr><tr><td>

License Key

</td><td>

License key of the software.

</td></tr><tr><td class="sub-head" colspan="2">

Device Allocations

</td></tr><tr><td>

Assigned to

</td><td>

The device to which the license is allocated.

</td></tr><tr><td>

Software Model

</td><td>

Automatically set based on entitlements software model.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of licenses allocated to this user. Default is 1.Multiple licenses come into play in the case where licenses are allocated per core and multiple core rights are needed.

</td></tr><tr><td>

License Key

</td><td>

License key of the software.

</td></tr></tbody>
</table>
**Parent Topic:**[Create a Software Asset Management Foundation plugin entitlement in classic](t_AddASoftwareEntitlementSAMF.md)

