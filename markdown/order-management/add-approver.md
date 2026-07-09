---
title: Add ad-hoc approvers to an approval request
description: As a requester or an approver, add one or more ad-hoc approvers to an approval request in Advanced Approval Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/add-approver.html
release: australia
topic_type: task
last_updated: "2026-06-28"
reading_time_minutes: 2
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Add ad-hoc approvers to an approval request

As a requester or an approver, add one or more ad-hoc approvers to an approval request in Advanced Approval Management.

## Before you begin

The person or group to be added as an ad hoc user must be defined as an advanced approval user or advanced approval group by your advanced approval admin.

Role required: sn\_adv\_appr\_mgmt.approval\_request\_writer or sn\_adv\_appr\_mgmt.approval\_request\_approver

## About this task

After an approval request has been submitted, you \(as a requester or approver\) can add other approval users or approval groups to an approval request. Add approvers when the request requires approval by others who are familiar with the rules or business guidelines relevant to the request, but were not included as original approvers.

When you add an ad-hoc approver, you can choose to add the approver to a General chain for the approval request. Or, you can specify an existing chain to which the ad-hoc approver is added and the rule order for step to be added to the chain. The approval engine validates the chain and rule order values, allowing ad-hoc approvers to be added only to chains that have not yet been triggered and approved.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the \[Omitted image "list-outline-24.svg"\] Alt text:List icon.

3.  Navigate to the approval request.

    Access the request by navigating to the transaction entity, and then select the entity, such as a quote for which an approval request was submitted. Select the Approvals tab for the transaction to open the approval workflow interface.

4.  Select **Add Approver**.

5.  In the Add ad-hoc approver dialog box:

    1.  Select **Approver\(s\)** or **Approver group**.

    2.  In the **Approver\(s\)** or **Approver group** field, enter the approver users or approver group.

    3.  In **Approval criteria**, select Anyone or All to indicate the approvers required.

    4.  In the Approval chain field, select the chain to which the approver is being added.

        If you don’t select a chain, the approver\(s\) or approval group is added to the General chain, which is displayed at the top of the approval workflow.

    5.  In the **Rule order** field, enter the numeric value of the approval step to which the ad-hoc approver is being added.

    6.  In **Comment to approvers**, enter the reason for adding approvers or approval groups.

    7.  Select **Add**.

    The approval engine verifies that the chain and rule order specified have not yet been triggered and approved. If valid, the ad-hoc approvers are added to the approval workflow in the rule order specified for the step.


## Result

The ad-hoc approver can approve or reject the approval request in one of the following ways:

-   From the simple Advanced Approval notification received informing the ad-hoc approver of the approval request.
-   In the approval step card in the chain, by selecting the **More options** \[Omitted image "icon-three-dots.png"\] Alt text: menu and choosing the **Approve** or **Reject** option.
-   In the My approvals feature in the ServiceNow AI Platform.

**Parent Topic:**[Using Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-advanced-approval-management.md)

