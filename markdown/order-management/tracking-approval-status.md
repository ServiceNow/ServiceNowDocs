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

After an approval request is submitted, approval users can view the approval steps in the CSM Configurable Workspace. For example, in a quote approval workflow, requesters, approvers, and users with view access can navigate to the quote. They access the approval workflow interface from the quote Approvals tab.

The approval workflow interface provides an audit trail of approval steps and steps approval chains. Approval cards identify the:

-   Approval rule
-   Assigned approvers
-   Actual approvers for completed steps
-   Approval comments
-   Approval duration timestamp for a step with pending approvals

Approvers use the More options menu in a step card to approve or reject the request.

\[Omitted image "approval-workflow-interface-v2.png"\] Alt text: Approval workflow that shows an approval chain for a quote. The following table describes key elements of the interface.

<table id="table_g4c_qq5_m3c"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Quote state

</td><td>

Quote state:-   Draft: Initial state of the quote. Editable by agent.
-   Requested for review: Quote has been submitted for approval. Not editable by agent unless the quote is recalled by the agent, or the quote has been approved or rejected.
-   Approved: Approvals for the quote are complete.
-   Rejected: Quote rejected by an approver. Editable by agent so that it can be revised and resubmitted for approval.

</td></tr><tr><td>

2. Approvals tab

</td><td>

Related list for the entity, such as a quote, which displays the approval workflow.

</td></tr><tr><td>

3. Approval chain with approval step cards

</td><td>

Grouping of approval steps that are run in sequential order, based on the chain order specified for the steps in the approval rules. Each step card represents an approval rule and its associated approvers. A step card provides the following information:

-   Approval step state
-   Approval duration, which reflects the time elapsed for the active step \(no action taken\):

    -   Number of minutes, for example 43m
    -   Number of hours and minutes, for example 1h 43m
    -   Number of days and hours, for example 2d 4h
    -   Number of weeks days \(over seven days has elapsed\), for example 1w 2 d
If the approval step state is escalated, the approval duration is highlighted and shows the elapsed time for the escalated approval.

-   If the request was previously recalled during the approval process, an Auto-approved flag indicates at least one or more previously completed approvals has been automatically reapplied.
-   For approvers assigned to a step, the card displays the More options \(\[Omitted image "icon-three-dots.png"\] Alt text: \) menu to approve or reject the approval step.
-   For approval admins that also have the requester role, the More options \(\[Omitted image "icon-three-dots.png"\] Alt text: \) menu provides an **Override** option to bypass the step if it's no longer required. For details, see [Override an approver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/override-approval-step.md).

</td></tr><tr><td>

4. Approval options

</td><td>

Options displayed for certain approval actions, depending on the user role.For example, requesters and approvers have the option to add an ad hoc approver to the approval workflow using the **Add approver** option. For more information, see [Add ad-hoc approvers to an approval request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/add-approver.md).

</td></tr></tbody>
</table>**Parent Topic:**[Using Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-advanced-approval-management.md)

