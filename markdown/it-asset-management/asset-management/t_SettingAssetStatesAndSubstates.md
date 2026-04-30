---
title: Set asset states and substates
description: Use asset states and substates to track assets accurately and at a detailed level.
locale: en-US
release: zurich
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Manage various assets through asset classes, Use, Asset Management, IT Asset Management]
---

# Set asset states and substates

Use asset states and substates to track assets accurately and at a detailed level.

## Before you begin

Role required: asset

## About this task

Good asset information helps you with reporting, controlling assets, and lowering costs. For example, recording missing items using the **State** and **Substates** fields enables you to run reports and analyze the information. You can use this information to lower costs.

**Tip:** You shouldn’t modify state values. If the state values are supported and defined by the process, you can modify substates.

Some of the substate values are available with more than one state. For example, the substate **Pending disposal** is available with the state **In stock**, **In transit**, and **Retired**. The combination of the **State** and the **Substate** fields provide the correct asset tracking information. For example, an asset that is **In stock** and **Pending disposal** indicates that the asset is no longer used and is in the stockroom waiting to be disposed of.

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **All Assets**.

2.  Select an asset.

3.  Edit the **State** and **Substate** fields.

<table id="table_xbc_25h_3p"><thead><tr><th>

State

</th><th>

Available substates

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

On order

</td><td>

None

</td><td>

Asset is ordered but isn't received.

</td></tr><tr><td>

In stock

</td><td>

-   Available: Asset is available for use.
-   Reserved: Asset is reserved for a user who requested it through a sourcing request.
-   Defective: Asset is faulty or inoperative.
-   Pending repair: Defective asset is marked for repair by the vendor.
-   Pending install: Asset is yet to be installed.
-   Pending donation: Asset is marked for donation because it’s no longer required in your stockroom.
-   Pending disposal: Asset is marked for disposal because it’s no longer required in the stockroom.
-   Pending transfer: Asset is being planned to be transferred through a transfer order.
-   Pre-allocated: Asset is ready to be allocated but isn’t a financial liability until it’s allocated to a user.
-   On hold: Asset isn’t ready to be used because it’s awaiting something. For example, necessary documentation is pending.
-   Legal hold: Asset is kept on hold because of some legal reasons.
-   Quarantine: Asset is kept in isolation in the stockroom.
-   Pending certificate: Asset is awaiting certificate for disposal.
-   Pending return: Asset that is leased is yet to be returned.
-   Test: Asset is in the testing phase and not yet operational.
-   Pending resale: Asset is awaiting resale.
-   Pending evaluation: Asset is yet to be evaluated or assessed to confirm if it can be used.


</td><td>

Asset is stored in a stockroom. Substate indicates if the asset can be put to use.

</td></tr><tr><td>

In transit

</td><td>

-   Available: Asset is available for use.
-   Reserved: Asset is reserved for a user who requested it through a sourcing request.
-   Defective: Asset is faulty or inoperative.
-   Pending install: Asset is yet to be installed.
-   Pending disposal: Asset is marked for disposal because it’s no longer required in your stockroom.
-   Pending donation: Asset is marked for donation because it’s no longer required in your stockroom.
-   Pre-allocated: Asset is ready to be allocated but isn’t a financial liability until it’s allocated to a user.
-   Pending resale: Asset is awaiting resale.


</td><td>

Asset is being transported.

</td></tr><tr><td>

In use

</td><td>

-   Pending fulfillment: Asset is functional but awaiting business conditions such as billing and signoff.
-   End of support: Asset isn't provided any support services through incidents or contracts.
-   Pending retirement: Asset is marked for retirement because it’s no longer in service. Asset has reached the end of life and can be sold, disposed, or donated.
-   None


</td><td>

Asset is in use. This option is available for non-consumables only.

</td></tr><tr><td>

In maintenance

</td><td>

None

</td><td>

Asset is being repaired or undergoing maintenance.

</td></tr><tr><td>

Retired

</td><td>

-   Disposed: Asset is disposed because it has reached end of life.
-   Pending disposal: Asset is marked for disposal because it’s nearing the end of life.
-   Sold: Asset is sold.
-   Donated: Asset is donated to charity organization through asset donation orders.
-   Vendor credit: Old faulty asset is returned to the vendor for a replacement asset through Return Merchandise Authorization \(RMA\).
-   Lease return: Leased hardware asset is returned before the expiry of contract.
-   Obsolete: Asset is obsolete and should be disposed.
-   RMA: Faulty asset is returned to or replaced by the vendor through Return Merchandise Authorization \(RMA\).
-   Buy out: Leased hardware asset is bought before the expiry of contract.
-   Pending resale: Asset is awaiting resale.


</td><td>

Set the asset to a Retired state when the asset has reached the end of life. Only delete asset records if they were created erroneously.

</td></tr><tr><td>

Missing

</td><td>

-   Lost
-   Stolen


</td><td>

An asset that is missing or lost.

</td></tr><tr><td>

Build

</td><td>

None

</td><td>

Asset is being prepared. This state is used during the creation of an asset bundle.**Note:** Hardware and consumables don't have a Build state.

</td></tr></tbody>
</table>
**Parent Topic:**[Manage various assets through asset classes](../concept/c_AssetClasses.md)

**Related topics**  


[Create an asset class](t_CreateAnAssetClass.md)

[Create license assets](t_CreatingLicenseAssets.md)

[Add depreciation to an asset](t_AddingDepreciationToAnAsset.md)

