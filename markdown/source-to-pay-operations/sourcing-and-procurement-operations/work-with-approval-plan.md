---
title: Monitor an approval plan
description: During evaluation, the approval engine converts each approval rule into one or multiple approval plans. You can monitor approval plans to understand how the overall approval process is being executed, the routing and decision methods, the list of approvers involved, the status on the approvals, the list of purchase lines the approval is planned for, and so on.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Monitor an approval plan

During evaluation, the approval engine converts each approval rule into one or multiple approval plans. You can monitor approval plans to understand how the overall approval process is being executed, the routing and decision methods, the list of approvers involved, the status on the approvals, the list of purchase lines the approval is planned for, and so on.

## Before you begin

To monitor an approval plan, you must have already defined an approval rule. For more information on how to create approval rules, see [Create an approval rule](create-approval-rule.md). You can review and update the plans if required. Approval plans are not created manually.

Role required: sn\_shop.procurement\_administrator

## About this task

You can monitor approval plans to understand how the overall approval process is being executed, from the Sourcing and Purchasing Automation module.

## Procedure

1.  Navigate to **All** &gt; **Sourcing and Purchasing Automation** &gt; **Administration ** &gt; **Approval Plan **.

2.  Select a record.

3.  On the form, review these fields.

    |Field|Description|
    |-----|-----------|
    |Number|System-generated unique identifier for the approval plan.|
    |Approval Rule|The approval rule you want to reference for this plan.|
    |Purchase requisition number|The unique identifier for the record on which this approval plan is applied.|
    |Approver list|User or users responsible for approving the plan.|
    |Approver group list|List of groups containing the users responsible for approving the plan.|
    |Approval routing method|Method of routing the approvals. The options are sequentially and in parallel.|
    |Approval decision method|Method of approving the rule. You can select if all approvers must approve the rule or any approval can approve it.|
    |Approval|Status of the approval plan request. The options are Not Yet Requested, Requested, Approved, and Rejected.|
    |State|Work status on the requested approval plan. The options are Pending, Open, Work in Progress, Closed Complete, Closed Incomplete, and Closed Skipped.|
    |Purchase requisition line\(s\)|List of the purchase lines that the approval is planned for.|
    |Primary contact|Business owner of the purchase who can be contacted with questions about the purchase. This field is automatically populated on creation of an approval plan with the referenced business owner of the purchase order.|
    |Short description|Short description of the approval plan. This is a calculated value, in the format: Approve &lt;total amount&gt; purchase for &lt;supplier name&gt;.|


## What to do next

Use the related lists of the approval plan form to view the approval plan details and approvers associated with this approval plan.

**Parent Topic:**[Sourcing and Purchasing Automation](../reference/purchase-experience-workflow.md)

