---
title: Submit a deal for approval
description: Submit a deal for approval to route it through your organization's configured approval workflow and identify the approvers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/submit-deal-for-approval.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Deal Registration approvals, Deal Registration, Configure Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Submit a deal for approval

Submit a deal for approval to route it through your organization's configured approval workflow and identify the approvers.

## Before you begin

Role required: Deal Agent \(sn\_prm\_dr.enterprise\_b2b\_deal\_reg\_agent, sn\_prm\_dr.enterprise\_b2c\_deal\_reg\_agent\).

## About this task

As a deal agent, you can submit any deal for approval to route it through your organization's approval chain. The deal must be in the Under Review state to submit. When you submit a deal, the system checks configured trigger conditions to determine if approval is required and identifies appropriate approvers based on your approval rules.

## Procedure

1.  Open the deal record that you want to submit for approval in the CSM Configurable Workspace.

2.  Scroll to the Approvals section.

    The deal must be in **Under Review** state.

3.  In the deal record header, select **Preview &amp; Submit for Approval**.

4.  In the preview modal, review the list of potential approvers.

5.  Add a comment or message for the approvers in the **Message to approvers** field.\[Omitted image "deal-approval.png"\] Alt text: Approval plan

6.  Select **Request Approval** to submit the deal for approval.

    The system validates the deal information and submits it for approval. The deal automatically moves to **Pending Approval** state.The deal record is now locked for editing \(read-only\). Approvers are notified and review the deal according to your organization's approval workflow.

7.  Review the deals that have been submitted for approval by deal agents.

    Based on your organization's configured approval rules, you receive approval requests for deals that meet specified trigger conditions. Your role is to evaluate the deal information and decide whether to approve or reject the deal.

    **Note:**

    You must have the Approver role \(manually assigned by the deal registration admin\) to access and process approval requests. If you can't see approval requests, contact your deal registration admin to request the Approver role.


## Result

Your approval decision is recorded in the system. If you approved the deal and it was the final approval step, the deal is now in Approved state and ready for next steps. If you rejected it, the deal is Closed \(Rejected\) and the approval process ends permanently.

## What to do next

If the approval process includes multiple sequential steps, the next approver receives their approval request. Monitor the deal's approval progress by viewing the Approvals tab. Once all approvals are complete or the deal is rejected, the deal agent receives notification of the final outcome.

For more information, see [Deal Registration approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/deal-registration-approvals-overview.md).

**Parent Topic:**[Deal Registration approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/deal-registration-approvals-overview.md)

