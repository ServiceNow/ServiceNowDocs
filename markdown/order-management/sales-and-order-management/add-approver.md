---
title: Add approvers to an approval request
description: As a requester or an approver, add one or more ad-hoc approvers to an approval request in Advanced Approval Management.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 1
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Use, Sales and Order Management]
---

# Add approvers to an approval request

As a requester or an approver, add one or more ad-hoc approvers to an approval request in Advanced Approval Management.

## Before you begin

Role required: sn\_adv\_appr\_mgmt.approval\_request\_writer or sn\_adv\_appr\_mgmt.approval\_request\_approver

## About this task

After an approval request has been submitted, you can add approval users or approval groups to an approval request. Add approvers when the request requires approval by others who are familiar with the rules or business guidelines relevant to the request, but outside of the original approvers.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the ![](../../../reuse/icons/product-icons/list-outline-24.svg)List icon.

3.  Navigate to the approval request.

    Access the request by navigating to the transaction entity, and then select the entity, such as a quote for which an approval request was submitted. Select the Approvals tab for the transaction to open the approval workflow interface.

4.  Select **Add Approver**.

5.  In the Add ad-hoc approver dialog box:

    1.  Select **Approver\(s\)** or **Approver group**.

    2.  In the **Approver\(s\)** or **Approver group** field, enter the approver users or approver groups.

    3.  In **Approval criteria**, select Anyone or All to indicate the approvers required.

    4.  In **Comment to approvers**, enter the reason for adding approvers or approval groups.

    5.  Select **Add**.

    The ad-hoc approvers are added as approvers to the approval workflow. A step card in the General chain is added at the top of the workflow interface, identifying approvers in the Ad-hoc Approval step.


## Result

The ad-hoc approver can approve or reject the approval request in one of the following ways:

-   In a simple Advanced Approval notification for the approval user or approval group.
-   In the approval step card in the General chain, by selecting the **More options** ![](../image/icon-three-dots.png) menu and choosing the **Approve** or **Reject** option.
-   In the My approvals feature in the ServiceNow AI Platform.

**Parent Topic:**[Using Advanced Approval Management](../concept/using-advanced-approval-management.md)

