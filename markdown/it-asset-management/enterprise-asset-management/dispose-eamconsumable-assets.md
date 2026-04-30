---
title: Dispose consumable assets in Enterprise Asset Workspace
description: Dispose of those consumable assets that are no longer required in your stockrooms.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and manage enterprise assets, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Dispose consumable assets in Enterprise Asset Workspace

Dispose of those consumable assets that are no longer required in your stockrooms.

## Before you begin

Role required: asset, itil, itil\_admin

Know that the Planned for disposal column in the Consumable \[alm\_consumable\] table indicates if the consumable asset is marked for disposal or not.

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Enterprise asset estate** &gt; **Consumable assets**.

2.  Open a consumable asset record and select **Mark for disposal**.

    **Mark for disposal** appears only for consumable assets that are in the in-stock state and not marked for disposal.

3.  In the Mark for disposal dialog box, enter the total quantity or partial quantity of the consumable asset.

    If you enter a partial quantity, a new consumable record is created with the substate as pending disposal. If you enter a total quantity, the consumable's record substatus changes to "pending disposal" and you return to the same consumable record.

    After you mark the consumable asset for disposal, **Mark for disposal** no longer appears.

    **Note:** Only a consumable marked for disposal is included in a disposal order. After you mark a consumable for disposal, it does not get merged with another consumable record.


**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

