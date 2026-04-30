---
title: Continual Improvement Management reference
description: Continual Improvement Management reference content including states and field descriptions.
locale: en-US
release: yokohama
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Continual Improvement Management, IT Service Management]
---

# Continual Improvement Management reference

Continual Improvement Management reference content including states and field descriptions.

## Improvement states

The state of an improvement indicates the [progress](../concept/cim-improvement-initiative-mgmt.md) of the improvement in the process.

<table id="table_btf_d1z_ycb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

Improvement request is created either manually, or from within an integrated application by an Improvement Requester.

 Integrated applications include Benchmarks, CMDB, Coaching, Demand, GRC, Major Incident Management, Problem Management, and Survey Management.

 **States** list:

-   Accepted
-   Canceled

 List Controls menu \(![List icon](../image/cim-list-controls.png)\) options on the Improvement Initiative form: Copy Initiative.

</td></tr><tr><td>

Accepted

</td><td>

Improvement request aligns with company strategic objectives and is considered valid by the Improvement Manager.

 **States** list:

-   Assess
-   Canceled

 List Controls menu \(![List icon](../image/cim-list-controls.png)\) options on the Improvement Initiative form: Copy Initiative.

</td></tr><tr><td>

Canceled

</td><td>

Improvement is not accepted \(**Reject** action is selected by the Improvement Manager\), or can be canceled directly in any state.

 **Note:** Any CIM tasks created for the improvement are also canceled.

 List Controls menu \(![List icon](../image/cim-list-controls.png)\) options on the Improvement Initiative form: Copy Initiative.

</td></tr><tr><td>

Assess

</td><td>

All improvement attributes are set by the Improvement Manager, including business process, business service, and success measurement details.

 The improvement is waiting to be assessed by an Approver group member for approval.

 **States** list:

-   Approved

\(only shown for an Approver group member\)

-   Canceled

 List Controls menu \(![List icon](../image/cim-list-controls.png)\) options on the Improvement Initiative form:

-   Copy Initiative
-   Revert to Accepted

</td></tr><tr><td>

Approved

</td><td>

The improvement is assessed and approved by an Approver group member and is ready for implementation.

 The improvement is set to implement by the Improvement Manager.

 **States** list:

-   Implement
-   Canceled
-   Assess \(for reapproval\)

If additional tasks were added, or if the target has changed, the improvement may need to go through approval again.


 List Controls menu \(![List icon](../image/cim-list-controls.png)\) options on the Improvement Initiative form:

-   Copy Initiative
-   Submit for Re-Approval

</td></tr><tr><td>

In Progress

</td><td>

CIM task creation is completed by the Improvement Manager or Improvement Coordinator. CIM tasks are completed by the task owners.

 The Improvement Coordinator determines either that the improvement is complete and sets it to review, or that progress is halted and places it on hold.

 **States** list:

-   Monitor/Review
-   On Hold
-   Assess \(for reapproval\)

If additional tasks were added, or if the target has changed, the improvement may need to go through approval again.


 List Controls menu \(![List icon](../image/cim-list-controls.png)\) options on the Improvement Initiative form:

-   Copy Initiative
-   Submit for Re-Approval

</td></tr><tr><td>

On Hold

</td><td>

Improvement is no longer in progress but may resume at a later date.

 The Improvement Manager determines the outcome of the improvement including whether it should go back to implementation, or be closed or canceled.

 **States** list:

-   Implement
-   Closed
-   Canceled

**Note:** When an improvement is placed on hold, all active CIM tasks \(not closed or canceled\) are also placed on hold, but the state can be changed manually.

When the improvement is taken off hold, all active CIM tasks \(not closed or canceled\) are set to Open state \(unless they were changed manually\).

 List Controls menu \(![List icon](../image/cim-list-controls.png)\) options on the Improvement Initiative form: Copy Initiative.

</td></tr><tr><td>

Monitor/Review

</td><td>

All CIM tasks for the improvement are complete, improvements have been measured, and no further action is required by the task owners.

 The improvement is reviewed for closure by the Improvement Manager.

 **States** list:

-   Implement
-   Closed
-   Assess \(for reapproval\)

If additional tasks were added, or if the target has changed, the improvement may need to go through approval again.


 List Controls menu \(![List icon](../image/cim-list-controls.png)\) options on the Improvement Initiative form: Copy Initiative.

</td></tr><tr><td>

Closed

</td><td>

Improvement is complete and is added to the Closed Improvement Register list.

</td></tr><tr><td>

Delete

</td><td>

Improvement is removed from the Improvement Register list.

 Available in each state but only to the Improvement Manager.

</td></tr></tbody>
</table>## CIM task states

An improvement contains of one or more [CIM tasks](../task/implement-cim-initiative.md) to complete the improvement. A CIM task is assigned to an owner to be responsible for the work specified.

The state of a CIM task indicates the level of progress for the task.

<table id="table_mps_55c_cdb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Pending

</td><td>

State of a CIM task added before the improvement has been approved.

 If a CIM task is added after the improvement is approved, the CIM task is set to Pending state until the improvement is approved again.

 Once approved, the CIM task is set to Open state.

 If rejected, the CIM task remains in the Pending state.

</td></tr><tr><td>

Open

</td><td>

