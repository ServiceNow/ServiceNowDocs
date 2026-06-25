---
title: Manage asset bundles from your inventory
description: Create asset bundles from existing assets in your inventory to track, reserve, or deploy a group of assets as a single entity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/create-bundled-assets.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Use, Hardware Asset Management, IT Asset Management]
---

# Manage asset bundles from your inventory

Create asset bundles from existing assets in your inventory to track, reserve, or deploy a group of assets as a single entity.

## Before you begin

An asset bundle is a grouping of assets and comprises of consumable and hardware assets. Only assets that are in the **In stock** status and **available** substatus are added to an asset bundle. Assets that are part of an asset bundle aren’t available as individual assets.

**Note:** For information on asset bundles, see [Asset bundles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/asset-bundles-concept.md).

Role required: asset

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Bundled Assets**.

2.  Select **New**.

    The model category defaults to **Bundle** and the state defaults to **Build**. The build state is associated to only the **Bundle** model category. The build state isn’t valid for assets.

3.  In the Bundle form layout, select a product model from the **Model** list.

4.  In the **Stockroom** field, select a stockroom from where the assets are sourced for the bundle.

5.  Automatically add assets to your bundle by selecting **Auto-allocate assets** or add specific assets by selecting **Select assets**:

    -   **Auto-select assets**: Automatically adds assets to the asset bundle. The assets are added from the stockroom specified in the asset bundle.

        **Note:** Assets are allocated only when all the assets that are part of the bundle are available. Excluded assets aren't considered for auto-selection. For more information about asset exclusion, see [Hardware Asset Management license exclusion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/ham-license-exclusion.md).

    -   **Select assets**: Select the assets that you want in your asset bundle and select **Add Assets**.

        **Note:**

        You can't select an excluded asset. For more information about asset exclusion, see [Hardware Asset Management license exclusion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/ham-license-exclusion.md). Assets displayed are confined to the stockroom specified in the asset bundle.

    Once the assets are allocated to the bundle, the assets appear in the Assets related list and **Auto-allocate assets** and **Select assets** no longer appear in the Bundle form layout.

    **Note:** You must include all the assets to the asset bundle that are associated with the bundled model as a model component. If any asset isn’t included, the bundle asset is considered incomplete, and the **State** field value of the bundle asset can’t be changed.

6.  Select **Save**.

    The asset bundle is created. The cost of the bundled model is stamped on the asset bundle and on the expense line of the asset bundle. The cost isn’t the cumulative cost of all the model components of the bundled model.

7.  You can swap assets from an asset bundle by selecting **Replace assets**.

    Assets belonging to an asset bundle can be swapped when the state of the bundle is **In maintenance** or **In stock** \(substate **Pending repair**\).

    1.  In the Replace assets dialog box, select the assets you want to swap.

    2.  Select the asset that you want to swap the current asset with.

    3.  Select **Replace**.

        The asset that was swapped is returned to the stockroom.

8.  You can delete an asset bundle by selecting **Delete**.

    You must disassociate assets from an asset bundle to delete the bundle. Once all the assets are released from the bundle, you can delete the bundle.

    1.  In the **State** field, select **Retired**.

    2.  Select **Save**.

    3.  Select the **Release Assets** related link.

    4.  In the confirmation dialog box, select **Release assets**.

        All the assets are disassociated from the asset bundle and are moved to a stockroom.

    5.  Select **Delete**.

        The asset bundle is deleted.


**Parent Topic:**[Using Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/using-ham-classic.md)

**Related topics**  


[Analyze hardware assets using the Generate hardware asset insights generative AI skill]()

[Work with hardware normalization]()

[Manage your inventory through pallet assets]()

[Manage loaner assets]()

[Donate assets to charity organizations]()

[Use Advanced Shipment Notification]()

[Manage RMA requests]()

[Create an inventory stock order request]()

[Create a disposal order]()

[Fulfilling hardware asset requests]()

[Audit hardware asset inventory]()

[Request a Hardware Asset Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[View RFID information of assets]()

[Manage the lifecycle of hardware models with calculated lifecycle templates]()

[Create an internal lifecycle in the Hardware Asset Workspace]()

[Receive asset warranty details from Lenovo]()

[Manage stockrooms]()

[Track shipments using the integration framework]()

[Track asset location using indoor maps]()

[Assess performance of Hardware Asset Management]()

[Manage refresh of assets using Zero Touch Refresh]()

[Configure the Total Cost of Ownership of assets]()

[Manage Hardware Asset Management subscriptions]()

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage hardware asset tasks using the Mobile Agent application]()

[Manage asset put away using the Hardware Asset Workspace]()

[Audit your hardware assets by using Asset Attestation]()

[Acknowledge receipt of assets on the Employee Center portal]()

[Update associated Decision tables for HAM flows]()

