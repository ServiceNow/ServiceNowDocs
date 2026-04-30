---
title: Map asset and CI fields
description: When you map the asset and CI fields, synchronization happens both ways. Changes to either the asset or CI record are updated to the logically mapped record. You can synchronize custom mappings and mappings provided with the base instance.
locale: en-US
release: yokohama
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Work with Asset and CI, Using Asset Management, Asset Management, IT Asset Management]
---

# Map asset and CI fields

When you map the asset and CI fields, synchronization happens both ways. Changes to either the asset or CI record are updated to the logically mapped record. You can synchronize custom mappings and mappings provided with the base instance.

## Before you begin

Role required: admin or asset

**Note:** If you upgraded from a prior release and customized the AssetAndCISynchronizer script include before the upgrade, you must overwrite the customization and then recreate the custom mappings.

## About this task

You can conditionally map the fields for synchronization. For example, you can map the Location field only for a hardware asset and not for a software asset. So when an asset is updated, the **Location** field is synchronized only for the hardware asset.

**Note:** You can't map the asset and CI fields if the asset value is present only in the Hardware \[alm\_hardware\] table and not in the Asset \[alm\_asset\] table.

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Administration** &gt; **Asset-CI Field Mapping** and click **New**.

2.  From the **Asset field** list, select the field.

    This list refers to the alm\_asset table.

3.  Select the logically associated field from the **Configuration Item field**list that refers to the cmdb\_ci table.

4.  To create conditions for the mapping, click the **Advanced view** related link.

    -   To specify conditions for synchronizing the asset field with the CI field, use the **Asset mapping condition** builder.
    -   To specify conditions for synchronizing the CI field with the asset field, use the **Configuration Item mapping condition** builder.
5.  Select the **Active** check box to activate the mapping.

6.  Select **Submit**.


**Parent Topic:**[Work with Asset and CI](../../hardware-asset-management/concept/work-with-asset-ci.md)

