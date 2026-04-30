---
title: Ask for Approval step
description: Request approval for a record with an approval field. You can configure a rule set for an approval, rejection, or cancellation. If a due date is added to an approval, the approval is automatically approved, rejected, or canceled if the approvers have not responded by the designated time.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-02-28"
reading_time_minutes: 4
breadcrumb: [Workflow Studio steps, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Ask for Approval step

Request approval for a record with an approval field. You can configure a rule set for an approval, rejection, or cancellation. If a due date is added to an approval, the approval is automatically approved, rejected, or canceled if the approvers have not responded by the designated time.

[Classic approvals](../../service-administration/reference/r_Approvals.md) is a platform feature that enables users or groups to approve or reject a task.

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Record**

    Data type: **Record**

    Reference to the record to approve. If the record contains an approval field, Workflow Studio automatically sets the Approval Field input.

-   **Table**

    Data type: **Table Name**

    Table name of the record associated with the approval request. The table that you select must support approvals by having an approval state field. For example, the Task table and its extensions contain approval fields.

-   **Approval Reason**

    Data type: **String**

    Text string containing a justification for the approval. You can use this field for auditing and regulation compliance. This information is stored in the Approval \[sysapproval\_approver\] table. For example, you can list why a specific approval request is needed from an individual or a group.

-   **Approval Field**

    Data type: **Field Name**

    Field containing the results of approval requests.

-   **Journal Field**

    Data type: **Field Name**

    Field to store history and comments associated with the approval request.

-   **Rules**

    Data type: **Approval Rules**

    Approval and rejection rules to determine which users can approve or reject requests, and what happens after approval or rejection.

    Approval or rejection rules include:

    -   Anyone approves
    -   All users approve
    -   All responded and anyone approves
    -   % of users approve
    -   \# of users approve
    In the field beside the approval rule, add the desired approvers. To add approvers:

    -   Select individual users or groups.
    -   Drag or select a field from a record.
    -   Select Manual approvers ![Manual approvers icon](../images/manual-users-icon.png) to allow a manual approver to process an approval or rejection. A manual approver is a user manually added to the Approvers related list who can then approve the request. For example, you can manually add a subject matter expert to a task to approve the request. To learn more about adding manual approvers, see [Generate approvals using the approvers related list](../../service-administration/concept/c_GenApprovalsUsingApprsRelList.md).
    **Note:** By default, Ask for Approval generates approval records for inactive users and groups. This behavior allows a flow or action to continue working even when a specific user or group is later made inactive. If you want to change the behavior of generating approvals for inactive entities, set the com.glide.hub.flow.approval.allow\_inactive\_entity system property. See [Workflow Studio flow system properties](flow-designer-system-properties.md).

    Define rejection rules by adding another OR rule set. When defining approvals, include rejection rules that run when there are no matching approvals. Such rejection rules prevent the flow from remaining in a waiting state. For example, if an approval can be approved by anyone, create a time-based rejection rule in case no one approves it.

    **Note:** If you set an approval rule with no rejection rule \(or vice versa\) and the expected approval state is not met, the runtime value will be **canceled**.

    For information about how to use inline script to specify approval rules, see the [Scripted Approvals in Flow Designer with Flow Variables](https://www.servicenow.com/community/now-platform-blog/scripted-approvals-in-flow-designer-with-flow-variables/ba-p/2284506) blog post on the ServiceNow Community.

-   **Due Date**

    Data type: **Schedule Date/Time**

    Due date for an approval state to prevent the flow from endlessly waiting for approval.


## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


## Output

These outputs appear in the Data panel. You can use them as inputs elsewhere in your action.

-   **Approval State**

    Data type: **Choice**

    Completion state of the approval request. The flow execution details page displays one of these values.

    -   Not Yet Requested \[not requested\]
    -   Requested \[requested\]
    -   Approved \[approved\]
    -   Rejected \[rejected\]
    -   Cancelled \[cancelled\]
    -   No Longer Required \[not\_required\]
    -   Skipped \[skipped\]

## Example

![Example Ask for Approval step in an action.](../images/ask-for-approval-example.png)

**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

