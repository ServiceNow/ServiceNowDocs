---
title: Add depreciation to an asset
description: Depreciation is the reduction in the value of an asset over time.
locale: en-US
release: yokohama
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage various assets through asset classes, Using Asset Management, Asset Management, IT Asset Management]
---

# Add depreciation to an asset

Depreciation is the reduction in the value of an asset over time.

## Before you begin

Role required: asset

## About this task

A depreciation schedule can be added to hardware assets. Based on the information specified in the asset record, the ServiceNow AI Platform calculates the depreciation amount using the **Calculate Depreciation** scheduled job. The following system properties determine when the **Calculate Depreciation** scheduled job should be triggered to calculate the depreciation amount:

-   The **sn\_itam\_depreciation\_job\_last\_run** system property stores the date on which the **Calculate Depreciation** scheduled job was last run.
-   The **sn\_itam\_trigger\_depreciation\_job\_after\_days** system property determines the frequency \(in days\) at which the **Calculate Depreciation** scheduled job should be triggered.

    **Note:** By default, this system property is set to **7**. Therefore, the **Calculate Depreciation** scheduled job runs weekly to calculate depreciation amount.


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

    **Important:** The **Calculate Depreciation** scheduled job calculates the depreciation amount weekly. If you perform this step before the next run date of the scheduled job, the recently calculated depreciation amount is displayed.


**Parent Topic:**[Manage various assets through asset classes](../concept/c_AssetClasses.md)

**Related topics**  


[Create an asset class](t_CreateAnAssetClass.md)

[Create license assets](t_CreatingLicenseAssets.md)

[Set asset states and substates](t_SettingAssetStatesAndSubstates.md)

