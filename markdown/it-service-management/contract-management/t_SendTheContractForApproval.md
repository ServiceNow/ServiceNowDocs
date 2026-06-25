---
title: Send the contract for approval
description: You can send a contract that is in Draft state for approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/contract-management/t\_SendTheContractForApproval.html
release: australia
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contracts, Contract Management use, Contract Management, Asset Management, IT Service Management]
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


-   **[Approve or reject a contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/contract-management/t_ApproveOrRejectAContract.md)**  
If you are the contract manager, you can approve or reject a contract.
-   **[View approval history on contracts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/contract-management/t_ObtainContractApproval.md)**  
You can view the approval history for a contract in the Approval History related list on the Contract form.

**Parent Topic:**[Contracts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/contract-management/c_Contracts.md)

**Related topics**  


[Create a contract]()

[Adjust a contract]()

[Verify contract administrator assignment for notification]()

[Terms and conditions]()

[Create a contract rate card]()

[Monitor a contract]()

[Contract approval flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/contract-management/contract-approval-workflow.md)

