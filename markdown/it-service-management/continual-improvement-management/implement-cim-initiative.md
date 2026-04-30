---
title: Prepare an improvement
description: Once the improvement is approved, you can create CIM phases, tasks, and identify impacted KPIs. The Improvement Coordinator for the improvement works with the Improvement Manager to plan implementation.
locale: en-US
release: xanadu
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Managing improvements, Continual Improvement Management, IT Service Management]
---

# Prepare an improvement

Once the improvement is approved, you can create CIM phases, tasks, and identify impacted KPIs. The Improvement Coordinator for the improvement works with the Improvement Manager to plan implementation.

## Before you begin

Role required: sn\_cim.improvement\_manager, sn\_cim.improvement\_coordinator

## About this task

Plan your implementation as phases to keep track of your project milestones. Add tasks to the phase and monitor the progress for the milestones. You can also track your goals by creating tasks directly from the initiatives.

![CIM implementation process](../image/cim-implement.png "Continual Improvement Management Implementation Process")

Preconditions:

-   Improvement Requester created the improvement request.
-   Improvement Manager accepted and assigned the improvement request.
-   Approver group member assessed and approved the improvement.

## Procedure

1.  Determine phases and tasks needed for the improvement.

    Improvement Manager and Improvement Coordinator meet to determine the tasks required to complete the improvement, and whether multiple phases are required.

2.  Set up CIM phases to track CIM tasks.

    1.  Navigate to **Continual Improvement** &gt; **Open** and open the improvement in the **In Progress** state.

    2.  In the CIM Phases related list, click **New** and fill in the description and planned end date.

    3.  Right-click the form header and select **Save**.

    4.  In the CIM Tasks related list, click **New** to create a CIM task.

    5.  In the **Parent** field, select the a CIM Phase record to which you want to associate the CIM task.

    6.  Set the CIM task attributes, including assignment, priority, state, planned end date, and short description.

    7.  Click **Submit**.

3.  Create and assign CIM tasks for an improvement.

    1.  In the CIM Tasks related list, click **New** to create a CIM task.

        By default, the CIM task is linked to the CIM initiative. To track the task within a phase, in the **Parent** field, select the a CIM Phase record to which you want to associate the CIM task.

    2.  Set the CIM task attributes, including assignment, priority, state, planned end date, and short description.

        **Note:**

        -   When the planned end date for a CIM task is updated, the planned end date that the CIM initiative that the task is associated with also gets updated. When the state for a CIM task is moved to Work In Progress, the Actual Start Date field is automatically updated with the current date.
        -   When the task is assigned, the task assignee receives an email notification.
4.  To create a separate application task for an [integrated application](../reference/cim-integration.md), click the related link for that application task.

5.  To monitor a KPI with the improvement, add a record to the Impacted KPIs tab.

6.  Meet with CIM task owners to oversee status, monitor work completed, add or update tasks and phases, and track overall progress of the improvement to completion.

    1.  Oversee the progress of CIM tasks with task owners on a regular basis until all tasks are presented as complete.

    2.  On the Improvement Initiative form, verify that all tasks in the CIM Tasks related list are **Closed Complete**.

        The improvement coordinator and task assignee receive an email notification when the task is moved to **Close Incomplete**, **Closed Skipped**, or **Closed Complete** state.

    3.  On the Improvement Initiative form, verify that all phases in the CIM Phases related list are 100% complete.

7.  Click **Review** in the header bar to request the improvement be reviewed by the Improvement Manager for closure.


## Implement improvement

In the process of reviewing KPI performance in the Performance Analytics application, the incident manager noticed the **Average time to resolve an incident** KPI scorecard was too high \(24 hours\).

As part of the implementation process, the Improvement Manager and Improvement Coordinator determined the work required in the next three to six months to complete the improvement, with a target review date 3 months after start.

-   Configured default CIM Phase 1 \(added two CIM tasks\), and created CIM Phase 2 \(added two CIM tasks\).
-   Created a Change Management application task record \(CHG0030001\) associated with CIM Task 2 using the **Create Change** related link, and set the change record attributes.
-   Added four KPIs to the Impacted KPIs tab to monitor with the improvement.

Improvement Coordinator met with CIM task owners regularly to oversee status and monitor work completed, and set the improvement status to review after all implementation was complete.

<table id="table_b4w_hkj_4cb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Number

</td><td>

CIMT0000116 \(assigned internally\)

</td></tr><tr><td>

Parent

</td><td>

CIM0000135

</td></tr><tr><td>

Percent complete

</td><td>

0

</td></tr><tr><td>

Planned end date

</td><td>

2018-06-19

</td></tr><tr><td>

Actual end date

</td><td>

--

</td></tr><tr><td>

Short description

</td><td>

