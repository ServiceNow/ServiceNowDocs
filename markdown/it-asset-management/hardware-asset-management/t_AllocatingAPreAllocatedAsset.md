---
title: Allocate a pre-allocated asset
description: Assets can be allocated from pre-allocated asset records, which creates new asset records and reduces the Quantity in the original pre-allocated asset record.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage pre-allocated assets, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Allocate a pre-allocated asset

Assets can be allocated from pre-allocated asset records, which creates new asset records and reduces the **Quantity** in the original pre-allocated asset record.

## Before you begin

Role required: asset

## About this task

Allocating an asset makes it a financial liability. After all pre-allocated assets have been allocated, the pre-allocated asset record is removed from the asset list.

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **All Assets**.

2.  Filter the **Substate** column to show only **Pre-allocated** assets.

3.  Select the reference icon in the row containing the asset to allocate.

4.  Select **Allocate** at the bottom of the form.

    **Note:** If the **glide.asset.create\_ci\_with\_ire** property is set to `true`, a form appears when you click **Allocate**. On the form, fill in the **Asset tag**, **Serial number**, and **Reserved for** fields, then click **OK**.


## Result

The system creates and navigates to a new asset record, which has the same model and parent information as the pre-allocated asset. The new asset has a **Quantity** of one, while the pre-allocated asset's **Quantity** is reduced by one.

**Parent Topic:**[Manage pre-allocated assets](../../hardware-asset-management/concept/manage-preallocated-asset.md)

