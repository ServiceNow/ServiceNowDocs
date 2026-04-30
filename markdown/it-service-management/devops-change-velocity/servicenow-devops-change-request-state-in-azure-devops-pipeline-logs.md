---
title: ServiceNow DevOps change request state in Azure DevOps pipeline logs
description: View the change request state and the corresponding policy conditions in the Azure DevOps pipeline console logs whenever the state of a change request is updated.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# ServiceNow DevOps change request state in Azure DevOps pipeline logs

View the change request state and the corresponding policy conditions in the Azure DevOps pipeline console logs whenever the state of a change request is updated.

You can navigate to the console logs in your Azure DevOps pipeline to view the state of a change request when a change request is created or when the state of the change request is updated. The policy conditions associated with the change request state will also be evaluated and displayed in the logs. For example, if the DevOps Change Request Advanced Automation Policy is activated, the policy conditions will be evaluated and the corresponding decision made \(auto-approve/auto-reject/manual-approval\) will be displayed in the logs.

The following change request details are displayed:

-   number
-   details
-   status
-   sys\_id
-   type
-   risk
-   priority
-   changeState
-   plannedStartDate
-   plannedEndDate
-   changeRequestURL

![Change state in Azure DevOps pipeline console logs.](../image/ado-change-state-policy-conditions.png)

**Note:** **changeState** is the state of the change request, and **status** is the status of the step execution.

The logs for policy conditions will be displayed for the base system change flows as follows:

-   DevOps Model Change Policy: Only logs will be displayed on change creation and when the change state is updated.
-   DevOps Change Request Minimal Automation Policy: Logs along with change decision and policy conditions corresponding to the change decision will be displayed.
-   DevOps Change Request Advanced Automation Policy: Logs along with change decision and policy conditions corresponding to the change decision will be displayed.

The change policy input and decision conditions are stored in the Decisions \[sys\_decision\_question\] table. Logs will be displayed if the following fields and operators are used as input for policy conditions:

-   **Fields**
    -   code\_coverage
    -   commits\_without\_work\_item
    -   integration\_tests\_failed
    -   load\_tests\_failed
    -   regression\_tests\_failed
    -   num\_of\_outages\_in\_last\_7\_days
    -   num\_of\_current\_outages
    -   num\_of\_open\_incidents
    -   total\_num\_of\_commits
    -   tests\_passing\_percent
    -   risk
    -   code\_security
    -   commits
-   **Operators**
    -   &lt;=
    -   &gt;=
    -   !=
    -   =
    -   &lt;
    -   &gt;
    -   ISNOTEMPTY
    -   ISEMPTY
    -   BETWEEN
    -   ANYTHING
    -   NSAMEAS
    -   SAMEAS
    -   GT\_FIELD
    -   LT\_FIELD

**Note:** If any field is modified in a change policy other than the base system fields, then those fields must be manually added to the flow for policy conditions to be evaluated.

If a change request does not get created due to any issue, then the reason for the failure and the state is also logged in the console.

![Change failure reason in ADO pipeline console logs.](../image/ado-change-state-failed.png)

**Note:** For Azure DevOps, if change receipt is enabled, the very first log may not be displayed onto the console. That is, when the change is created and is in the New state.

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](azure-devops-integration-dev-ops.md)

