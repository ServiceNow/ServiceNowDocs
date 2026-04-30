---
title: Create assets
description: Create hardware, software, consumable, bundle, pallet, mobile, and facility assets using the Core UI or the Hardware Asset Workspace.
locale: en-US
release: zurich
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Work with Asset and CI, Use, Asset Management, IT Asset Management]
---

# Create assets

Create hardware, software, consumable, bundle, pallet, mobile, and facility assets using the Core UI or the Hardware Asset Workspace.

## Before you begin

Role required: asset

## About this task

-   **Unique identifiers for assets**

    When you create an asset that belongs to a model category linked to a CI class with identification rules defined for fields like the Asset tag, Serial number, or MAC address, you should provide details for at least one of these fields. The identification rules for a CI class are defined in the CMDB Identification and Reconciliation engine \(IRE\). For more details, see [Identification rules](https://www.servicenow.com/docs/access?context=c_IdentificationRules&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) and [Create a CI identification rule](https://www.servicenow.com/docs/access?context=t_CreateCIIdentificationRule&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US). These rules help to uniquely identify the asset through these required fields and maintain accurate asset records. However, specifying the values for these fields is optional in the following scenarios:

    -   When you are creating an asset that belongs to a model category without a CI class.
    -   When you are creating an asset that belongs to a model category linked to a CI class without any identification rules defined.

## Procedure

1.  Create an asset.

<table id="choicetable_tcm_zwf_cxb"><thead><tr><th align="left" id="d100511e99">

Interface

</th><th align="left" id="d100511e102">

Action

</th></tr></thead><tbody><tr><td id="d100511e108">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **All Assets**.
2.  Select the type of asset that you want to create.
3.  Select **New**.


</td></tr><tr><td id="d100511e147">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset estate**.
2.  Select **New Asset**.
3.  In the dialog box, select the asset type and then select **Create**.


</td></tr></tbody>
</table>2.  On the Asset record fields form, fill in the fields.

    For a description of the field values, see [Asset record fields](../reference/asset-record-fields.md).

3.  Submit or save the asset form.


**Parent Topic:**[Work with Asset and CI](../../hardware-asset-management/concept/work-with-asset-ci.md)

