---
title: Approve or reject a contract
description: If you are the contract manager, you can approve or reject a contract.
locale: en-US
release: xanadu
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Send the contract for approval, Contracts, Contract Management use, Contract Management, Asset Management, IT Service Management]
---

# Approve or reject a contract

If you are the contract manager, you can approve or reject a contract.

## Before you begin

Role required: admin, contract\_manager\(core UI and Hardware Asset Workspace only\), sn\_eam.enterprise\_admin \(Enterprise Asset Workspace only\), or sn\_eam.enterprise\_asset\_manager \(Enterprise Asset Workspace only\)

## Procedure

1.  Open the list of contract and contract renewal requests.

    -   If you are using the core UI, navigate to **All** &gt; **Contract** &gt; **My Approvals**.
    -   If you are using the Hardware Asset Workspace, open the Contract management view and then select the **My approvals** tab.
    -   If you are using the Enterprise Asset Workspace, open the Contract and lease management view and then select the **My contract approvals** tab.
2.  Select a contract in the **Requested** state.

3.  Approve or reject the contract.

    -   Approve the contract.
        -   To approve the contract in the core UI, click **Approve**. The contract **Substate** changes to **Approved**.
        -   To approve the contract in the Hardware Asset Workspaceor Enterprise Asset Workspace, set the **State** field to **Approved**.
    -   Reject the contract.
        -   To reject the contract in the core UI, click **Reject** and enter a rejection reason in the **Comments** field. The contract **Substate** changes to **Rejected**.
        -   To reject the contract in the Hardware Asset Workspaceor Enterprise Asset Workspace, set the **State** field to **Rejected**.
4.  Click **Update** \(core UI\) or **Save** \(Hardware Asset Workspaceand Enterprise Asset Workspace\).

    -   A contract with the state set to **Draft** and a start date set in the future is kept in **Draft** until the start date is reached. If the contract has a **Substate** of **Approved**, the system changes the **State** to **Active** and removes the **Substate** value.
    -   When a contract with a **State** of **Draft** and a **Start Date** set to a date in the past is approved, the contract **State** is automatically set to **Active** and **Substate** is left blank.

**Parent Topic:**[Send the contract for approval](t_SendTheContractForApproval.md)

