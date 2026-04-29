---
title: Add terms and conditions to a contract
description: After you create a terms and conditions record, add the record to a contract that is in the Awaiting Review, Rejected, Renewal Rejected, or Extension Rejected substate.
locale: en-US
release: australia
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Terms and conditions, Contracts, Contract Management use, Contract Management, Asset Management, IT Service Management]
---

# Add terms and conditions to a contract

After you create a terms and conditions record, add the record to a contract that is in the Awaiting Review, Rejected, Renewal Rejected, or Extension Rejected substate.

## Before you begin

Role required: admin, contract\_manager\(core UI and Hardware Asset Workspace only\), sn\_eam.enterprise\_admin \(Enterprise Asset Workspace only\), or sn\_eam.enterprise\_asset\_manager \(Enterprise Asset Workspace only\)

## About this task

Terms and Conditions can only be added to a contract when it is being created. After the contract is approved, the terms and conditions cannot be changed.

## Procedure

1.  Open the list of contracts that are used across your deployment.

    -   If you are using the core UI, navigate to **Contract** &gt; **Contracts** &gt; **All**.
    -   If you are using the Hardware Asset Workspace, open the Contract management view and then select the **All contracts** tab.
    -   If you are using the Enterprise Asset Workspace, open the Contract and lease management view and then select the **All contracts** tab.
2.  Select a contract.

3.  Add terms and conditions to the contract.

    -   If you are using the core UI, use the following steps:
        1.  In the **Terms and Conditions** related list, double-click **Insert a new row**.
        2.  Click the reference lookup icon and select a terms and conditions record from the list.
        3.  \(Optional\) Enter a number in **Order** to specify the sequence in which the record should appear in the terms and condition document.

            **Note:** If you attempt to enter a duplicate terms and conditions record for a contract and save the record, an error message appears and the new duplicate record is not added.

    -   If you are using the Hardware Asset Workspace, use the following steps:
        1.  On the **Terms and Conditions** tab, click **Add**.
        2.  When prompted, provide the required information.
    -   If you are using the Enterprise Asset Workspace, use the following steps:
        1.  On the **Terms and Conditions** tab, click **Add**.
        2.  In the dialog box, select the check box for each term and condition that you want to add.
        3.  Click **Add**.

**Parent Topic:**[Terms and conditions](../concept/c_TermsAndConditions.md)

**Related topics**  


[Create a terms and conditions record](t_CreateATermsAndConditionsRecord.md)

[Build a terms and conditions document within a contract](t_BuildTandCDocWinContract.md)

