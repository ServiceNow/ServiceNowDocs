---
title: Notify change request rejection or cancellation reason to Jenkins pipeline
description: Send change request rejection or cancellation reason along with approver name and the change request number to Jenkins pipeline logs.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Notify change request rejection or cancellation reason to Jenkins pipeline

Send change request rejection or cancellation reason along with approver name and the change request number to Jenkins pipeline logs.

## Before you begin

-   Ensure that you have upgraded to ServiceNow DevOps version 1.28 or later.
-   Have an active Jenkins integration.

Role required: sn\_devops.admin

## About this task

You can send change request rejection or cancellation reasons or comments to the Jenkins pipeline logs.

-   Ensure that you enter appropriate reasons or comments when rejecting or canceling a Change Request manually.
-   If you have loaded demo data during upgrade, and are using the DevOps Demo Change Automation flow or a custom flow based on it, a notification with default message values is sent to the Jenkins pipeline logs.

**Note:**

-   The Change request number is also automatically sent to the Jenkins pipeline logs \(for both scripted and freestyle pipelines\) as soon as the change is created.
-   The **Approver name** and time stamp of the cancellation/rejection is also automatically sent to the Jenkins pipeline logs.

## Procedure

1.  To manually reject or cancel change requests, follow these steps:

    1.  Navigate to **DevOps** &gt; **Orchestrate** &gt; **Pipeline Change Requests** &gt; **Change Request record**.

    2.  Open the required Change Request record.

    -   From the context menu, click **Cancel Change**. In the **Cancel Change Request &gt; Reason** field, enter an appropriate reason for cancelling the change, and click **Save**.
    -   In the Approvers related list, provide your inputs in the **Comment** field, right-click the record, and click **Reject**.
    The change request is canceled/rejected and the reason for canceling the change is added to the **Comments** field and sent to the Jenkins pipeline log.

2.  To send custom messages \(from auto-rejected change requests\) to Jenkins, follow these steps:

    1.  Navigate to **Flow Designer** &gt; **DevOps Demo Change Automation flow** &gt; **DevOps Demo Change Policy**.

    2.  Navigate to the **DevOps Auto Reject** decision &gt;**DevOps Apply Change Approval Definition** subflow &gt; **Devops Create Auto Approval Record** action.

    3.  Modify the action's input script for the `approval.comments` attribute value.

    By default, the auto-rejected change requests stores and sends the `approval.comments = 'Auto ' + state + ' via Change Policy';` variables as messages to the Jenkins pipeline as notifications.

3.  In Jenkins, navigate to the pipeline \(that is corresponding to the rejected change request\), and then select **Console Output**.

    The Change Request's rejection or cancellation comments that are stored as part of the step execution reflect in the Jenkins Console Output.