State of a new CIM task for an improvement that has been approved.

</td></tr><tr><td>

Work in Progress

</td><td>

State of a CIM task for which work has begun.

</td></tr><tr><td>

Closed Complete

</td><td>

State of a closed CIM task that has been completed.

</td></tr><tr><td>

Closed Incomplete

</td><td>

State of a closed CIM task that has been closed but not fully completed.

</td></tr><tr><td>

Closed Skipped

</td><td>

State of a closed CIM task for which no work has been done.

</td></tr><tr><td>

On Hold

</td><td>

State of a CIM task for an improvement set to On Hold state.

 The state of a CIM task on hold can be manually changed to Open or Work In Progress states.

**Note:** When an improvement is placed on hold, all active CIM tasks \(not closed or canceled\) are also placed on hold, but the state can be changed manually.

When the improvement is taken off hold, all active CIM tasks \(not closed or canceled\) are set to Open state \(unless they were changed manually\).

</td></tr></tbody>
</table>## CIM approver states

Each improvement needs at least one [approval](https://www.servicenow.com/docs/access?context=r_Approvals&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) to progress to the Implement state. The Approvers related list in the improvement contains a list of user approval records and the state of the approval.

The users in the Approvers related list belong to the **Approver Group** specified on the Improvement Initiative form. Once the improvement has been approved by an Approver Group member, approval from other members is no longer required to progress the improvement. However, other Approver Group members can still set their individual approval state.

To require additional approvers, configure the CIM Approval workflow in [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

## Improvement process flow

![CIM process flow](../image/cim-closed.png "Process flow for Continual Improvement Management")

<table id="table_l1v_mfc_zdb"><thead><tr><th>

Process flow

</th><th>

Role

</th><th>

Description

</th><th>

Next action

</th></tr></thead><tbody><tr><td>

**Create Improvement Initiative**

</td><td>

Improvement Requester

</td><td>

The need is determined for an improvement and an improvement request is created.

</td><td>

Click **Submit.**

 Required: Short Description

</td></tr><tr><td>

New

</td><td>

Improvement Manager

</td><td>

Acceptance is determined by verifying that the improvement objective aligns to a company strategic objective, and an Improvement Coordinator is assigned.

</td><td>

Click **Accept.**

 Required:

-   Improvement Coordinator
-   Strategies

</td></tr><tr><td>

Accepted

</td><td>

Improvement Manager

</td><td>

Other attributes are set and the improvement request is ready to be assessed for approval \(by Approver group members\).

</td><td>

Click **Assess.**

 \(Waiting for approval\)

 Approver group members are notified.

 Required: Approver Group

</td></tr><tr><td>

Assess

</td><td>

CIM approver\(member of the Approver group\)

 [CIM approver states](cim-reference.md)

</td><td>

The improvement attributes are assessed for approval from the Approvers related list.

</td><td>

Click **Approved.**

</td></tr><tr><td>

Approved

</td><td>

Improvement Manager or Improvement Coordinator

</td><td>

Improvement Coordinator and Improvement Manager work together to determine what is needed to ready the improvement for implementation.

</td><td>

Click **Implement**.

 **Actual start date** \(Schedule tab\) is automatically populated.

</td></tr><tr><td>

Implement

</td><td>

Improvement Coordinator

</td><td>

Implementation of the improvement begins with the assigned task owners.Any problem, change, or knowledge submission is shown in the corresponding related list.

</td><td>

Click **Review** if implementation is complete.

 Click **On Hold** if the process has halted.

 Required: On Hold Reason

</td></tr><tr><td>

On Hold

</td><td>

Improvement Manager or Improvement Coordinator

</td><td>

Implementation for the improvement has halted \(**On Hold** state\) but the process flow remains in **Implement**.

</td><td>

Click **Implement** to continue the process.

 Click **Close** if no further work will be done.

</td></tr><tr><td>

Review

</td><td>

Improvement Manager

</td><td>

The improvement attributes are reviewed for completeness and efficacy for closure.

</td><td>

Click **Close**.

 Required: Closure Notes tab

 **Actual end date** is automatically populated.

</td></tr></tbody>
</table>-   **[CIM roles](cim-roles.md)**  
Roles are added with installation of Continual Improvement Management.
-   **[Improvement field descriptions](cim-field-descriptions.md)**  
Improvement Initiative form and related field descriptions.
-   **[Components installed with Continual Improvement Management](cim-components.md)**  
Several types of components are installed with the CIM plugin, including tables, user roles, and scheduled jobs.
-   **[Quick tests for Continual Improvement Management](quick-tests-cim.md)**  
Validate the continued functionality of Continual Improvement Management during application development and after upgrades. Copy and configure these automated tests to identify customizations needing review. All test suites and tests should pass.
-   **[Updates after improvement initiative creation from integrated applications](ui-updates-initiative-from-app.md)**  
UI changes display on the source application record and on the initiative record when you create an improvement initiative from an integrated application.
-   **[Updates after application record creation from improvement initiatives](updates-app-record-from-initiative.md)**  
UI changes display on the source improvement initiative or CIM task record and on the corresponding application records of some applications when you create application records from improvement initiatives or CIM tasks.

**Parent Topic:**[Continual Improvement Management](../concept/cim-landing-page.md)

