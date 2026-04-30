---
title: Create entitlements in workspace
description: Create entitlements in the Software Asset Workspace to enter your license details and allocate purchased software rights to users or devices.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create entitlements in workspace

Create entitlements in the Software Asset Workspace to enter your license details and allocate purchased software rights to users or devices.

## Before you begin

These instructions are for using the standard form for creating software entitlements one at a time. You can also use the step by step approach of a [guided walk-through](guidedwalk-workspace.md) for creating entitlements. If you already have software entitlement details entered in a spreadsheet, you can also [import](import-entitlements-workspace.md) them using the bulk import functionality.

When you start creating the entitlement it is in the **build** status. Once you publish the entitlement, the status changes to **in use** and makes the entitlement eligible to be included in the reconciliation process.

If you installed SaaS License Management, a software model is generated automatically after you create an integration profile. Create an entitlement for the software model to track software used against software owned.

if you installed the SAP publisher pack, see [Create entitlements for SAP](create-entitlement-sap.md).

You can also create entitlements for RHEL and Citrix publisher packs. For details on the entitlement form fields for RHEL, see [Software Entitlement form](../concept/rhel-entitlements.md#table_cjg_xfn_mnb).

Role required: sam\_admin or sam\_user

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace**.

2.  Select **Create entitlement** to open the Create new entitlement dialog box.

    You can also navigate to the Create new entitlement dialog box from **Software asset** &gt; **Software Asset Workspace** &gt; **License operations**

    ![create entitlement using the standard form](../image/create-standard-entitlement.png)

3.  Select **Fill out the details in a standard form** and then select **Next**.

4.  In the Create New Software Entitlement page, fill in the fields.

    For a detailed description of the fields, see [Software entitlement fields](../reference/software-entitlement-fields.md).

5.  Select **Save**.

    After you save the entitlement, the **Allocations**, **General**, **Financial**, and **Contracts** tabs appear on the page. You can now add details in these related tabs.

6.  Once you have entered the required details, select **Publish**.

    The entitlement is created and state of the entitlement is changed to **in use** from **build**. The entitlement is ready to be picked up for the reconciliation process.

    You can perform additional configuration on the new entitlement by entering details in the other tabs such as Contracts, Downgrade Rights, Expense Lines, Entitlement History. For a detailed description of the fields in these tabs, see [Software entitlement fields](../reference/software-entitlement-fields.md).


-   **[Create maintenance entitlements in workspace](create-maint-entitlements-workspace.md)**  
Define license details, for all publishers other than Microsoft in the Software Asset Workspace. Create maintenance entitlements to manage all your software license maintenance needs such as start and end dates of your contracts and software upgrades.
-   **[Create Microsoft Software Assurance entitlements in workspace](create-sa-entitlements-workspace.md)**  
Define license details for Microsoft Software Assurance \(SA\) in the Software Asset Workspace to manage your contracts start and end dates, software upgrades, and related software entitlements.

**Parent Topic:**[Configuring Software Asset Workspace](../concept/Config-sam-workspace.md)

**Related topics**  


[Create device allocation](create-device-allocation.md)

