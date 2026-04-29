---
title: Submitting approval requests
description: As a requester with the approval request writer role, when you submit your request for approval, you preview it, then request approval. You can also recall a request if you need to make changes or update a request if it was rejected, then resubmit it for approval.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Use, Sales and Order Management]
---

# Submitting approval requests

As a requester with the approval request writer role, when you submit your request for approval, you preview it, then request approval. You can also recall a request if you need to make changes or update a request if it was rejected, then resubmit it for approval.

## Previewing and submitting approval requests

When a business item such as a customer quote is ready for approval, you can submit an approval request from the Sales and Order Management application for the entity, for example Quote Management. When you select the **Preview and Submit for approval** option, a preview of your request and the approval workflow opens. You can see the approval conditions that will be used to evaluate your request, the approval steps in the process, and the approvers who review your request. Select **Request Approval** to generate the request.

![Approval request preview that shows approval steps and approvers in the Sales chain and the approval step and approvers for Finance](../image/approval-preview.png "Preview approval request")

## Recalling approval requests

After you submit a request for approval, you can recall the approval request using the **Recall approval request** option if changes are required. Recalling an approval request cancels any pending approval steps and returns the request to a draft state where it can be updated.

Recalling a request helps prevent approvers from continuing to review outdated information and allows you to address issues before resubmitting the request for approval.

## Resubmitting rejected or recalled approval requests

If you recalled an approval request or a request was rejected, you can revise it and resubmit for approval. For example, when you resubmit an approval request for a quote, the approval engine reevaluates the request and determines which approval steps must run again based on the configured rules and conditions.

Approval steps that are unaffected by the changes might be automatically approved \(smart reapprovals\) depending on the reapproval conditions set by your approval admin. But approval steps affected by the changes are routed again to the appropriate approvers. This helps reduce unnecessary reapprovals while ensuring that all required conditions are met before the quote is approved.

Once all required approval steps are approved, your business item, such as the quote that was approved, can proceed to the next stage of the sales process.

## Adding ad-hoc approvers to an approval request

As a requester, you can add one or more approvers or approval groups to a chain named General, when an approval request requires approval by others who are familiar with the rules or business guidelines relevant to the request, but outside of the original approvers. For details on adding ad-hoc approvers, see [Add approvers to an approval request](../task/add-approver.md).

## Overriding an approval step

There may be times when an approval is no longer required. If you're a requester who also has the approval admin role, you can override or bypass a pending approval request step to unblock an approval request when the approval is no longer required. For more information, see [Override an approver](../task/override-approval-step.md).

**Parent Topic:**[Using Advanced Approval Management](using-advanced-approval-management.md)

