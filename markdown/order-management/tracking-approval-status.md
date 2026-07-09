---
title: Tracking approval status and history
description: Monitor the progress of an approval request as it moves through the steps in an approval workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/tracking-approval-status.html
release: australia
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 2
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Tracking approval status and history

Monitor the progress of an approval request as it moves through the steps in an approval workflow.

## Approval workflow interface

After a requester submits an approval request, users involved in the approval process can view and track the approval request steps for the entity in the CSM Configurable Workspace. For example, in a quote approval workflow, the requesters, approvers, and users with view access can navigate to the quote and access the approval workflow interface from the Approvals tab.

The approval workflow interface provides an audit trail of each approval step, including the rule, assigned approvers, actual approvers \(for completed steps\), approval comments, and assignment and completion timestamps.

\[Omitted image "approval-workflow-interface.png"\] Alt text: Approval workflow for a quote. The following table describes key elements of the interface.

<table id="table_g4c_qq5_m3c"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Quote state

</td><td>

Quote state:-   Draft: Initial state of the quote. Editable by agent.
-   In Review: Quote has been submitted for approval. Not editable by agent unless the quote is recalled by the agent, or the quote has been approved or rejected.
-   Approved: Approvals for the quote are complete.
-   Rejected: Quote rejected by an approver. Editable by agent so that it can be revised and resubmitted for approval.

</td></tr><tr><td>

2. Approvals tab

</td><td>

Related list for the entity, such as a quote, which displays the approval workflow.

</td></tr><tr><td>

3. Approval chain with approval steps

</td><td>

Grouping of approval steps that are run in sequential order, based on the order specified for the steps in the approval rules. Each step card represents an approval rule and its associated approvers.

</td></tr><tr><td>

4. Approval step card

</td><td>

Card that provides the following information about the approval step and the rules and conditions for that step:-   Approval step state:
-   If the request was previously recalled during the approval process, an Auto-approved flag indicates at least one or more previously completed approvals are automatically reapplied.
-   Depending on the approval step state and the user role, the card displays the More options \(\[Omitted image "icon-three-dots.png"\] Alt text: \) menu for approvers to approve or reject the request in the step.
-   For approval admins that also have the requester role, the More options \(\[Omitted image "icon-three-dots.png"\] Alt text: \) menu provides an **Override** option to bypass the step if it's no longer required. For details, see [Override an approver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/override-approval-step.md).

</td></tr><tr><td>

5. Approval options

</td><td>

Options displayed for certain approval actions, depending on the user role.For example, requesters and approvers have the option to add an ad hoc approver to the approval workflow using the **Add approver** option. For more information, see [Add ad-hoc approvers to an approval request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/add-approver.md).

</td></tr></tbody>
</table>**Parent Topic:**[Using Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-advanced-approval-management.md)

