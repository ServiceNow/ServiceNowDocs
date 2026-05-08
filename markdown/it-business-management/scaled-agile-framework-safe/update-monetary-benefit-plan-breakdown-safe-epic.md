---
title: Update a monetary benefit plan breakdown for an epic
description: Update a monetary benefit plan breakdown record that specifies the estimated and actual benefits, at a granular level, for specific fiscal periods.
locale: en-US
release: australia
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a monetary benefit plan for an epic, Define an epic in SAFe, SAFe entities, Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Update a monetary benefit plan breakdown for an epic

Update a monetary benefit plan breakdown record that specifies the estimated and actual benefits, at a granular level, for specific fiscal periods.

## Before you begin

Role required: safe\_product\_owner, safe\_scrum\_master, or safe\_admin

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Epics**.

2.  Open the required epic.

3.  Click the hamburger icon \(![Hamburger icon](../../agile-development/image/hamburger-icon.png)\) and navigate to **View** &gt; **Benefit**.

4.  Click the Monetary Benefit Plans related list.

5.  Open the required monetary benefit plan.

6.  In the Monetary Benefit Plan Breakdowns related list, click the information icon for a monetary benefit plan breakdown.

7.  Click **Open Record**.

8.  On the Monetary Benefit Plan Breakdown form, view and update the enabled fields.

<table id="choicetable_os3_4p1_dcb"><thead><tr><th align="left" id="d256924e125">

Field

</th><th align="left" id="d256924e128">

Description

</th></tr></thead><tbody><tr><td id="d256924e134">

**Task**

</td><td>

Task to which the benefit plan breakdown belongs.

</td></tr><tr><td id="d256924e143">

**Portfolio**

</td><td>

Portfolio to which the benefit plan breakdown belongs.

</td></tr><tr><td id="d256924e152">

**Entered currency**

</td><td>

Currency specified in the benefit plan.

</td></tr><tr><td id="d256924e161">

**Exchange rate**

</td><td>

Rate in effect for the period corresponding to the benefit plan breakdown. When the period corresponding to the benefit plan break down has multiple rates, the rate in effect on the first date of that period is used. Exchange rate is used to convert the entered benefit into the functional benefit. It is obtained from the itfm\_fx\_rate \[budget\_reference\_rates\] table.

</td></tr><tr><td id="d256924e174">

**Actual benefit**

</td><td>

Actual benefit that is incurred from the epic.

</td></tr><tr><td id="d256924e183">

**Benefit plan**

</td><td>

Benefit plan to which the benefit plan breakdown belongs.

</td></tr><tr><td id="d256924e192">

**Fiscal period**

</td><td>

Fiscals generated at the period level. For information on periods, see [fiscal calendars](https://www.servicenow.com/docs/access?context=c_FiscalCalendar&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td id="d256924e205">

**Entered benefit**

</td><td>

Benefit in entered currency.

</td></tr><tr><td id="d256924e214">

**Functional benefit**

</td><td>

Functional benefit obtained by multiplying the exchange rate with the entered benefit.

</td></tr><tr><td id="d256924e223">

**Exchange rate date**

</td><td>

First date of the fiscal period corresponding to the benefit plan breakdown.

</td></tr></tbody>
</table>9.  Click **Update**.


**Parent Topic:**[Create a monetary benefit plan for an epic](create-monetary-benefit-plan-safe-epic.md)

