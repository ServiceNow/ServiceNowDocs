---
title: Cancel a workflow
description: Canceling a workflow stops the workflow from executing and sets the workflow context State to Canceled. To cancel an executing workflow, you can use the cancelContext\(context\) script. You can define an onCancel script to clean up unresolved workflow activities.To cancel an executing workflow, you can use the cancelContext\(context\) script. This script can be useful in cases where a workflow must be canceled in response to an event or where a user must manually cancel a workflow.Canceling a workflow can leave records or scripts in an unresolved state. For example, canceling a service catalog workflow may leave catalog items in the requesting user's cart. An administrator can specify an On-cancel script that runs when the workflow transitions to the Canceled state. This script can notify users, log information, or resolve the state of any scripts run within a workflow activity. The sys\_id of the workflow context is available in this script using the context\_sys\_id variable.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administering workflow contexts, Workflow administration, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Cancel a workflow

Canceling a workflow stops the workflow from executing and sets the workflow context **State** to **Canceled**. To cancel an executing workflow, you can use the cancelContext\(context\) script. You can define an onCancel script to clean up unresolved workflow activities.

## Before you begin

Role required: admin or workflow\_admin

## About this task

Canceling a workflow attempts to stop the workflow gracefully by injecting a cancel command into the workflow engine.

## Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Active Contexts**.

2.  Select a workflow context record.

3.  Configure form layout to add **On-cancel script** field to form.

    For detailed information about configuring form layout, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

4.  Select the **Cancel** related link.

    A confirmation appears.

    ![Cancel Confirmation](../image/CancelConfirmation.png)

5.  Click **OK**.

    The workflow engine attempts to cancel the workflow gracefully.

    ![Wait for Cancel](../image/WaitForCancel.png)

    If the workflow does not respond to the cancel command, the Force Cancel option appears.

    ![Force Cancel](../image/ForceCancel.png)

6.  Click **Force cancel** to interrupt the thread the workflow is actively executing or click **Continue waiting** to continue waiting for the workflow to cancel gracefully.

    **Warning:** Whenever possible, allow a workflow to cancel gracefully. Forcing a workflow to cancel can leave related workflows and scripts in an unresolved state. You can use an on-cancel script to clean up unresolved artifacts from a cancelled workflow.


**Parent Topic:**[Administering workflow contexts](../reference/r_AdministeringWorkflowContexts.md)

## Cancel a workflow with the cancelContext\(context\) script

To cancel an executing workflow, you can use the cancelContext\(context\) script. This script can be useful in cases where a workflow must be canceled in response to an event or where a user must manually cancel a workflow.

### Before you begin

Role required: admin

### About this task

For more information, see the [Workflow - cancelContext\(GlideRecord context\)](https://www.servicenow.com/docs/access?context=c_Workflow_api&version=australia&pubname=australia-api-reference&section=r_WF-cancelContext_GR&ft:locale=en-US).

## Define an on-cancel script

Canceling a workflow can leave records or scripts in an unresolved state. For example, canceling a service catalog workflow may leave catalog items in the requesting user's cart. An administrator can specify an On-cancel script that runs when the workflow transitions to the Canceled state. This script can notify users, log information, or resolve the state of any scripts run within a workflow activity. The sys\_id of the workflow context is available in this script using the context\_sys\_id variable.

### About this task

On-cancel scripts run asynchronously from the global scope. Your instance workload determines when the system schedules and runs the on-cancel script.

**Important:** Since the system runs on-cancel scripts from the global scope, they cannot call or run scoped script includes.

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Versions**.

2.  Select a workflow version that you have checked out.

    Workflow versions that are not checked out are not editable.

3.  Edit the **On-cancel script** field.

    You may need to configure the form to add this field.

4.  Click **Update**.


### Example

This example script adds a comment to a Requested Item \[sc\_req\_item\] record indicating the workflow for that request has been canceled.

```
var grContext = new GlideRecord("wf_context"); 
grContext.get(context_sys_id); 
var grReq = new GlideRecord("sc_req_item");
 
// The current record may not exist, make sure it exists before modifying it.
if (grReq.get(grContext.id)) {
    grReq.comments = "The workflow processing this item was Canceled. Contact your system administrator for further information.";
    grReq.update();
}
```

