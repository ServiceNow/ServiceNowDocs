---
title: Update a monetary benefit plan breakdown for an epic
description: Update a monetary benefit plan breakdown record that specifies the estimated and actual benefits, at a granular level, for specific fiscal periods.
locale: en-US
release: yokohama
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a monetary benefit plan for an epic, Create an epic in Agile Development 2.0, Use, Agile Development 2.0, Strategic Portfolio Management]
---

# Update a monetary benefit plan breakdown for an epic

Update a monetary benefit plan breakdown record that specifies the estimated and actual benefits, at a granular level, for specific fiscal periods.

## Before you begin

Role required: scrum\_master, scrum\_product\_owner, or scrum\_admin

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Epics**.

2.  Open the required epic.

3.  Select **View** &gt; **Benefit** from the Additional actions menu \(![Hamburger icon](../image/hamburger-icon.png)\).

4.  Click the Monetary Benefit Plans related list.

5.  Open the required monetary benefit plan.

6.  In the Monetary Benefit Plan Breakdowns related list, click the information icon \(![information icon](../../planning-and-policy/image/informationicon.png)\) for a monetary benefit plan breakdown.

7.  Click **Open Record**.

8.  On the Monetary Benefit Plan Breakdown form, view and update the enabled fields.

<table id="choicetable_os3_4p1_dcb"><thead><tr><th align="left" id="d203562e131">

Field

</th><th align="left" id="d203562e134">

Description

</th></tr></thead><tbody><tr><td id="d203562e140">

**Task**

</td><td>

Task to which the benefit plan breakdown belongs.

</td></tr><tr><td id="d203562e149">

**Portfolio**

</td><td>

Portfolio to which the benefit plan breakdown belongs.

</td></tr><tr><td id="d203562e158">

**Entered currency**

</td><td>

Currency specified in the benefit plan.

</td></tr><tr><td id="d203562e167">

**Exchange rate**

</td><td>

Rate in effect for the period corresponding to the benefit plan breakdown. When the period corresponding to the benefit plan break down has multiple rates, the rate in effect on the first date of that period is used. Exchange rate is used to convert the entered benefit into the functional benefit. It is obtained from the itfm\_fx\_rate \[budget\_reference\_rates\] table.

</td></tr><tr><td id="d203562e180">

**Actual benefit**

</td><td>

Actual benefit that is incurred from the epic.

</td></tr><tr><td id="d203562e189">

**Benefit plan**

</td><td>

Benefit plan to which the benefit plan breakdown belongs.

</td></tr><tr><td id="d203562e198">

**Fiscal period**

</td><td>

Fiscals generated at the period level. For information on periods, see [fiscal calendars](https://www.servicenow.com/docs/access?context=c_FiscalCalendar&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td id="d203562e211">

**Entered benefit**

</td><td>

Benefit in entered currency.

</td></tr><tr><td id="d203562e220">

**Functional benefit**

</td><td>

Functional benefit obtained by multiplying the exchange rate with the entered benefit.

</td></tr><tr><td id="d203562e229">

**Exchange rate date**

</td><td>

First date of the fiscal period corresponding to the benefit plan breakdown.

</td></tr></tbody>
</table>9.  Click **Update**.


**Parent Topic:**[Create a monetary benefit plan for an epic](create-monetary-benefit-plan-agile-epic.md)

