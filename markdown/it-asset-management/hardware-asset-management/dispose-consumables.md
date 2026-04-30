---
title: Plan disposal of consumable assets
description: Make the consumable assets that are no longer required in your stockrooms ready for disposal.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Consumables life cycle, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Plan disposal of consumable assets

Make the consumable assets that are no longer required in your stockrooms ready for disposal.

## Before you begin

Role required: asset, itil, itil\_admin

Know that the Planned for disposal column in the Consumable \[alm\_consumable\] table indicates if the consumable asset is marked for disposal or not.

## About this task

When you mark assets for disposal, you are only making them available for disposal. To dispose of the consumable assets, you should create a disposal order in the Hardware Asset Management application.

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Consumables**.

2.  In the consumable record on the top right of the page, click **Mark for disposal**.

    **Mark for disposal** appears only for consumable assets that are in the In stock state and not marked for disposal.

    The state and substate of the consumable asset change to In stock and Pending disposal.

3.  In the Planned for disposal dialog box, enter the total quantity or partial quantity of the consumable asset.

    If you enter a partial quantity, a new consumable record is created with the substate as pending disposal. If you enter a total quantity, the consumable's record substatus changes to "pending disposal" and you return to the same consumable record.

    After you mark the consumable asset for disposal, **Mark for disposal** no longer appears.

    **Note:** Only a consumable marked for disposal is included in a disposal order. After you mark a consumable for disposal, it does not get merged with another consumable record.

4.  Select **Cancel from disposal** to cancel disposing a consumable asset.

    **Cancel from disposal** appears if the Planned for disposal column for the consumable is set to true and the **Disposal number** field is blank.

5.  In the Cancel from disposal dialog box, select a stockroom.

    If a stockroom is already selected, then the **Stockroom** field is read-only.

6.  Select a substate and select **OK**.

    The Planned for disposal column is set to false. If you added this consumable record to a disposal record, the planned asset record is deleted.


## What to do next

[Create a disposal order](create-disposal-order.md).

**Parent Topic:**[Consumables life cycle](../../asset-management/concept/c_FollowLifeCycleConsumbl.md)

