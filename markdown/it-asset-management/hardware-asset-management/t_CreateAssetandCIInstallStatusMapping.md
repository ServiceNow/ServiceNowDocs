---
title: Map asset state and CI install status
description: Map the asset State and Substate fields to the CI Install Status field. The Substatus field of the CI Install Status field should not be used for hardware CIs.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Work with Asset and CI, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Map asset state and CI install status

Map the asset **State** and **Substate** fields to the **CI Install Status** field. The **Substatus** field of the **CI Install Status** field should not be used for hardware CIs.

## Before you begin

Role required: admin or asset

**Note:** If you upgraded from a prior release and customized the AssetAndCISynchronizer script include before the upgrade, you must overwrite the customization and then recreate the custom mappings.

## About this task

Asset synchronization does not update this field when hardware assets are updated. When you create the mapping, you can set the synchronisation direction from Asset to CI, but not from CI to Asset. For non-Hardware CI classes, you can set the synchronisation in both the directions.

The hardware and consumable assets don't have the Build state and Design substate because they are already prepared. Therefore, the Asset CI install status mappings table doesn't have a mapping for the Build state. For more details on asset states, see [Set asset states and substates](t_SettingAssetStatesAndSubstates.md).

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Administration** &gt; **Asset-CI Install Status Mapping**.

    By default, only custom mappings display. The list of mappings uses the filter condition of **\[Out of the box\] \[is\] \[False\]**.

2.  Click **New**.

3.  From the **Asset State** list, select the state you want to map.

4.  If available, select a substate from the **Asset Substate** list.

    Some of the asset states do not have a substate.

5.  From the **Configuration Item Status** list, select the logically associated CI status you want to map.

6.  From the **Sync direction** list, select the direction you want to drive the synchronization.

7.  Select the **Active** check box to activate the mapping.

8.  Click **Submit**.


**Parent Topic:**[Work with Asset and CI](../../hardware-asset-management/concept/work-with-asset-ci.md)

