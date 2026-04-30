---
title: Managing improvements
description: After an improvement is requested, the Improvement Manager reviews it, assigns an Improvement Coordinator, and monitors progress of all improvements to ensure value and success. The Improvement Coordinator works with the Improvement Manager to implement the improvement.
locale: en-US
release: yokohama
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Continual Improvement Management, IT Service Management]
---

# Managing improvements

After an improvement is requested, the Improvement Manager reviews it, assigns an Improvement Coordinator, and monitors progress of all improvements to ensure value and success. The Improvement Coordinator works with the Improvement Manager to implement the improvement.

The Improvement Manager oversees, identifies, drives, and monitors the progress of all improvements.

The Improvement Coordinator manages the improvements to which they have been assigned by the Improvement Manager, and works with the CIM task owners to track task completion.

**Note:** Although both roles can cancel an improvement, only the Improvement Manager can delete an improvement, which removes it from the Improvement Register list.

## Process flow

![CIM process flow](../image/cim-closed.png "Continual Improvement Management Process Flow")

1.  The process flow starts with a **new** improvement request. A need for improvement is identified in the environment and a new improvement request is submitted by a user with the Improvement Requester role.
2.  The Improvement Manager then verifies that the new improvement request aligns with at least one company strategic objective, and assigns an Improvement Coordinator before accepting the improvement as valid. The assigned Improvement Coordinator is notified that the improvement request has been **accepted**.

    There is typically more than one Improvement Coordinator in a company since that role is responsible for implementing and tracking the progress of assigned improvement initiatives at the task level, and there can be many tasks per improvement.

3.  Once accepted, the Improvement Manager sets the remaining attributes on the Improvement Initiative form, and progresses it to be **assessed** for approval \(by Approver group members\).
4.  During assessment, users in the approver group \(shown in the Approvers related list\) are notified of the approval request. One or all of the approver group members evaluate the improvement attributes and either **approve** or reject the improvement.
5.  Once approved, the Improvement Coordinator and Improvement Manager work together \(in regular implementation meetings, for example\) to determine what work is needed to ready the improvement for **implementation**.

    During implementation, the Improvement Coordinator creates and assigns phases and can create tasks directly from an initiative or from a phase to complete the improvement. The Improvement Coordinator works with the task owners \(in regular task status meetings, for example\) to track the progress of task completion. Records for other supported applications can also be created from within the improvement initiative or CIM task, if needed, and are typically shown in a related list in the improvement initiative or CIM task.

    If, for some reason, implementation for the improvement has been halted, the Improvement Manager or Improvement Coordinator can place the improvement **on hold**. All CIM tasks that are not closed or canceled are also placed on hold. You can cancel a CIM initiative at any stage when the initiative is in progress. When you cancel an initiative, the initiative as well as the tasks associated with the initiative move to **Closed Incomplete**.

6.  The Improvement Coordinator places the improvement under **review** when all CIM tasks in all CIM phases are verified 100% complete. The Improvement Manager reviews the improvement completeness and sets the improvement to **closed**.

## CIM task progress rollup calculation

You can create a task directly from an initiative or from a phase. When a task is moved to the Closed Complete state, the progress of the CIM initiative is calculated based on the percentage of all tasks that are in Closed Complete state for that initiative. The duration of the task which is based on the planned end date is also taken into consideration when the progress of the CIM initiative is calculated. The longer the duration, the slower the progress. As you add new tasks to a phase or associate it directly with the CIM initiative, the percentage completion for the CIM initiative is updated accordingly.

The table below shows an example of how the CIM task progress rollup is calculated.

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

You can ensure alignment with company goals by setting the **Strategies** field on the Improvement Initiative form to one or more company [enterprise strategies](https://www.servicenow.com/docs/access?context=overview-business-planning&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) from the Strategic Objectives lookup list so they are linked.

**Note:** Only the Improvement Manager can create a strategy.

Coordinating improvements with enterprise strategies of the company ensures the improvement contributes to the overall goals of the company.

Access enterprise strategies by navigating to **Continual Improvement** &gt; **Enterprise Strategies** \(or **Organization** &gt; **Enterprise Strategy**\).

## Improvement Register list

View, prioritize, and track improvements, related tasks, and phases from one Improvement Register list that includes all open and closed improvements in one list.

![Improvement register](../image/cim-register.png "Improvement Register")

## Embedded Performance Analytics scorecard

Use the [Analytics Hub](https://www.servicenow.com/docs/access?context=c_UsePerformanceAnalyticsScorecards&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) embedded in the Improvement Initiative form for continuous KPI monitoring, and to track the progress of the KPI improvement during the lifecycle of the improvement. The KPI scorecard is useful so you can monitor the incremental benefits of the KPI, or adjust CIM tasks and assignments to meet your improvement goal, if needed.

![CIM scorecard](../image/cim-scorecard.png "Embedded KPI scorecard")

The improvement icon \(![Improvement icon](../image/cim-improvement-icon.png)\) indicates the start and end dates that are tracked on the KPI scorecard chart.

Scorecards are also shown for any KPIs listed in Impacted KPIs related list on the Improvement Initiative form.

-   **[Accept an improvement](../task/accept-assign-cim-request.md)**  
Accept and assign a new improvement request so it can be assessed for approval. You can reject the improvement request if it does not align with company strategic objectives.
-   **[Prepare an improvement](../task/implement-cim-initiative.md)**  
Once the improvement is approved, you can create CIM phases, tasks, and identify impacted KPIs. The Improvement Coordinator for the improvement works with the Improvement Manager to plan implementation.
-   **[Assess an improvement for approval](../task/assess-cim-initiative.md)**  
Once accepted and set to assess, Approver group members evaluate the improvement for approval before implementation can begin.
-   **[Review and close an improvement](../task/review-close-cim-initiative.md)**  
Once all tasks in each phase of the improvement have been completed, the Improvement Coordinator sets the improvement to review for the Improvement Manager to close.

**Parent Topic:**[Continual Improvement Management](cim-landing-page.md)

**Related topics**  


[Continual Improvement Management reference](../reference/cim-reference.md)

[Improvement field descriptions](../reference/cim-field-descriptions.md)

