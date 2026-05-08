---
title: Approve or reject a contract renewal request
description: Approve or reject a contract renewal request for all Contract Renewal Request Lines.
locale: en-US
release: australia
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contract renewal workflow, Contract Management, IT Asset Management]
---

# Approve or reject a contract renewal request

Approve or reject a contract renewal request for all Contract Renewal Request Lines.

## Before you begin

The Renewal approver field must contain a value. If you need to change the approver, navigate to the parent contract and adjust the value there.

Role required: contract\_system\_admin, asset\_manager\(core UI and Hardware Asset Workspace only\), contract\_manager\(core UI or Hardware Asset Workspace only\), sn\_eam.enterprise\_admin \(Enterprise Asset Workspace only\), or sn\_eam.enterprise\_asset\_manager \(Enterprise Asset Workspace only\)

## Procedure

1.  Verify your contract renewal details.

    -   If you are using the core UI or Hardware Asset Workspace,select the **Open Tasks** tab on the Contract Renewal Request form. Select the contract renewal request number to view the contract renewal details and then click **Close Task**.
    -   If you are using the Enterprise Asset Workspace, open the Contract and lease management view. Select the **All contracts** tab and then open the enterprise asset contract that you want to renew. View the contract renewal details in the Renewal section of the **Details** tab.
    An approval request is triggered and the substate of the draft contract changes to Under review.

2.  Open the list of contract and contract renewal requests.

    -   If you are using the core UI or Hardware Asset Workspace,navigate to **All** &gt; **Contract** &gt; **My Approvals**.
    -   If you are using the Enterprise Asset Workspace, open the Contract and lease management view and then select the **My contract approvals** tab.
3.  Select the contract renewal request waiting for approval.

4.  Evaluate any contract renewal request lines and contract renewal tasks.

5.  Either approve or reject the contract renewal request.

<table id="choicetable_lcq_2fl_4tb"><thead><tr><th align="left" id="d78597e134">

Action

</th><th align="left" id="d78597e137">

Result

</th></tr></thead><tbody><tr><td id="d78597e143">

**Approve the request by selecting Approve**

</td><td>

-   The substate of the draft contract changes to Approved.
-   The Renewal purchase order task or the Manual purchase order task is created.


</td></tr><tr><td id="d78597e161">

**Reject the request by selecting Reject**

</td><td>

-   The renewal request gets terminated.
-   The substate of the draft contract changes to Renewal rejected.


</td></tr></tbody>
</table>6.  Go to the **Approval History** tab to view the approval or rejection history of the contract and child contracts.


## What to do next

[Receive a purchase order for contract assets](receive-po.md)

