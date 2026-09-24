---
title: Manage your expiring contracts for leased hardware assets
description: Use the lease contract expiration flow and decide on what to do before your leased hardware asset contract expires. Get notifications about the lease contracts that are nearing their expiration dates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/manage-your-leased-hw-asts-expiring-contract.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Asset lifecycle and disposal, Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Manage your expiring contracts for leased hardware assets

Use the lease contract expiration flow and decide on what to do before your leased hardware asset contract expires. Get notifications about the lease contracts that are nearing their expiration dates.

## Before you begin

Role required: contract\_manager

## About this task

When a lease contract is nearing its expiration, contract administrators and business owners are notified 90, 60, and 30 days before the expiration date. Getting these notifications early can help give them enough time to act and to avoid paying a penalty. You can customize the email notifications by navigating to **System Notification** &gt; **i** &gt; **Notification** &gt; **Lease contract threshold breached**.

You can view a consolidated list of asset contracts that are expiring on the Hardware Asset Dashboard in the month, quarter, and year formats. For more information, see [Hardware Asset Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/hardware-asset-content-pack.md).

**Note:**

When the Hardware Asset Management license is activated, the **Renew** UI button doesn't appear for active lease contracts that have assets covered.

If an asset is associated with more than one lease contract, then the **Lease contract** field on the asset record reflects the most recently associated contract.

There are readily available decision tables that you can use to customize the Lease Contract Expiration Flow, Leased Asset Buyout Flow, Leased Asset Extension Flow, and Leased Asset Return Flow. For more details, see [Hardware Asset Management flow customization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/readily-available-dec-tables-ham.md).

With the lease contract expiration flow, the possible lease actions are buying out the leased asset, extending the lease agreement, or returning the asset or another like product.

**Note:** For an asset covered, if the **Date removed** field is in the past, then the state of the asset is automatically set to Canceled and you can’t take any lease actions.

## Procedure

1.  Navigate to **Contract** &gt; **Contracts** &gt; **Leases**.

    The Lease page opens. It shows a list of lease contracts.

2.  Open the relevant active lease contract and click the **Begin Lease expiration process** related link.

    **Note:**

    The **Begin Lease expiration process** related link is visible only in active contracts that have at least one asset covered.

    You can't choose a lease action such as Buy out, return, and extend for an excluded lease asset. For more information, see [Hardware Asset Management license exclusion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/ham-license-exclusion.md).

    The Leased Assets related list shows all the hardware assets that are covered in the lease contract.

    In each asset record that is covered under the lease agreement, a Planning task is generated. The Planning task is automatically assigned to the contract administrators.

3.  Under the Leased Assets related list, perform any of the following to take a lease action:

    -   Open a record and then open the Planning task. In the Planning task, select a lease action from the Lease action list.
    -   Open an asset. From the Asset Covered form, select a wanted lease action from the Lease action list.
    -   On the list of assets, double-click the **Lease action** field of an asset and select a lease action.
    A set of tasks is created. If you select a lease action by a method other than opening the Planning task, then the state of Planning task is automatically moved to Closed.

    **Note:** By default, the Planning tasks are created only for the first 1000 assets under the contract. If you want to create Planning tasks for more than 1000 assets, then you can change the default value \(1000\) of the **com.sn\_hamp.flow.lease\_contract\_expiration.max\_results** key in the Asset Property \(asset\_property.list\) table. Only users with the asset role can change this property.


## Result

Based on your selected action, the corresponding workflow is triggered and the associated Contract Asset tasks are created. Close one task to go to the next task.

## What to do next

Based on what lease action you selected, perform any of the following:

-   [Return your leased hardware asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/return-your-leased-hardware-asset.md).
-   [Buy out your leased hardware asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/purchase-your-leased-hw-asset.md).
-   [Extend your lease contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/extend-your-lease-contract.md).

-   **[Return your leased hardware asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/return-your-leased-hardware-asset.md)**  
Return your hardware asset before the contract expires and avoid paying a penalty.
-   **[Buy out your leased hardware asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/purchase-your-leased-hw-asset.md)**  
Buy out your leased hardware asset before the contract expires and avoid paying a penalty.
-   **[Extend your lease contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/extend-your-lease-contract.md)**  
Extend your lease contract before the contract expires and avoid paying a penalty.

**Parent Topic:**[Asset lifecycle and disposal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/asset-lifecycle-disposal-ham.md)

**Related topics**  


[Request a Hardware Asset Refresh]()

[Manage refresh of assets using Zero Touch Refresh]()

[Reclaim hardware assets]()

[Create a disposal order]()

[Donate assets to charity organizations]()

[Manage asset bundles from your inventory]()

[Manage obligations in the Hardware Asset Workspace]()

[Manage contract repository agentic workflow in the Hardware Asset Workspace]()

