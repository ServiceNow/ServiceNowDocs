---
title: Add or remove assets for a contract renewal
description: Add or remove hardware or enterprise assets from the contract renewal process. You can also view the hardware or enterprise assets carried over to the new contract.
locale: en-US
release: zurich
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Contract renewal workflow, Contract Management, IT Asset Management]
---

# Add or remove assets for a contract renewal

Add or remove hardware or enterpriseassets from the contract renewal process. You can also view the hardware or enterpriseassets carried over to the new contract.

## Before you begin

To add or remove hardware assets from the contract renewal process, request the Hardware Asset Management application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).To add or remove enterprise assets from the contract renewal process, request the Enterprise Asset Management application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

Role required: asset, contract\_manager\(core UI and Hardware Asset Workspace only\), sn\_eam.enterprise\_admin \(Enterprise Asset Workspace only\), or sn\_eam.enterprise\_asset\_manager \(Enterprise Asset Workspace only\)

## About this task

The active and valid assets from the contract that are being renewed are carried over to the new contract, and are listed in the Assets Covered tab. Valid hardware and enterpriseassets are the assets that are not removed from the contract before the end date, and are in the following states or substates:

-   State
    -   In stock
    -   In transit
    -   In maintenance
    -   In use
-   Substate
    -   Available
    -   Reserved
    -   Pending transfer
    -   None
    -   Pending repair
    -   Pending install

Invalid assets are not carried over to the draft contract and you must add them manually.

## Procedure

1.  Open the assets selection task or contract for which you want to add assets.

    -   If you are using the core UI or Hardware Asset Workspace,select the assets selection task number on the Contract Renewal Request Line form.
    -   If you are using the Enterprise Asset Workspace, open the Contract and lease management view. Select the **All contracts** tab and then open the contract that you want to add assets to.
2.  Select the **Assets Covered** tab.

3.  If you are using the core UI or Hardware Asset Workspace,click **Edit**.

4.  Update the hardware or enterpriseassets in the contract.

<table id="choicetable_ftz_d1c_qtb"><thead><tr><th align="left" id="d165571e172">

Interface

</th><th align="left" id="d165571e175">

Action

</th></tr></thead><tbody><tr><td id="d165571e181">

**Core UI**

</td><td>

Indicate the assets that you want to cover by moving assets to the **Assets Covered List** or removing them.

</td></tr><tr><td id="d165571e193">

**Hardware Asset Workspace**

</td><td>

Add or remove assets from the existing list to indicate the assets you want to cover.

 -   To add an asset, select **Add** and provide the required asset information.
-   To remove an asset, select it and select **Remove**.


</td></tr><tr><td id="d165571e220">

**Enterprise Asset Workspace**

</td><td>

Add or remove assets from the existing list to indicate the assets you want to cover.

 -   To add an asset, click **Add**. In the Add assets dialog box, select the check box for each asset that you want to add and then click **Add**.
-   To remove an asset, select the check box for that asset and then click **Remove**.


</td></tr></tbody>
</table>5.  Select **Save**.

6.  Edit the renewal cost of the assets.

    **Note:** This step is applicable only if you are using the core UI or Hardware Asset Workspace.

    1.  Select the asset that you want to update the renewal cost for.

    2.  In the **Renewal cost** field, update the renewal cost of the asset.

    3.  Click **Update**.

7.  Click **Save**.

8.  If you are adding assets through the asset selection task on the Contract Renewal Request Line form, click **Close Task**.


## Result

The Payment amount field in the Financial tab of the draft contract shows the total renewal cost of the hardware or enterprise assets you selected.

## What to do next

[Add or remove entitlements for a contract renewal](select-sw-asset.md)

