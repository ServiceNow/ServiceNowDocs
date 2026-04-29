---
title: Dispose of consumable assets
description: Dispose of those consumable assets that are no longer required in your stockrooms.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Consumables life cycle, Using Asset Management, Asset Management, IT Asset Management]
---

# Dispose of consumable assets

Dispose of those consumable assets that are no longer required in your stockrooms.

## Before you begin

Role required: asset, itil, itil\_admin

Know that the Planned for disposal column in the Consumable \[alm\_consumable\] table indicates if the consumable asset is marked for disposal or not.

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Consumables**.

2.  In the consumable record on the top right of the page, click **Mark for disposal**.

    **Mark for disposal** appears only for consumable assets that are in the in-stock state and not marked for disposal.

3.  In the Planned for disposal dialog box, enter the total quantity or partial quantity of the consumable asset.

    If you enter a partial quantity, a new consumable record is created with the substate as pending disposal. If you enter a total quantity, the consumable's record substatus changes to "pending disposal" and you return to the same consumable record.

    After you mark the consumable asset for disposal, **Mark for disposal** no longer appears.

    **Note:** Only a consumable marked for disposal is included in a disposal order. After you mark a consumable for disposal, it does not get merged with another consumable record.

4.  Click **Cancel from disposal** to cancel disposing a consumable asset.

    **Cancel from disposal** appears if the Planned for disposal column for the consumable is set to true and the **Disposal number** field is blank.

5.  In the Cancel from disposal dialog box, select a stockroom.

    If a stockroom is already selected, then the **Stockroom** field is read-only.

6.  Select a substate and click **OK**.

    The Planned for disposal column is set to false. If you added this consumable record to a disposal record, the planned asset record is deleted.


**Parent Topic:**[Consumables life cycle](../../asset-management/concept/c_FollowLifeCycleConsumbl.md)

