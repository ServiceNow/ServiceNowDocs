---
title: ServiceNow DevOps change request state in Jenkins pipeline logs
description: You can use the Jenkins Snippet Generator utility to configure how and when the change state and the corresponding policy conditions must be displayed in the Jenkins pipeline job logs. This enables developers to view the status of the change in the console logs of the pipeline itself.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# ServiceNow DevOps change request state in Jenkins pipeline logs

You can use the Jenkins Snippet Generator utility to configure how and when the change state and the corresponding policy conditions must be displayed in the Jenkins pipeline job logs. This enables developers to view the status of the change in the console logs of the pipeline itself.

To generate a step snippet, navigate to the Pipeline Syntax from a configured pipeline, select the **SnDevOpsChange** step from the **Sample Step** list, and update the values for the change state variables in the step. Select the **ignore error** option to prevent job failure if there is an error. Select **Generate Pipeline Script** to create a snippet. You can copy and paste the snippet into the pipeline to start receiving the change state notifications. Update the following variables in the **SnDevOpsChange** step to receive change state notifications:

-   **Polling Interval**: Specifies the frequency \(in seconds\) at which Jenkins polls ServiceNow for the change status and updates the console logs with the status. The change status is updated in the console logs only when the **Change state transitions**, **Assignment Group updates**, **Approval updates**, **Planned Start/End date**, or **Change Details** \(if any\) fields are updated.

    **Note:** If no value is entered in the field, polling interval check won’t be run to update the change status in the console logs.

-   **Change Creation Timeout**: Specifies the change creation timeout value in seconds. On timeout, Jenkins checks the change creation status in ServiceNow. If the change did not get created, the pipeline is resumed or aborted based on the **Abort on change creation failure** flag. By default, the pipeline is aborted when timeout is specified and the **Abort on change creation failure** flag is selected.

    **Note:** If no value is entered in the field, change creation timeout check won’t be run to update the pipeline.

-   **Abort on change creation failure**: Abort or resume the pipeline if change is not created till the change creation timeout.
    -   Selected: Abort
    -   Cleared: Resume
-   **Change Step Timeout**: Specifies the change step timeout value in seconds. On timeout, Jenkins checks the change step status in ServiceNow. If the change step is still in progress, the pipeline is resumed or aborted based on the **Abort on change step timeout** flag. By default, the pipeline aborted when timeout is specified, and the **Abort on change step timeout** flag is selected.

    **Note:** If no value is entered in the field, change step timeout check won’t be run to update the pipeline.

-   **Abort on change step timeout**: Abort or resume the pipeline if the change step is still in progress on change step timeout.
    -   Selected: Abort
    -   Cleared: Resume

You can navigate to the console logs in your pipeline to view the state of a change request when a change request is created or when the state of the change request is updated. The policy conditions associated with the change request state will also be evaluated and displayed in the logs. For example, if the DevOps Change Request Advanced Automation policy is activated, the policy conditions will be evaluated and the corresponding decision made \(auto-approve/auto-reject/manual-approval\) will be displayed in the logs.

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

![Change state logs in Jenkins pipeline console](../image/jenkins-change-state.png)

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

**Parent Topic:**[Jenkins integration with DevOps Change Velocity](jenkins-integration-dev-ops.md)

