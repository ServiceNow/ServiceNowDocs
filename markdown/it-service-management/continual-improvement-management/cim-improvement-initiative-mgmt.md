---
title: Managing improvements
description: Continual Improvement Management \(CIM\) provides a structured process for requesting, approving, implementing, and tracking improvements aligned with company strategic objectives.
locale: en-US
release: australia
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Continual Improvement Management, IT Service Management]
---

# Managing improvements

Continual Improvement Management \(CIM\) provides a structured process for requesting, approving, implementing, and tracking improvements aligned with company strategic objectives.

After an improvement is requested, the Improvement Manager reviews it, assigns an Improvement Coordinator, and monitors progress of all improvements. The Improvement Manager oversees, identifies, drives, and monitors the progress of all improvements.

The Improvement Coordinator manages assigned improvements and works with the Improvement Manager and CIM task owners to implement and track task completion.

**Note:** Although both roles can cancel an improvement, only the Improvement Manager can delete an improvement, which removes it from the Improvement Register list.

## CIM Process flow

1.  New: The process flow starts with a new improvement request. A user with the Improvement Requester role submits a new improvement request after identifying a need for improvement in the environment.
2.  Accepted: The Improvement Manager verifies that the new improvement request aligns with at least one company strategic objective and assigns an Improvement Coordinator before accepting the improvement as valid. The assigned Improvement Coordinator is notified that the improvement request has been accepted.

    Companies typically have more than one Improvement Coordinator since that role implements and tracks the progress of assigned improvement initiatives at the task level. There can be many tasks per improvement.

3.  Assess: After acceptance, the Improvement Manager sets the remaining attributes on the Improvement Initiative form, and progresses it to be assessed for approval \(by Approver group members\).
4.  Approved: During assessment, users in the approver group \(shown in the Approvers related list\) are notified of the approval request. One or all of the approver group members evaluate the improvement attributes and either approve or reject the improvement.
5.  In Progress: After approval, the Improvement Coordinator and Improvement Manager work together \(in regular implementation meetings, for example\) to determine what work is needed to ready the improvement for implementation.

    During implementation, the Improvement Coordinator creates and assigns phases and can create tasks directly from an initiative or from a phase to complete the improvement. The Improvement Coordinator works with the task owners \(in regular task status meetings, for example\) to track the progress of task completion. Records for other supported applications can also be created from within the improvement initiative or CIM task, if needed, and are typically shown in a related list in the improvement initiative or CIM task.

    If implementation for the improvement has been halted, the Improvement Manager or Improvement Coordinator can place the improvement **on hold**. All CIM tasks that are not closed or canceled are also placed on hold. You can cancel a CIM initiative at any stage when the initiative is in progress. When you cancel an initiative, the initiative as well as the tasks associated with the initiative move to **Closed Incomplete**.

6.  Review: The Improvement Coordinator places the improvement under **review** when all CIM tasks in all CIM phases are verified 100% complete.
7.  Closed: The Improvement Manager reviews the improvement completeness and sets the improvement to closed.

## CIM task progress rollup calculation

You can create a task directly from an initiative or from a phase. When a task is moved to the Closed Complete state, the progress of the CIM initiative is calculated based on the percentage of all tasks that are in Closed Complete state for that initiative. The duration of the task which is based on the planned end date is also taken into consideration when the progress of the CIM initiative is calculated. The longer the duration, the slower the progress. As you add new tasks to a phase or associate it directly with the CIM initiative, the percentage completion for the CIM initiative is updated accordingly.

The following table shows an example of how the CIM task progress rollup is calculated.

<table id="table_odn_nl4_pnb"><thead><tr><th>

Parent Record

</th><th>

Task

</th><th>

Task duration

</th><th>

State

</th><th>

Contribution to initiative progress \(%\)

</th></tr></thead><tbody><tr><td>

CIM Phase 1

</td><td>

Task 1

</td><td>

2 days

</td><td>

Closed Complete

</td><td>

20%

</td></tr><tr><td>

CIM Phase 1

</td><td>

Task 2

</td><td>

3 days

</td><td>

Closed Complete

</td><td>

30%

</td></tr><tr><td>

CIM Initiative

</td><td>

Task 3

</td><td>

2 days

</td><td>

Any state other than Closed Complete

</td><td>

50%**Note:** This task is directly associated with the CIM initiative.

</td></tr></tbody>
</table>## Alignment with company strategic objectives

You can verify alignment with company goals by setting the **Strategies** field on the Improvement Initiative form to one or more company [enterprise strategies](https://www.servicenow.com/docs/access?context=overview-business-planning&version=australia&pubname=australia-it-business-management&ft:locale=en-US) from the Strategic Objectives lookup list so they are linked.

**Note:** Only the Improvement Manager can create a strategy.

Coordinating improvements with enterprise strategies of the company helps you verify that the improvement contributes to the overall goals of the company.

Access enterprise strategies by navigating to **Continual Improvement** &gt; **Enterprise Strategies** \(or **Organization** &gt; **Enterprise Strategy**\).

## Improvement Register

View, prioritize, and track improvements, related tasks, and phases from one Improvement Register list that includes all open and closed improvements.

You can access the Improvement Register by navigating to **All** &gt; **Continual Improvement** &gt; **Workbench** and selecting **View Standard List**.![Improvement register](../image/cim-register.png)

## Embedded Performance Analytics scorecard

Use the [Analytics Hub](https://www.servicenow.com/docs/access?context=c_UsePerformanceAnalyticsScorecards&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) embedded in the Improvement Initiative form for continuous KPI monitoring and to track the progress of the KPI improvement during the lifecycle of the improvement. The KPI scorecard is useful so you can monitor the incremental benefits of the KPI or adjust CIM tasks and assignments to meet your improvement goal, if needed. Toggling **Show Records** displays the list of records that contribute to the KPI values shown on the scorecard. ![CIM scorecard](../image/cim-scorecard.png)

Scorecards are also shown for any KPIs listed in Impacted KPIs related list on the Improvement Initiative form.

-   **[Accept an improvement](../task/accept-assign-cim-request.md)**  
Accept and assign a new improvement request so it can be assessed for approval. You can reject the improvement request if it does not align with company strategic objectives.
-   **[Prepare an improvement](../task/implement-cim-initiative.md)**  
Create CIM phases and tasks to implement an approved improvement. The Improvement Coordinator works with the Improvement Manager to plan implementation and track progress.
-   **[Assess an improvement for approval](../task/assess-cim-initiative.md)**  
Once accepted and set to assess, Approver group members evaluate the improvement for approval before implementation can begin.
-   **[Review and close an improvement](../task/review-close-cim-initiative.md)**  
Once all tasks in each phase of the improvement have been completed, the Improvement Coordinator sets the improvement to review for the Improvement Manager to close.

**Parent Topic:**[Continual Improvement Management](cim-landing-page.md)

**Related topics**  


[Continual Improvement Management reference](../reference/cim-reference.md)

[Improvement field descriptions](../reference/cim-field-descriptions.md)