Resolved incident and reassigned count improvements

</td></tr><tr><td class="sub-head" colspan="2">

CIM Task 1

</td></tr><tr><td>

Number

</td><td>

CIMT0000118 \(assigned internally\)

</td></tr><tr><td>

Parent

</td><td>

CIMT0000116

</td></tr><tr><td>

Configuration item

</td><td>

--

</td></tr><tr><td>

Active

</td><td>

\(Selected\)

</td></tr><tr><td>

Implementing task

</td><td>

--

</td></tr><tr><td>

Assigned to

</td><td>

Bernard Laboy

</td></tr><tr><td>

Improvement register

</td><td>

CIM0000135

</td></tr><tr><td>

Priority

</td><td>

4 - Low

</td></tr><tr><td>

State

</td><td>

Open

</td></tr><tr><td>

Planned end date

</td><td>

2018-06-19

</td></tr><tr><td>

Short description

</td><td>

Improve % of incidents resolved by first assigned group by using self service and more automation

</td></tr><tr><td>

Work notes

</td><td>

--

</td></tr><tr><td class="sub-head" colspan="2">

CIM Task 2

</td></tr><tr><td>

Number

</td><td>

CIMT0000119 \(assigned internally\)

</td></tr><tr><td>

Parent

</td><td>

CIMT0000116

</td></tr><tr><td>

Configuration item

</td><td>

--

</td></tr><tr><td>

Active

</td><td>

\(Selected\)

</td></tr><tr><td>

Implementing Task

</td><td>

CHG0030001

</td></tr><tr><td>

Assigned to

</td><td>

Change Manager

</td></tr><tr><td>

Improvement register

</td><td>

CIM0000135

</td></tr><tr><td>

Priority

</td><td>

4 - Low

</td></tr><tr><td>

State

</td><td>

Open

</td></tr><tr><td>

Planned end date

</td><td>

2018-06-19

</td></tr><tr><td>

Short description

</td><td>

Reduce the reassigned count by using ServiceNow Auto Categorization and Auto Assignment models

</td></tr><tr><td>

Work notes

</td><td>

--

</td></tr></tbody>
</table>|Field|Value|
|-----|-----|
|Number|CIMT0000120|
|Parent|CIM0000135|
|Percent complete|0|
|Planned end date|2018-06-19|
|Actual end date|--|
|Short description|Knowledge improvements and self-service improvements|
|CIM Task 1|
|Number|CIMT0000121 \(assigned internally\)|
|Parent|CIMT0000120|
|Configuration item|--|
|Active|\(Selected\)|
|Implementing task|--|
|Assigned to|David Loo|
|Improvement register|CIM0000135|
|Priority|4 - Low|
|State|Open|
|Planned end date|2018-06-19|
|Short description|Add new KB articles for common issues|
|Work notes|--|
|CIM Task 2|
|Number|CIMT0000123 \(assigned internally\)|
|Parent|CIMT0000120|
|Configuration item|--|
|Active|\(Selected\)|
|Implementing task|--|
|Assigned to|Adela Cervantsz|
|Improvement register|CIM0000135|
|Priority|4 - Low|
|State|Open|
|Planned end date|2018-06-19|
|Short description|Provide training and enablement training for new apps|
|Work notes|--|

<table id="table_yjt_jqy_2db"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Number

</td><td>

CHG0030001 \(set internally\)

</td></tr><tr><td>

Requested by

</td><td>

Improvement Manager

</td></tr><tr><td>

Configuration item

</td><td>

--

</td></tr><tr><td>

Planned start date

</td><td>

2018-03-18

</td></tr><tr><td>

Planned end date

</td><td>

2018-06-19

</td></tr><tr><td>

Type

</td><td>

Normal

</td></tr><tr><td>

State

</td><td>

New

</td></tr><tr><td>

Priority

</td><td>

4 - Low

</td></tr><tr><td>

Impact

</td><td>

3 - Low

</td></tr><tr><td>

Risk

</td><td>

Moderate

</td></tr><tr><td>

Short description

</td><td>

Reduce the reassigned count by using ServiceNow Auto Categorization and Auto Assignment models.

</td></tr><tr><td>

Description

</td><td>

--

</td></tr></tbody>
</table><table id="table_gkj_gmp_2db"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Impacted KPI

</td><td>

-   % of incidents resolved by first assigned group
-   % of incidents resolved on same day opened
-   % of incidents resolved without reassignment
-   Average age open incidents

</td></tr></tbody>
</table>**Parent Topic:**[Managing improvements](../concept/cim-improvement-initiative-mgmt.md)

**Related topics**  


[Improvement field descriptions](../reference/cim-field-descriptions.md)

[Improvement integration with other applications](../reference/cim-integration.md)

