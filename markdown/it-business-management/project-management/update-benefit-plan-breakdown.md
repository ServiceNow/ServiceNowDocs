---
title: Update a monetary benefit plan breakdown for a project
description: Update a monetary benefit plan breakdown record that specifies the estimated and actual benefits, at a granular level, for specific fiscal periods.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a monetary benefit plan for a project, Define a project, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Update a monetary benefit plan breakdown for a project

Update a monetary benefit plan breakdown record that specifies the estimated and actual benefits, at a granular level, for specific fiscal periods.

## Before you begin

Role required: it\_project\_manager

## Procedure

1.  Navigate to **Project** &gt; **Projects** &gt; **All**.

2.  Open the required project.

3.  Click the Monetary Benefit Plans related list.

4.  Open the required monetary benefit plan.

5.  In the Monetary Benefit Plan Breakdowns related list, click the information icon \(![information icon](../../planning-and-policy/image/informationicon.png)\) for a monetary benefit plan breakdown.

6.  Click **Open Record**.

7.  On the Monetary Benefit Plan Breakdown form, view and update the enabled fields.

<table id="choicetable_os3_4p1_dcb"><thead><tr><th align="left" id="d67179e117">

Field

</th><th align="left" id="d67179e120">

Description

</th></tr></thead><tbody><tr><td id="d67179e126">

**Task**

</td><td>

Task to which the benefit plan breakdown belongs.

</td></tr><tr><td id="d67179e135">

**Portfolio**

</td><td>

Portfolio to which the benefit plan breakdown belongs.

</td></tr><tr><td id="d67179e144">

**Entered currency**

</td><td>

Currency specified in the benefit plan.

</td></tr><tr><td id="d67179e153">

**Exchange rate**

</td><td>

Rate in effect for the period corresponding to the benefit plan breakdown. When the period corresponding to the benefit plan break down has multiple rates, the rate in effect on the first date of that period is used. Exchange rate is used to convert the entered benefit into the functional benefit. It is obtained from the itfm\_fx\_rate \[budget\_reference\_rates\] table.

</td></tr><tr><td id="d67179e166">

**Actual benefit**

</td><td>

Actual benefit that is incurred from the project or demand.

</td></tr><tr><td id="d67179e175">

**Benefit plan**

</td><td>

Benefit plan to which the benefit plan breakdown belongs.

</td></tr><tr><td id="d67179e184">

**Fiscal period**

</td><td>

Fiscals generated at the period level. For information on periods, see [fiscal calendars](https://www.servicenow.com/docs/access?context=c_FiscalCalendar&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr><tr><td id="d67179e197">

**Entered benefit**

</td><td>

Benefit in entered currency.

</td></tr><tr><td id="d67179e206">

**Functional benefit**

</td><td>

Functional benefit obtained by multiplying the exchange rate with the entered benefit.

</td></tr><tr><td id="d67179e215">

**Exchange rate date**

</td><td>

First date of the fiscal period corresponding to the benefit plan breakdown.

</td></tr></tbody>
</table>8.  Click **Update**.

    **Note:** Changing benefit plan start and end date is not possible if the recorded actual benefits are outside of the date range.


**Parent Topic:**[Create a monetary benefit plan for a project](create-project-benefit-plan.md)

