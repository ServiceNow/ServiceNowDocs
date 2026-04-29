---
title: Add depreciation to an asset
description: Depreciation is the reduction in the value of an asset over time.
locale: en-US
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage various assets through asset classes, Using Asset Management, Asset Management, IT Asset Management]
---

# Add depreciation to an asset

Depreciation is the reduction in the value of an asset over time.

## Before you begin

Role required: asset

## About this task

A depreciation schedule can be added to hardware assets. Based on the information specified in the asset record, the ServiceNow AI Platform calculates the depreciation amount daily using the **Calculate Depreciation** scheduled job. The **sn\_itam\_trigger\_depreciation\_job\_after\_days** system property determines when the **Calculate Depreciation** scheduled job calculates the depreciation amount.

**Important:** The depreciation fields on the asset, such as Depreciated amount, Residual value, and Residual date are updated daily by the **Calculate Depreciation** job. If you plan to enable audit logging in these fields, it logs every change daily. This process could result in a large volume of audit entries, which might impact storage and log management.

The ServiceNow AI Platform calculates the read-only **Residual date** and **Residual value** fields based on the **Cost**, **Depreciation**, and **Depreciation effective date** fields. For example, if the asset **Cost** is $1000.00, the **Straight Line** depreciation method is selected, and exactly two years have passed, the **Residual value** would be $500.00.

When an asset is in the **In Use** state, the asset form populates a Deprecation effective date.

For more information about fixed assets and depreciation, see [Using Depreciation with Fixed Assets](../concept/c_CreatingFixedAssets.md#).

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **Hardware Assets**.

2.  Select an asset.

3.  Fill in the **Depreciation**, **Depreciation effective date**, **Salvage Value**, and **Covered by fixed asset** fields as described in [Create assets](t_CreatingAssets.md).

    Consider these points.

    -   If the depreciation effective date is in the future, depreciation is 0 and the current residual value is the original purchase price. The system doesn’t begin to calculate depreciation until the effective date is reached.
    -   The salvage value must be less than or equal to the asset cost. If a salvage value greater than the cost is entered, a warning message appears and the record can’t be saved.
4.  Select and hold \(or right-click\) the header and select **Save**.

5.  Select **Calculate Depreciation**.

    The **Residual date**, **Residual value**, and **Depreciated amount** fields are automatically calculated.


**Parent Topic:**[Manage various assets through asset classes](../concept/c_AssetClasses.md)

**Related topics**  


[Create an asset class](t_CreateAnAssetClass.md)

[Create license assets](t_CreatingLicenseAssets.md)

[Set asset states and substates](t_SettingAssetStatesAndSubstates.md)

