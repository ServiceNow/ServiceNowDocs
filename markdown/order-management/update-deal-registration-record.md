---
title: Update deal registration record
description: Create a deal registration record or perform actions on an existing record in the CSM Configurable Workspace, including submitting for approval and managing post-approval actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/update-deal-registration-record.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 6
breadcrumb: [Partner Workspace, Configure Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Update deal registration record

Create a deal registration record or perform actions on an existing record in the CSM Configurable Workspace, including submitting for approval and managing post-approval actions.

## Before you begin

Role required: sn\_prm\_dr.deal\_reg\_ui, Approver role \(sn\_adv\_appr\_mgmt.approval\_request\_approver\).

You must have one of the following roles:

-   Deal agents \(Enterprise B2B and B2C\): Create deals, Preview and submit for approval, manage tasks.
-   Enterprise Relationship Managers: Oversee deals under their hierarchy.
-   Enterprise Contributors: Manage deals for their channel partners.
-   Deal Registration Admin: Configure approval rules, manage all deal records and tasks.
-   Internal team members: Work on deal-related tasks \(account creation, compliance review, and so on\).

## About this task

After a deal is created on the Partner portal and is in the **Submitted** state, an agent on the **CSM/FSM Configurable Workspace** can see the same deal. The information in the fields is automatically populated from the Partner portal based on selections made by the deal registration initiator and deal registration manager.

## Procedure

1.  Navigate to the CSM/FSM Configurable Workspace and select the list view.

2.  Select **Deal Registration &gt; Submitted** to see a list of submitted deals.

    To learn how to create a deal and submit it, see [Register a deal on Partner portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/register-a-deal-partner-portal.md). The deal registration form details are auto-filled based on selections made in the Partner portal. The following roles can make these selections: B2B deal registration initiator \(sn\_prm\_dr.partner\_b2b\_deal\_reg\_initiator\), B2C deal registration initiator \(sn\_prm\_dr.partner\_b2c\_deal\_reg\_initiator\), deal registration initiator \(sn\_prm\_dr-partner\_deal\_reg\_initiator\), and deal registration manager \(sn\_prm\_dr.partner\_deal\_reg\_manager\).

3.  Open a deal record to view or update the details.

    The deal form displays all populated fields and available actions based on the current deal state.

4.  Review the deal information and perform one of the following actions based on your role and the deal state.

    1.  To assign a deal to yourself for review, select **Assign to me**.

        This action is available only to agent personas. When you assign a deal to yourself, the state changes to **Under Review**, and you can perform the following actions on the deal:

        -   **Reject** — Reject the deal and fill in the Closure notes.
        -   **Mark as Duplicate** — Mark the deal as a duplicate of another deal and fill in the Closure notes.
        -   **Cancel Deal Registration** — Cancel the deal registration entirely.
    2.  To submit the deal for approval, select **Preview &amp; Submit for Approval**.

        The approval plan comes from your administrator's configuration of approval rules and approval chains. The deal state changes to **Pending Approval**, and the system sends approval requests to designated approvers. For step-by-step instructions, see [Submit a deal for approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/submit-deal-for-approval.md).\[Omitted image "deal-states.png"\] Alt text: Deal states

        A preview modal opens showing which approvers receive the request and in what order. Review the approval chain to confirm all required approvers are listed in the correct sequence. The approval plan comes from your administrator's configuration of approval rules and approval chains. Select **Request approval** to submit the deal. The first approver in the chain receives a notification. You can track which approvers have been notified and which have acted on the request. Sequential approvers receive requests only after the previous step is approved.\[Omitted image "deal-approval.png"\] Alt text: Preview and request approval

5.  Submit the deal registration for approval.

6.  If you are an approver, review and approve or reject the deal.

    1.  Open the deal record and review all details on the **Details**, **Line Items**, and other tabs.

        Verify the information is correct before proceeding with your approval decision.

    2.  Navigate to the **Approvals** tab on the deal record.

        This tab displays the pending approval request and approval history.

    3.  Select the three dots menu and select **Approve** or **Reject**.\[Omitted image "deal-approve.png"\] Alt text: Approve or Reject the deal

        If needed, you can add comments to explain your decision.

    If you approved, the next approver in the chain \(if any\) receives a notification. If you rejected, the deal returns to the submitter. Sequential approval means the next step only begins after your approval. Comments are visible to the requester and other approvers. After all approvers in the chain approve, the deal moves to Approved state. If any approver rejects it, the deal moves to closed state with Rejected closure code.

    After the deal registration is approved, the state changes to **Approved**.

7.  After a deal is approved, you can perform one of the following actions on the approved deal.

    1.  To cancel the deal registration, select **Cancel Deal Registration**.

        Enter the closure notes to document the reason for cancellation. The closure code updates to **Rejected**. Use this action if the deal is no longer valid or the partner withdrew the registration.

    2.  To close the deal, select **Close**.

        Close a deal if there's been no activity for a period of time. The deal state changes to **Closed**, and the closure code updates to **Closed**. Closed deals are archived but remain visible in historical records.

    3.  To convert the deal to an opportunity, select **Convert to Opportunity**.

        Convert an approved deal to a CRM opportunity to begin the sales cycle. The deal state changes to **Closed**, and the closure code updates to **Converted**. All line items from the deal registration are automatically transferred to opportunity line items using Primitives.

        The deal registration is successfully converted to an opportunity. You can now manage the opportunity in the standard CRM sales pipeline.


## Result

The deal registration record is updated with the action you performed. Depending on the action:

-   Submitted for Approval: The deal moves to **Pending Approval**, and approvers receive notifications to review the deal.
-   Approved: The deal state becomes **Approved**, and you can perform post-approval actions.
-   Cancelled/Rejected: The deal state becomes **Closed** with a **Rejected** closure code, and the deal is removed from active workflows.
-   Converted to Opportunity: The deal is converted to a CRM opportunity, line items are transferred, and the deal workflow completes.

## What to do next

**Approval workflow details**

When you submit a deal for approval, the approval workflow evaluates the deal against configured approval rules. The workflow identifies required approvers based on deal attributes and organizational hierarchy, then sends notifications to those approvers. Approvers review the deal in their approval queue and can approve, reject, or request additional information.

For detailed information about the approval workflow, approval states, and approver responsibilities, see [Deal Registration approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/deal-registration-approvals-overview.md).

**Related topics**

-   [Deal Registration approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/deal-registration-approvals-overview.md)
-   [Submit a deal for approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/submit-deal-for-approval.md)
-   [Approval configuration setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/approval-configuration-setup.md)
-   [Register a deal on Partner portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/register-a-deal-partner-portal.md)

**Parent Topic:**[Partner Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/partner-workspace.md)

**Related topics**  


[Register a deal on Partner portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/register-a-deal-partner-portal.md)

