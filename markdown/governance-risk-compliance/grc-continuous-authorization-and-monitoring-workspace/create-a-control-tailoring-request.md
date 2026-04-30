---
title: Create a control tailoring request
description: Create a control tailoring request to modify baseline controls for an authorization package after the Select step without reverting the package or disrupting ongoing assessments.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-01-26"
reading_time_minutes: 3
breadcrumb: [Request control trailoring, View package details in CAM Workspace, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Create a control tailoring request

Create a control tailoring request to modify baseline controls for an authorization package after the Select step without reverting the package or disrupting ongoing assessments.

## Before you begin

Ensure you have the following:

-   An authorization package in the Categorize step or later
-   Authorizing Official \(AO\) or AO Delegate configured for the package

Role required: sn\_grc\_cam.manager or sn\_grc\_cam.admin

## About this task

Control tailoring requests allow you to propose changes to baseline controls without reverting the package to the Select step. You can add new controls, change control applicability \(Applicable to Not Applicable or vice versa\), or modify hybrid and inherited control configurations. All changes require AO approval before taking effect.

When you submit the request, the system generates an approval task for the AO. After approval, an item generation job applies the changes to baseline controls and updates related controls accordingly. Controls not affected by the request remain in their current state.

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace** and then select the lists icon \(![Lists icon.](../../grc-workspace-vrm/image/ws-list-icon.png)\).

2.  From the Authorization packages in the RMF list, select an authorization package record.

3.  Select more action icon and then select **Request control tailoring**.

4.  In the **Request control tailoring** pop-up page, enter a brief explanation for the baseline changes you are requesting.

5.  Select **Request** to a new control tailoring request record.

    CAM creates a new control tailoring request record and opens it.

6.  On the control tailor request record **Details** tab, review the automatically populated fields.

    |Field|Description|
    |-----|-----------|
    |Number|Auto-generated unique identifier for the request|
    |State|The state of the control tailor request|
    |Authorization package|The package you selected|
    |Assigned to|The AO or AO Delegate from the authorization package|
    |Step|The current NIST Risk Management Framework step of the authorization package|
    |Request reason|Explanation for the baseline changes you are requesting|
    |Work notes \(Private\)|Notes for the approves|
    |Additional comments \(Customer visible\)|Additional comments|

7.  Select the **Control Tailoring** tab to specify your baseline modifications.

8.  To add baseline controls that do not exist in the authorization package:

    1.  In the **Requested Records** section, set the **Allocation type** drop-down to **Baseline Control**.

    2.  Select **Add**.

    3.  In the **Control Objectives** pop-up page select one or more control objective to set as baseline control.

    4.  Select **Add** to add the selection to the requested record.

        The control objectives appear in the **Requested Records** section.

9.  To change the allocation of existing controls:

    1.  In the **Current Records** section, set the **Allocation type** drop-down for which you want to request the changes.

        -   **Baseline Control**
        -   **Hybrid Control**
        -   **Inherited Control**
        -   **Not Applicable Control**
        -   **Fully Inherited Control**
    2.  Select one or more baseline controls, to mark a baseline control as not applicable.

    3.  Select **Mark as Not applicable** to change selected controls to not applicable.

    4.  In the **Mark as Not Applicable** confirmation page, enter a justification and select **Confirm**.

        The system moves the selected controls to the **Requested Records** section in the **Not Applicable Control** allocation type.

10. In the **Requested Changes** tab, review the requested changes.

    The tab displays the requested allocation and previous allocation for each control.

11. Select the more action icon and then select **Reassign** to reassign the request to a different AO or AO Delegate within the same authorization package.

    In the **Re-assign** pop-up page select the new approver in the **User** field, reason for the new approver in the **Reassign reason** field, and the select **Reassign**.

12. Select **Request for Approval** to submit the request for approval.


## Result

The request state changes to In Review, and the system assigns the request to the AO or AO Delegate for approval. The control tailoring request appears in the Pending state. The authorization package displays an indicator showing that baseline changes are under review. You can view the request status in the My Items view under the CAM Workspace task page, which shows all control tailoring requests you have created.

**Parent Topic:**[Request control trailoring](../concept/request-control-trailoring.md)

