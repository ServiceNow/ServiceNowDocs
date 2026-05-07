---
title: Replace aged enterprise assets
description: Replace aged enterprise assets by sourcing new enterprise assets.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Request an enterprise asset refresh, Using Service Catalog for Enterprise Asset Management requests and flows, Enterprise Asset Management, IT Asset Management]
---

# Replace aged enterprise assets

Replace aged enterprise assets by sourcing new enterprise assets.

## Before you begin

Role required: inventory\_user

## About this task

When refreshing enterprise assets, you don't have to manually update the asset records. When closing the enterprise asset refresh lines, the asset records and the assets are automatically updated. Close each task to go to the next task, complete the refresh, and reclaim the aged assets.

After sourcing the new assets, asset refresh is completed through the following stages:

-   Prepare asset task: Prepare the new asset before you hand it over to the user. For example, install any software that's required.
-   Schedule refresh task: Schedule a date to hand over the asset to the requester.
-   Deploy new asset: Hand over the asset to the requester or install the asset at the requester's location if necessary.
-   Reclaim aged asset: Collect the aged asset.

## Procedure

1.  Select the hardware asset refresh request.

<table id="choicetable_upl_qst_ywb"><thead><tr><th align="left" id="d191863e73">

Interface

</th><th align="left" id="d191863e76">

Action

</th></tr></thead><tbody><tr><td id="d191863e82">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Open Record** &gt; **Requests**.
2.  Select the request number of the enterprise asset refresh request that you want to fulfill.


</td></tr><tr><td id="d191863e115">

**Enterprise Asset Workspace**

</td><td>

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Procurement view**.
2.  Select the **Requests** tab.
3.  Select the request number of the enterprise asset refresh request that you want to fulfill.


</td></tr></tbody>
</table>    After your enterprise asset refresh request is approved, the following events happen:

    -   The Source Request flow is triggered to source new assets.
    -   In the **Catalog Tasks** tab, a catalog task is created for the procurement of the new enterprise asset.
2.  Under the Requested Item related list, open a requested item.

    After your enterprise asset request is approved, the Source Request flow is triggered. Under the Catalog tasks related list, a catalog task is created for the procurement of the new enterprise assets.

3.  Source items in the request.

    You can source items in the request by consuming the local stock, through purchase orders, or through transfer orders.

    For more details on sourcing items, see [Sourcing items in a service catalog request](../../procurement/concept/c_SourcingRequestItems.md).

    After the new asset is received, the following events happens:

    -   The Enterprise Asset Refresh Line flow is triggered for the asset.
    -   The Enterprise Asset Refresh Line tab is displayed next to the Asset Tasks tab on the requested item form.
    -   The Asset pick task is created under the Refresh Line Tasks only if the requested item is consumed from the local stockroom for which the Asset pick task is enabled. Otherwise thePrepare asset task is createddirectly without the Pick task. For details, see [Enable the Asset pick task for your stockroom in the Enterprise Asset Workspace](enable-pick-task-for-stockroom-eam.md).
4.  Select the **Enterprise Asset Refresh Line** tab.

5.  Select the enterprise asset refresh line.

6.  Select the **Refresh line tasks** tab.

7.  Complete the Asset pick task by using the Mobile Agent application.

    For details on completing this step, see [Locate and pick the enterprise assets in your stockroom using the Mobile Agent application](locate-and-pick-enterprise-asset-mobile-app.md).

8.  Prepare the asset.

    1.  Select the **Prepare asset** task.

    2.  In the **Asset** field, select the enterprise asset that you want to replace.

    3.  Select **Save**.

    4.  Select **Close Task**.

    -   A Schedule refresh task is created under the Refresh Line Tasks.
    -   The state of the Replacement asset changes to In stock.
    -   The substate changes to Reserved.
    -   The **Reserved for** field is populated with the requester details.
9.  Complete the Schedule refresh task.

    1.  Select the **Schedule refresh** task.

    2.  In the **Scheduled deployment date** field, select the date on which the new asset will be deployed.

    3.  Select **Close Task**.

    -   The Deploy new asset task is created under the Refresh Line Tasks.
    -   The state of the Replacement asset changes to In stock and the substate changes to Pending install.
10. Complete the Deploy new asset task.

    1.  Select the **Deploy new asset** task.

    2.  Confirm if you have reclaimed the old asset in the **Is reclaimed** list.

        -   If you’ve collected the aged asset, select **Yes**.
        -   If you didn’t collect the aged asset, select **No**.
    3.  Select **Close task**.

        **Note:** If you select **Yes** from the Is reclaimed list, then the Reclaim aged asset task is also closed by default.

    -   Reclaim aged asset task is created under the Refresh Line Tasks.
    -   The state of the replacement asset changes to In use.
    -   The allocations are transferred from the aged asset to the replacement asset.
11. Complete reclaiming the aged assets.

    1.  Select the **Reclaim aged asset** task.

    2.  Confirm if you have reclaimed the old asset in the **Is reclaimed** list.

        -   If you’ve collected the aged asset, select **Yes**.
        -   If you didn’t collect the aged asset, select **No**.
    3.  Select **Close task**.

    **Note:** You can cancel the enterprise asset Refresh Line either by selecting **Cancel** or by changing the **State** field to **Closed Incomplete** in the Refresh Line task.


## Result

After the aged enterprise asset is reclaimed, the following changes happen on the asset form:

-   The state of the aged asset changes to In stock.
-   The substate changes to Pending disposal.

