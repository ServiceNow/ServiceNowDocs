---
title: Send the contract for approval
description: You can send a contract that is in Draft state for approval.
locale: en-US
release: yokohama
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Contracts, Contract Management use, Contract Management, IT Asset Management]
---

# Send the contract for approval

You can send a contract that is in **Draft** state for approval.

## Before you begin

Role required: admin, contract\_manager\(core UI and Hardware Asset Workspace only\), sn\_eam.enterprise\_admin \(Enterprise Asset Workspace only\), or sn\_eam.enterprise\_asset\_manager \(Enterprise Asset Workspace only\)

## Procedure

1.  Open the list of contracts that are used across your deployment.

    -   If you are using the core UI, navigate to **Contract** &gt; **Contracts** &gt; **All**.
    -   If you are using the Hardware Asset Workspace, open the Contract management view and then select the **All contracts** tab.
    -   If you are using the Enterprise Asset Workspace, open the Contract and lease management view and then select the **All contracts** tab.
2.  Select a contract in the **Draft** state and **Awaiting Review** substate.

3.  Select an **Approver** for the contract.

4.  Click **Submit For Review**.

    An email message is sent to the selected approver and the contract **Substate** changes to **Under Review**.


-   **[Approve or reject a contract](t_ApproveOrRejectAContract.md)**  
If you are the contract manager, you can approve or reject a contract.
-   **[View approval history on contracts](t_ObtainContractApproval.md)**  
You can view the approval history for a contract in the Approval History related list on the Contract form.

**Parent Topic:**[Contracts](../concept/c_Contracts.md)

**Related topics**  


[Create a contract](t_CreateAContract.md)

[Adjust a contract](t_AdjustAContract.md)

[Verify contract administrator assignment for notification](t_SendAContractNotification.md)

[Terms and conditions](../concept/c_TermsAndConditions.md)

[Create a contract rate card](t_ContractRateCardsAndExpenseLines.md)

[Monitor a contract](t_MonitoringContracts.md)

