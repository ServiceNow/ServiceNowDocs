---
title: Cost plan breakdown
description: A cost plan breakdown captures the estimated cost and actual cost for every fiscal period. Cost plan, project, demand, program, and portfolio are the breakdowns types that are available.Update a cost plan breakdown record that specifies the estimated and actual cost, at a granular level, for specific fiscal periods.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a project cost plan, Define a project, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Cost plan breakdown

A cost plan breakdown captures the estimated cost and actual cost for every fiscal period. Cost plan, project, demand, program, and portfolio are the breakdowns types that are available.

-   **Requirement**

    Requirement corresponds to a single cost plan. For example, for a regular calendar and a cost plan spanning across one year, 12 breakdowns would appear.

-   **Task**

    Task corresponds to a project or a demand. The cost across all the cost plans per period is rolled up to the project or demand level. These records have breakdown type set to **Task**. There would be only one record of type **Task** per period. The number of records of type **Task** that are created depends on the duration of the project or demand, and the requirements planned in the project or demand. For example, for a regular calendar and a project with three cost plans, 12 breakdowns appear.

-   **Program**

    If a project or a demand is part of a program, the breakdown type of **Program** provides the aggregate of program level costs per period.

-   **Portfolio**

    If a project or a demand is part of a portfolio, the breakdown type of **Portfolio** provides the aggregate of portfolio level costs per period.


**Parent Topic:**[Create a project cost plan](../task/t_CreateAProjectCostPlan.md)

## Update a cost plan breakdown

Update a cost plan breakdown record that specifies the estimated and actual cost, at a granular level, for specific fiscal periods.

### Before you begin

Role required: it\_project\_manager

### Procedure

1.  Open the required project.

2.  Click the **Cost Plan** related list.

3.  Click the **Cost Plan Breakdowns** related list.

4.  Click the **i** icon against a cost plan breakdown.

5.  Click **Open Record**.

6.  In the Cost Plan Breakdown form, view and update the enabled fields.

<table id="choicetable_os3_4p1_dcb"><thead><tr><th align="left" id="d95440e215">

Field

</th><th align="left" id="d95440e218">

Description

</th></tr></thead><tbody><tr><td id="d95440e224">

**Task**

</td><td>

Task to which the cost plan breakdown belongs.

</td></tr><tr><td id="d95440e233">

**Portfolio**

</td><td>

Portfolio to which the cost plan breakdown belongs.

</td></tr><tr><td id="d95440e242">

**Entered currency**

</td><td>

Currency specified in the cost plan.

</td></tr><tr><td id="d95440e251">

**Exchange rate**

</td><td>

Rate in effect for the period corresponding to the cost plan breakdown. When the period corresponding to the cost plan break down has multiple rates, the rate in effect on the first date of that period is used. Exchange rate is used to convert entered cost into functional cost. It is obtained from the itfm\_fx\_rate \[budget\_reference\_rates\] table.

</td></tr><tr><td id="d95440e264">

**Actual**

</td><td>

Actual cost generated from processed expense lines.

</td></tr><tr><td id="d95440e273">

**Cost plan**

</td><td>

Cost plan to which the cost plan breakdown belongs.

</td></tr><tr><td id="d95440e282">

**Fiscal period**

</td><td>

Fiscals generated at period level. For information on periods, see [fiscal calendars](https://www.servicenow.com/docs/access?context=c_FiscalCalendar&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr><tr><td id="d95440e295">

**Entered cost**

</td><td>

Breakdown amount in entered currency.

</td></tr><tr><td id="d95440e304">

**Functional cost**

</td><td>

Functional cost obtained by multiplying exchange rate with entered cost.

</td></tr><tr><td id="d95440e313">

**Exchange rate date**

</td><td>

First date of the fiscal period corresponding to the cost plan breakdown.

</td></tr></tbody>
</table>
