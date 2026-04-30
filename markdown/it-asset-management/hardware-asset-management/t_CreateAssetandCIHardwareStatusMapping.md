---
title: Map asset state and CI hardware status
description: Map the asset State and Substate fields to the CI Hardware Status field. Don't use the Substatus field on hardware CIs because the CI synchronization does not update the field when assets are updated. When you create the mapping, you can set the synchronization direction from the asset, CI, or both.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Work with Asset and CI, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Map asset state and CI hardware status

Map the asset **State** and **Substate** fields to the **CI Hardware Status** field. Don't use the **Substatus** field on hardware CIs because the CI synchronization does not update the field when assets are updated. When you create the mapping, you can set the synchronization direction from the asset, CI, or both.

## Before you begin

Role required: admin or asset

**Note:** If you upgraded from a prior release and you've customized the AssetAndCISynchronizer script before the upgrade, overwrite the customization and then recreate the custom mappings.

The hardware and consumable assets don't have the Build state and Design substate because they are already prepared. Therefore, the Asset CI hardware state mappings table doesn't have a mapping for the Build state. For more details on asset states, see [Set asset states and substates](t_SettingAssetStatesAndSubstates.md).

## About this task

The **Install Status** and **Hardware Status** fields of a CI are independent of each other. There is no correlation between them. A change to the **Hardware Status** field does not change the **CI Install Status** field and vice versa.

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Administration** &gt; **Asset-CI Hardware Status Mapping**.

    By default, only custom mappings display. The list of mappings uses the filter condition of **\[Out of the box\] \[is\] \[False\]**.

2.  Click **New**.

3.  From the **Asset state** list, select the state you want to map.

4.  If available, select a substate from the **Asset substate** list.

    Some of the asset states do not have a substate.

5.  From the **Configuration Item status**list, select the logically associated CI state you want to map.

6.  If available, select a substate from the **Configuration Item substatus** list.

    Some of the CI statuses do not have a substatus.

7.  From the **Sync direction** list, select the direction you want to drive the synchronization.

8.  Select the **Active** check box to activate the mapping.

9.  Click **Submit**.


**Parent Topic:**[Work with Asset and CI](../../hardware-asset-management/concept/work-with-asset-ci.md)

