---
title: Deal Registration approvals
description: Enable deal agents to submit deals for approval through a configurable approval workflow built on the Advanced Approval Management framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/deal-registration-approvals-overview.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 4
breadcrumb: [Deal Registration, Configure Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Deal Registration approvals

Enable deal agents to submit deals for approval through a configurable approval workflow built on the Advanced Approval Management framework.

## Deal approvals overview

Deal registration approvals provide a flexible, configurable workflow to route deals through your organization's approval process. Instead of hard-coded approvers and fixed conditions, you can define custom approval rules based on deal characteristics to ensure that the right approvers review each deal.

Deal approvals help your organization by:

-   Verifying that deals meet business criteria before approval
-   Routing deals to the appropriate reviewers based on deal characteristics
-   Maintaining an audit trail of all approval decisions
-   Enabling flexible approval workflows that adapt to business needs

## How approvals work

The deal approval process follows these steps:

1.  Agent creates a deal and submits it for approval from the **Under Review** state.
2.  System evaluates whether approval is needed based on configured rules.
3.  System identifies approvers based on the triggered approval rule.
4.  System sends approval requests to the designated approvers.
5.  Deal moves to **Pending Approval** state while awaiting approval.
6.  Approvers review the deal and select **Approve** or **Reject**.
7.  Deal moves to **Approved** or **Closed \(Rejected\)** based on the decision.

## Key approval components

The deal registration approval workflow consists of the following components:

|Component|Description|
|---------|-----------|
|Approval Rules|Define the conditions and approvers for a deal submission. Each rule specifies when it applies and who should approve.|
|Trigger Conditions|Specify when a deal requires approval, for example, deal size less than $1 million. When a condition is met, its associated approval rule is triggered.|
|Approval Requests|Automatically created when a deal is submitted for approval. Each request tracks the approvers and approval steps.|
|Approval Steps|Sequential stages within an approval request. Each step represents a single approver's decision point.|
|Approvers|Users designated to review and approve or reject deals. Approvers must be manually assigned the Approver role.|
|Approval Reminders|Automatic notifications sent to approvers about pending approval requests based on configured frequency.|

## Deal states and transitions

|State|Description|Transitions To|Available Actions|
|-----|-----------|--------------|-----------------|
|Draft|Deal has been created but not yet submitted for review or approval|Submitted|Edit deal, Submit, Delete.|
|Submitted|Deal has been submitted for initial review by internal team|Under Review, Canceled|Create tasks, Add work notes, Move to Under Review.|
|Under Review|Deal is being evaluated by the internal team. Submit for approval from this state|Pending Approval, Closed, Canceled|Create tasks, Preview &amp; Submit for approval, Add work notes.|
|Pending Approval|Deal is routed through the approval workflow and is awaiting approver decisions|Approved, Closed \(Rejected\)|View **Approvals** tab, Create tasks, Add work notes \(record is read-only\).|
|Approved|Deal has received all required approvals and is cleared to move forward. Record is editable|Closed, Canceled|Create opportunity, Create tasks, Add work notes, Move to Closed or Canceled.|
|Closed|Deal work is completed and opportunity has been created|None|View only \(read-only state\).|
|Canceled|Deal has been canceled and is no longer active|None|View only \(read-only state\).|

## Approval personas and roles

Three main personas are involved in the approval workflow based on the Advanced Approval Management.

-   Deal agents \(Enterprise B2B and B2C\): Submit deals for approval. The **Approval Request Writer** role is inherited from the Advanced Approval Framework. Can submit any deal for approval, beyond deals they created.
-   Deal registration admin: Configure approval rules, trigger conditions, and approver groups. The **Approval Rule Admin** role is inherited from the Advanced Approval Framework.
-   Approvers: Review and approve or reject the submitted deals. Must be manually assigned the **Approver** \(sn\_adv\_appr\_mgmt.approval\_request\_approver\) role by the deal registration admin to access approval requests.

**Note:**

-   Unlike other roles, the approver role must be manually assigned by the admin to each user who approves deals. This is critical—without this role, approvers can't access approval requests.
-   Demo approval configuration is not included in this release. You must configure your own approval rules and trigger conditions.
-   Deal approval is available in CSM Configurable Workspace Partner Workspace, not on the Partner portal.

## Deal states during approval

A deal moves through specific states during the approval process:

-   Under Review: Deal is created and in initial state. Deal agents can submit for approval from this state.
-   Pending Approval: Deal is submitted and is awaiting approver decisions. Deal record is read-only to prevent changes during review.
-   Approved: All approval steps are complete and deal is approved. Deal can move to Closed or be further modified.
-   Closed \(Rejected\): An approver rejected the deal, ending the approval process. Deal can't be re-approved.\[Omitted image "deal-states.png"\] Alt text: Different states of deal registration

-   **[Submit a deal for approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/submit-deal-for-approval.md)**  
Submit a deal for approval to route it through your organization's configured approval workflow and identify the approvers.
-   **[Approval configuration setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/approval-configuration-setup.md)**  
Configure deal registration approval rules, trigger conditions, approver groups, and reminders to implement your organization's approval workflow.

**Parent Topic:**[Deal Registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/deal-registration-management.md)

