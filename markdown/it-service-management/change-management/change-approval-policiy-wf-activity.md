---
title: Change Approval Policy workflow activity
description: The Change Approval Policy workflow activity controls the approval process for a change request. It creates user and group approvals according to a change approval policy record. A workflow can include multiple activities, each referencing the same or different Change Approval Policies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/change-approval-policiy-wf-activity.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Creating change approval policies, Use, Change Management, IT Service Management]
---

# Change Approval Policy workflow activity

The Change Approval Policy workflow activity controls the approval process for a change request. It creates user and group approvals according to a change approval policy record. A workflow can include multiple activities, each referencing the same or different Change Approval Policies.

Using the current change request and additional inputs defined in the **Policy Input** script field in the activity, you can evaluate the Change Approval Policy record, which applies the approval definitions from matching decisions.

**Note:** This activity is only available when the workflow runs on a table that extends or is the Change Request \[change\_request\] table.

## Results

The activity assigns a result value according to the outcome of the applied policy. The possible result values are:

-   Approved
-   Rejected
-   Canceled
-   Skipped
-   Finished

## Input variables

Input variables determine the initial behavior of the activity.

|Field|Description|
|-----|-----------|
|Approval Policy|Change Approval Policy to apply to the change request.|
|Policy Input|Policy Inputs that are defined on the Change Approval Policy record. Set additional policy inputs here.|
|Finish condition|Determine if the activity should complete while pending approvals remain. Use this condition if the workflow is configured to handle restarting the Change Approval Policy activity. For example, when the change request is put on hold.|

## Condition

The following conditions determine which transition runs after this activity.

<table id="table_zgj_ttw_w4"><thead><tr><th>

Condition

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approved

</td><td>

The change request is approved when it meets the criteria defined by the applied approval definitions.

</td></tr><tr><td>

Rejected

</td><td>

Any rejection from the applied approval definitions results in the Rejected outcome.

</td></tr><tr><td>

Error

</td><td>

The event or condition that generates an error.

</td></tr><tr><td>

Skipped

</td><td>

If this condition is not configured on the activity, then the Approved condition is used. This outcome occurs for the following scenarios:-   No decisions from the Change Approval Policy match
-   No approvals can be generated from matched decisions

</td></tr></tbody>
</table>## States

The workflow engine uses the activity state to perform the next logical action on the activity.

|State|Description|
|-----|-----------|
|Executing|The workflow engine starts the execute function of the activity.|
|Waiting|The workflow engine ignores the activity until a specific event to restart the activity is fired.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

## Example

This example uses the Risk approvals activity in the **Change Request - Normal** workflow. In the workflow, the change approval policy factors in whether the assigned group's manager has already approved the change request.

\[Omitted image "CAPwfexample.png"\] Alt text: Example for Change Approval Policy Risk approvals

You can use this activity to assess the risk of the change request of a normal change policy. When this activity runs, the associated decisions request the required approvals.

\[Omitted image "examplepolicyinput.png"\] Alt text: Example policy input script for risk assessment

Use the **Policy Input** field to set up additional inputs. In the given example, the activity defines the manager\_approved property and performs the query to check if an approved record exists for the approved group's manager.

**Note:** Ensure that the manager\_approved policy input is defined in the Change Approval Policy record.

The **Finish condition** field completes the activity by marking pending approvals as **No Longer Required**. In this workflow example, when the Change Request is put on-hold, the Change Approval Policy activity is completed. The workflow then disregards pending approvals and waits for the Change Request to resume. When the on-hold state is released, the Change Approval Policy activity restarts.

**Parent Topic:**[Creating change approval policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/using-change-approval-policies-cf.md)

