---
title: Contract approval flow
description: Use the Contract Approval flow to get approval from the approver defined in the contract. You can edit the existing flow or create a flow in the graphical Workflow Studio to meet your organization's contract approval process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/contract-management/contract-approval-workflow.html
release: australia
product: Contract Management
classification: contract-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [contract approval workflow]
breadcrumb: [Contract Management, IT Asset Management]
---

# Contract approval flow

Use the Contract Approval flow to get approval from the approver defined in the contract. You can edit the existing flow or create a flow in the graphical Workflow Studio to meet your organization's contract approval process.

## Prerequisites

Ensure that the Contract Management \(com.snc.contract\_management\) plugin is installed.

## Contract Approval flow

Submit your contract for approval by selecting an approver in the contract record. This workflow enables you to manage the terms and conditions the contract must meet to approve a contract.

\[Omitted image "contract-approval-workflow-actions.png"\] Alt text: Contract approval flow actions

## Contract approval process

-   Select an **Approver** for the contract and select **Submit for Review**. If the contract's end date is greater than the current date, an approval history record is automatically created to track the status of the approval process. For more information about sending a contract for approval, see [Send the contract for approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/contract-management/t_SendTheContractForApproval.md).
-   Access the contract approval history record and take an approval action. For more information about viewing the approval history for a contract, see [View approval history on contracts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/contract-management/t_ObtainContractApproval.md). Based on the approval decision on the contract, the state and substate of the contract is updated.

**Parent Topic:**[Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/contract-management/c_ContractManagement.md)

**Related topics**  


[Use the Asset Contract Overview module]()

[Components installed with Contract Management]()

[Contract Management use]()

[Condition check definitions]()

[Domain separation and Contract Management]()

[Send the contract for approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/contract-management/t_SendTheContractForApproval.md)

[Approve or reject a contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/contract-management/t_ApproveOrRejectAContract.md)

[View approval history on contracts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/contract-management/t_ObtainContractApproval.md)

