---
title: Add an activity to a catalog workflow
description: You can add activities to a workflow to perform tasks such as running a script, sending notifications, or requesting approvals. Activities can succeed or fail, which can result in actions performed by other activities.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service catalog workflows, Service Catalog request fulfillment, Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add an activity to a catalog workflow

You can add activities to a workflow to perform tasks such as running a script, sending notifications, or requesting approvals. Activities can succeed or fail, which can result in actions performed by other activities.

## Before you begin

Role required: workflow\_creator, workflow\_admin, or admin

## About this task

After creating the workflow to add a laptop fulfillment process, add the activities.

## Procedure

1.  Complete the following steps to add an activity that requests manager approval.

    1.  In the **Core** pane, expand **Approvals** and drag the activity **Approval - User** onto the arrow between **Begin** and **End**.

        This activity generates an approval from the manager of the person requesting the laptop.

    2.  Complete the form with the following information.

        -   **Name**: `Manager Approval`
        -   **Stage**: **Waiting for Approval**
        -   **User**: Click the lock icon in the Approvers section, and then click the select fields icon. Expand **Requested** &gt; **Requested For**, and then select **Manager**.
    3.  Click **Submit**.

2.  Complete the following steps to add an action for when the approver rejects the request.

    1.  Expand **Utilities** in the **Core** pane and drag the activity **Set Values** to the space below the approval.

    2.  Complete the form with the following information.

        -   **Name**: `Rejected`
        -   **Stage**: **Completed**
        -   **Values** condition builder: **\[Approval\] \[Rejected\]**
    3.  Click **Submit**.

    4.  Drag from the yellow box beside **Rejected** on the **Approval - User** activity to the new **Set Values** activity.

    5.  Drag again from the yellow box beside **Always** on the **Set Values** activity to **End**.

        This activity marks the request as rejected if the manager rejects the request and then ends the workflow

3.  Complete the following steps to add an action for when the approver approves the request.

    1.  Drag the activity **Set Values** onto the arrow between **Approval - User** and **End**.

    2.  Complete the form with the following information.

        -   **Name**: `Approved`
        -   **Stage**: **Fulfillment**
        -   **Values** condition builder: **\[Approval\] \[Approved\]**
        This activity marks the request as approved once a manager approves it.

    3.  Click **Submit**.

4.  Expand **Tasks** and drag the activity **Create Task** onto the arrow between **Approval - User** and **End**, add the following information, and click **Submit**.

    -   **Name**: `Laptop Procurement`
    -   **Stage**: **Fulfillment**
    -   **Task Type**: **Catalog Task \[sc\_task\]**
    -   **Priority**: **3 - Moderate**
    -   **Fulfillment group**: **Procurement**
    -   **Short description**: `Procure a Laptop`
    This task tells Procurement to procure a laptop for the user.

5.  Expand **Notifcations** and drag the activity **Notification** onto the arrow between **Laptop Procurement** and **End**, add the following information, and click **Submit**.

    -   **Name**: `Procurement`
    -   **Stage**: **Fulfillment**
    -   **To**: Click the lock icon in the Addressee\(s\) section, and then click the select fields icon. Expand **Requested** and select **Requested For**.
    -   **Subject**: `Your laptop has been procured.`
    This activity marks the request as approved if a manager approves it.

6.  Drag the activity **Create Task** onto the arrow between **Procurement** and **End**, and then fill in the form.

<table id="choicetable_yn3_s25_dq"><tbody><tr><td id="d284988e469">

**Name**

</td><td>

Set Up Laptop

</td></tr><tr><td id="d284988e478">

**Stage**

</td><td>

Fulfillment

</td></tr><tr><td id="d284988e487">

**Task Type**

</td><td>

Catalog Task

</td></tr><tr><td id="d284988e496">

**Priority**

</td><td>

3 - Moderate

</td></tr><tr><td id="d284988e505">

**Fulfillment Group**

</td><td>

Hardware

</td></tr><tr><td id="d284988e515">

**Short Description**

</td><td>

Set up laptop.

</td></tr></tbody>
</table>    This task tells Hardware to configure the laptop and prepare it for use.

7.  Drag the activity **Create Task** onto the arrow between **Set Up Laptop** and **End**, add the following information, and click **Submit**.

    -   **Name**: `Pickup Laptop`
    -   **Stage**: **Delivery**
    -   **Task Type**: **Catalog Task \[sc\_task\]**
    -   **Priority**: **3 - Moderate**
    -   **Assigned to**: Leave the field blank, as the script in the **Advanced** field assigns this task to the requester.
    -   **Short description**: `Pick up laptop.`
    -   **Advanced**: Select the check box and set the **Advanced Script** value to: `task.assigned_to=current.requested_for;`
    This task informs the requester to come pick up the laptop.

8.  Drag the activity **Log Message** onto the arrow between **Pick Up Laptop** and **End**, add the following information, and click **Submit**.

    -   **Name**: `Delivered`
    -   **Stage**: **Completed**
    -   **Message**: `The laptop delivery workflow is complete.`
    Leaves a message in the log to record the successful completion of the workflow.


**Parent Topic:**[Service catalog workflows](../concept/c_ServiceCatalogWorkflowDefinition.md)

