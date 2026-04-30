---
title: Create fixed assets
description: Fixed assets are containers that can hold multiple assets. Fixed assets are commonly tracked at the corporate level by a finance or accounting department, but may contain IT assets such as hardware and software.You can calculate depreciation for a fixed asset using a choice of depreciation schedules. Calculating depreciation for a fixed asset can help IT coordinate with the corporate fixed asset system to report correct valuation and book value.
locale: en-US
release: yokohama
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Asset Management, Asset Management, IT Asset Management]
---

# Create fixed assets

Fixed assets are containers that can hold multiple assets. Fixed assets are commonly tracked at the corporate level by a finance or accounting department, but may contain IT assets such as hardware and software.

The **Fixed Asset** option in the Cost application shows the IT assets related to a fixed asset record. This link can help IT stay coordinated with the corporate asset system. Users with the financial\_mgmt\_admin and financial\_mgmt\_user roles can create fixed assets. After creating a fixed asset and adding assets, the residual value can be automatically calculated.

To create a fixed asset:

1.  Navigate to **Cost** &gt; **Fixed Assets**.
2.  Click **New**.
3.  Enter a name for the fixed asset.
4.  Click **Submit**.

To add assets to a fixed asset:

1.  Navigate to **Cost** &gt; **Fixed Assets**.
2.  Click a fixed asset.
3.  In the **Covered assets** related list, click **Edit**.
4.  In the **Collection** list, double-click an asset to add it to the **Covers Assets List**.
5.  Click **Save**.

To sum the residual values of all assets in a fixed asset:

1.  Navigate to **Cost** &gt; **Fixed Assets**.
2.  Click a fixed asset.
3.  Click **Sum Residual Value**.

    The ServiceNow platform calculates the**Residual Value**, **Total cost,** and **Total depreciation** based on information in the **Financial** and **Depreciation** sections on the individual asset records.


**Parent Topic:**[Using Asset Management](using-asset-management.md)

**Related topics**  


[Mobile app for Hardware Asset Management](../../../administer/mobile-my-asset/concept/mobile-my-asset.md)

[Work with Asset and CI](../../hardware-asset-management/concept/work-with-asset-ci.md)

[Manage various assets through asset classes](c_AssetClasses.md)

[Consumables life cycle](c_FollowLifeCycleConsumbl.md)

[Stockrooms](c_Stockrooms.md)

[Manage pre-allocated assets](../../hardware-asset-management/concept/manage-preallocated-asset.md)

[Manage transfer order](manage-transfer-orders.md)

[Example Asset Management process](../task/t_AssetManagementProcess.md)

[Use Organization Management](../reference/org-mgmt.md#)

## Use depreciation with fixed assets

You can calculate depreciation for a fixed asset using a choice of depreciation schedules. Calculating depreciation for a fixed asset can help IT coordinate with the corporate fixed asset system to report correct valuation and book value.

### Before you begin

Role required: financial\_mgmt\_admin or financial\_mgmt

### About this task

When creating a new depreciation schedule, select the **Declining Balance** or **Straight Line** depreciation **Category**. The two categories depreciate an asset by the same overall amount during the asset life cycle, but do so on different schedules.

-   **Declining Balance**: depreciates an asset by a greater amount in earlier accounting periods than in later periods.
-   **Straight Line**: depreciates an asset by an equal amount each accounting period.

The following example shows depreciated value on a $10,000.00 asset over five years using the two different methods.

|Year|Declining balance|Straight line|
|----|-----------------|-------------|
|1|$5000.00|$8000.00|
|2|$2500.00|$6000.00|
|3|$1250.00|$4000.00|
|4|$625.00|$2000.00|
|5|$0|$0|

### Procedure

1.  To view a depreciation schedule, navigate to **Financial Management** &gt; **Depreciation** and click the **Category**.

2.  To create a new depreciation schedule, click **New**.

3.  Enter a **Name**.

4.  Select a **Category**.

5.  Add a **Script** to calculate depreciation value.

    ![Depreciation schedule](../image/DepreciationSchedule.png "Example depreciation schedule script")

6.  Click **Submit**.

    The depreciation schedule is now available in the **Depreciation** field on the asset record.


