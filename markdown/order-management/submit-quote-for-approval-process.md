---
title: Submit a quote for approval
description: Submit a quote for approval when you have configured approval rules that require authorization before the quote can be completed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/submit-quote-for-approval-process.html
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 3
keywords: [approvals, quote, submit, workflow]
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Submit a quote for approval

Submit a quote for approval when you have configured approval rules that require authorization before the quote can be completed.

## Before you begin

Role required: sn\_adv\_appr\_mgmt.approval\_request\_writer or sn\_adv\_appr\_mgmt.approval\_request\_approver

**Important:** Before submitting quotes for approval, ensure that your administrator has completed the following setup tasks:

-   [Set up the environment to manage approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/setup-approvals-prerequisites.md) - Install required plugins and enable approval tenant settings
-   [Create an approval configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-approval-configuration.md) - Create approval configurations with trigger conditions and rules
-   [Define an approval user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-approval-users.md) - Assign approvers for the configured approval rules

## About this task

When you create or modify a quote, the approval engine automatically evaluates whether the quote meets any configured approval conditions. If one or more conditions are met, you must submit the quote for approval before it can proceed to the completed state.

Before submitting, you can preview which approvals are required and who will review your quote. This helps you understand the approval chain and any conditions that triggered the approval requirement.

Approvals are triggered based on conditions configured by your approval administrator. Common examples include:

-   Account-based triggers: Approvals required for specific customer accounts \(for example, VIP accounts or accounts requiring compliance review\)
-   Discount triggers: Approvals required when quote discounts exceed configured thresholds
-   Price adjustment triggers: Approvals required for line-level price modifications
-   Custom triggers: Any other business conditions configured by your organization

If your quote does not meet any configured approval conditions, the approval framework automatically approves the quote without requiring manual review. You can proceed directly to completing the quote.

## Procedure

1.  Open the quote you want to submit for approval.

2.  Click the **Request Approval** button.

    A preview panel appears showing:

    -   All approval rules that apply to your quote
    -   The trigger conditions that activated each approval \(for example, "Account Exception" or "Discount Tier 1: 0-69.99%"\)
    -   The approver names or groups assigned to each approval rule
    -   The sequence in which approvals will be routed \(sequential approval chains\)
3.  Review the approval preview to confirm the required approvers and approval sequence.

    The preview shows:

    -   First approval: The initial approver or group that will receive your request
    -   Subsequent approvals: Approvers who will receive the request after the previous step is approved
    -   Parallel approvals: Multiple approvers who can approve simultaneously \(when configured with OR logic\)
    -   Sequential approvals: Approvers who must approve in order \(when configured with AND logic\)
4.  If you want to make changes to your quote before submission, click **Cancel** to close the preview and edit your quote.

    After making changes, click **Request Approval** again to see the updated approval requirements.

5.  When you are ready to submit your quote for approval, click **Submit** in the approval preview.

    Your approval request is submitted. A confirmation message appears, and the quote status changes to "Pending Approval." The approval engine routes your request to the first assigned approver.

    **Note:** If your quote was already approved previously and you are resubmitting without significant changes, the system may use **smart approvals** to skip re-approval if this feature is enabled. Contact your administrator for details.

6.  Click **View Approval** to track the status of your submitted request.

    A panel shows:

    -   The current approval request status
    -   Each approver assigned to your request
    -   Which approvers have already reviewed your quote
    -   Approval history from any previous requests

## What to do next

After submitting your quote for approval:

-   Monitor the approval status using the **View Approval** button
-   If an approver rejects your quote, you can make revisions and resubmit \(see [Reject or return a quote for revision](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/reject-or-return-quote-for-revision.md)\)
-   If all required approvers approve your quote, proceed to complete the quote transaction.

**Parent Topic:**[Using Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-advanced-approval-management.md)

