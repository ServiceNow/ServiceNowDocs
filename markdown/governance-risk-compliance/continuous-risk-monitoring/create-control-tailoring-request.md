---
title: Create a control tailoring request
description: Create a control tailoring request to modify baseline controls for an authorization package after the Select step without reverting the package to earlier workflow steps.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Request control tailoring, Implementing controls and assessment objectives in CAM, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Create a control tailoring request

Create a control tailoring request to modify baseline controls for an authorization package after the Select step without reverting the package to earlier workflow steps.

## Before you begin

-   An authorization package in the Implement step or later

Roles required: sn\_irm\_cont\_auth.admin, sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.authorization\_official

## About this task

Control tailoring requests allow you to propose changes to baseline controls without reverting the package to the Select step. You can add new controls, change control applicability \(Applicable to Not Applicable or vice versa\), or modify hybrid and inherited control configurations. All changes require AO approval before taking effect.

When you submit the request, the AO receives an email notification. After approval, the system applies the changes to baseline controls and updates related controls accordingly. Controls not affected by the request remain in their current state.

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace** and then select the **lists icon**.

2.  From the **Authorization packages in the RMF** list, select an authorization package record.

3.  Select the **more action icon** \(**...**\) and then select **Request control tailoring**.

4.  In the **Request control tailoring** pop-up page, enter a brief explanation for the baseline changes you are requesting.

5.  Select **Request** to create a new control tailoring request record.

    CAM creates a new control tailoring request record and opens it.

6.  On the control tailoring request record **Details** tab, review the automatically populated fields.

    |Field|Description|
    |-----|-----------|
    |Number|Auto-generated unique identifier for the request|
    |State|The state of the control tailoring request|
    |Authorization package|The package you selected|
    |Assigned to|The AO or AO Delegate from the authorization package|
    |Step|The current RMF step of the authorization package|
    |Request reason|Explanation for the baseline changes you are requesting|
    |Work notes \(Private\)|Notes for the approver|
    |Additional comments \(Customer visible\)|Additional comments|

7.  Select the **Control Tailoring** tab to specify your baseline modifications.

8.  Review current package configuration in the **Current Records** section.

    The Current Records panel \(left side\) displays existing control allocations:

    -   Baseline Control
    -   Hybrid Control
    -   Inherited Control
    -   Not Applicable Control
    -   Fully Inherited Control
    Use the **Allocation type** drop-down to view controls by allocation type. This section is read-only and serves as reference while making requested changes.

9.  To add baseline controls that do not exist in the authorization package:

    1.  In the **Requested Records** section \(right side\), set the **Allocation type** drop-down to **Baseline Control**.

    2.  Select **Add**.

    3.  In the **Control Objectives** pop-up page, select one or more control objectives to add as baseline controls.

    4.  Select **Add** to add the selection to the requested records.

        The control objectives appear in the **Requested Records** section.

10. To change the allocation of existing controls:

    1.  In the **Current Records** section, use the **Allocation type** drop-down to filter controls by their current allocation type.

    2.  Select one or more controls to modify.

    3.  Select the action that represents the change you want to make:

        -   **Mark as Not Applicable**
        -   **Create Hybrid**
        -   **Inherit from Single Provider**
        -   **Inherit from Multiple Providers**
        -   **Return to Baseline**
    4.  If marking controls as not applicable, enter a justification in the confirmation page and select **Confirm**.

        The system moves the selected controls to the **Requested Records** section with the new allocation type.

11. To remove a requested change before submitting:

    1.  In the **Requested Records** section, select the control to remove.

    2.  Select **Revert**.

        The system removes the change. For newly added controls, Revert deletes the record. For allocation changes, Revert returns the control to its original allocation in Current Records.

12. In the **Requested Changes** tab, review all requested changes.

    The tab displays the requested allocation and previous allocation for each control.

13. Select the **more action icon** \(**...**\) and then select **Reassign** to reassign the request to a different AO within the same authorization package.

    In the **Reassign** pop-up page, select the new approver in the **User** field, enter a reason for the reassignment in the **Reassign reason** field, and then select **Reassign**.

14. To recall the request after submission but before approval:

    1.  Select the **more action icon** \(**...**\) and then select **Recall**.

        The request returns to Draft state, allowing you to make additional modifications.

15. Select **Request for Approval** to submit the request for approval.


## Result

The request state changes to In Review, and the system assigns the request to the AO for approval. The AO receives an email notification. The authorization package displays an indicator showing that baseline changes are under review. You can view the request status in the **My Items** view under the **CAM Workspace task page**, which shows all control tailoring requests you have created.

