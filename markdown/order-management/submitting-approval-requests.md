---
title: Working with approval requests as a requester
description: As a requester with the approval request writer role, when you submit your request for approval, you preview it, then request approval. You can also recall a request if you need to make changes or update a request if it was rejected, then resubmit it for approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/submitting-approval-requests.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Working with approval requests as a requester

As a requester with the approval request writer role, when you submit your request for approval, you preview it, then request approval. You can also recall a request if you need to make changes or update a request if it was rejected, then resubmit it for approval.

## Previewing and submitting approval requests

When a business item such as a customer quote is ready for approval, you can submit an approval request from the Sales Customer Relationship Management application for the entity, for example Quote Management. When you select the **Preview and Submit for approval** option, a preview of your request and the approval workflow opens. You can see the approval conditions that will be used to evaluate your request, the approval steps in the process, and the approvers who review your request. After reviewing the approval workflow, select **Request Approval** to generate the request.

\[Omitted image "approval-preview.png"\] Alt text: Approval request preview that shows approval steps and approvers in the Sales chain and the approval step and approvers for Finance

## Recalling approval requests

If you need to change an approval request after you submit it for approval, you can recall the approval request using the **Recall approval request** option in the quote header. Recalling an approval request cancels any pending approval steps and returns the request to a draft state where it can be updated.

Recalling a request helps prevent approvers from continuing to review outdated information while you address issues before resubmitting the request for approval.

## Resubmitting rejected or recalled approval requests

If you recalled an approval request or your request was rejected, you can revise it and resubmit the request for approval. For example, when you resubmit an approval request for a quote, the approval engine reevaluates the request and determines which approval steps must run again based on the configured rules and conditions.

Approval steps that are unaffected by the changes might be automatically approved \(smart reapprovals\) depending on the reapproval conditions set by your approval admin. But approval steps affected by the changes are routed again to the appropriate approvers. This helps reduce unnecessary reapprovals while ensuring that all required conditions are met before the quote is approved.

Once all required approval steps are approved, your business item, such as the quote that was approved, can proceed to the next stage of the sales process.

## Adding ad-hoc approvers to an approval request

As a requester, you can add one or more approvers or approval groups to a chain when an approval request requires approval by others who are familiar with the rules or business guidelines relevant to the request, but outside of the original approvers.

By default, ad-hoc approvers are added to the General chain, but you can add an ad-hoc approver to an existing approval chain and specify the order \(step\) to which the approver is added. For details on adding ad-hoc approvers, see [Add ad-hoc approvers to an approval request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/add-approver.md).

## Overriding an approval step

There may be times when an approval is no longer required. If you're a requester who also has the approval admin role, you can override or bypass a pending approval request step to unblock an approval request when the approval is no longer required. For more information, see [Override an approver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/override-approval-step.md).

**Parent Topic:**[Using Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-advanced-approval-management.md)

