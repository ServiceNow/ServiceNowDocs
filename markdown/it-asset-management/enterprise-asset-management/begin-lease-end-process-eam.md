---
title: Begin the lease-end process for an expiring enterprise asset lease contract
description: Initiate the lease-end process for an expiring enterprise asset lease contract so that you can return the associated enterprise asset, buy out the associated enterprise asset, or extend the lease contract.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing expiring contracts for leased enterprise assets, Create and manage contracts for enterprise assets, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Begin the lease-end process for an expiring enterprise asset lease contract

Initiate the lease-end process for an expiring enterprise asset lease contract so that you can return the associated enterprise asset, buy out the associated enterprise asset, or extend the lease contract.

## Before you begin

**Important:** You can begin the lease-end process only for active lease contracts that are expiring within 90 days but do not have a **Substate** of **Expiring**. A **Substate** of **Expiring** indicates that the lease-end process for that contract has already begun.

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## Procedure

1.  From the Enterprise Asset Workspace, open the Contract and lease management view.

2.  On the **Lease contracts** tab, select the lease contract for the enterprise asset that you want to return, buy out, or extend the contract for.

    The lease contract record opens.

3.  On the lease contract record header, select **Begin lease-end process**.

4.  When prompted to confirm that you want to begin the lease-end process for the contract, select **OK**.


## Result

The lease-end process for the specified lease contract begins. The Enterprise Asset Management application then automatically generates a Planning task for the lease contract.

## What to do next

Complete the Planning task for the lease contract so that you can specify what action you want to take on either the associated enterprise asset or the lease contract itself. See [Complete the Planning task for an expiring enterprise asset lease contract](complete-leased-asset-planning.md) for detailed instructions.

**Parent Topic:**[Managing expiring contracts for leased enterprise assets](../concept/managing-expiring-contracts-leased-assets.md)

