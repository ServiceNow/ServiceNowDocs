---
title: Managing expiring contracts for leased enterprise assets
description: You can use the Contract and lease management view to track and take action on leased enterprise assets that are nearing the end of their contracts. You can choose to return your leased enterprise assets, buy out your leased enterprise assets, or extend your lease contracts.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create and manage contracts for enterprise assets, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Managing expiring contracts for leased enterprise assets

You can use the Contract and lease management view to track and take action on leased enterprise assets that are nearing the end of their contracts. You can choose to return your leased enterprise assets, buy out your leased enterprise assets, or extend your lease contracts.

## Lease management flow

When a lease contract for a given enterprise asset is nearing its expiration, the Enterprise Asset Management application automatically sends out a notification informing you that the contract will be expiring soon. You can customize the timing, content, and recipients of this expiry notification by navigating to **System Notification** &gt; **Email** &gt; **Notifications** and then selecting **Contract Threshold breached** from the list of available email notifications.

After you receive an expiry notification for one of your lease contracts, you can begin the lease-end process for that contract.

**Note:** You can begin the lease-end process only for active lease contracts that are expiring within 90 days but do not have a **Substate** of **Expiring**. A **Substate** of **Expiring** indicates that the lease-end process for that contract has already begun.

When the lease-end process begins, the Enterprise Asset Management application automatically generates a Planning task that you must complete to specify what action you want to take on either the associated enterprise asset or the lease contract itself. You can choose to

-   return the enterprise asset to the asset vendor,
-   buy out the enterprise asset so that you can permanently add it to your asset inventory,
-   or extend the lease contract.

Based on the action that you select, you must then perform all subsequent tasks to complete the lease-end process and move the lease contract out of the expiring substate.

-   **[Begin the lease-end process for an expiring enterprise asset lease contract](../task/begin-lease-end-process-eam.md)**  
Initiate the lease-end process for an expiring enterprise asset lease contract so that you can return the associated enterprise asset, buy out the associated enterprise asset, or extend the lease contract.
-   **[Complete the Planning task for an expiring enterprise asset lease contract](../task/complete-leased-asset-planning.md)**  
Complete the Planning task for an expiring enterprise asset lease contract so that you can proceed with either returning the associated enterprise asset, buying out the associated enterprise asset, or extending the lease contract.
-   **[Return a leased enterprise asset](../task/return-leased-enterprise-asset.md)**  
Return a leased enterprise asset to the asset vendor before the corresponding lease contract expires.
-   **[Buy out a leased enterprise asset](../task/buy-out-leased-enterprise-asset.md)**  
Buy out a leased enterprise asset before the corresponding lease contract expires.
-   **[Extend the lease contract for an enterprise asset](../task/extend-enterprise-asset-lease-contract.md)**  
Extend the lease contract for an enterprise asset before it expires.

**Parent Topic:**[Create and manage contracts for enterprise assets](create-manage-enterprise-asset-contracts.md)

