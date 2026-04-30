---
title: Allocate budget to a demand
description: Set the budget of a demand according to the fiscal years.
locale: en-US
release: yokohama
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a demand, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Allocate budget to a demand

Set the budget of a demand according to the fiscal years.

## Before you begin

Role required: it\_portfolio\_manager

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All** and open the demand form.

2.  In the related links, click **Demand Budget**.

    The **Demand Budget** dialog box opens.

3.  Select the fiscal year for which you want to set the budget for the demand.

    **Tip:** You can work on allocating lean budget at fiscal period level using the Investment Budget. For more information, see [Enable lean budgeting for demands](config-investment-budget-demand.md).

4.  Enter the amounts for **Capex Budget** and **Opex Budget**.

    The **Total Budget** is updated with the sum of capex and opex amounts.

5.  Click **OK**.

    **Note:**

    -   If the demand does not have a cost plan, start date, and due date, then demand budget is distributed from current month until the end of demand budget fiscal year.
    -   If the demand does not have a cost plan and a due date but has a start date, then demand budget is distributed from either:
        -   Start date \(if start date falls in the given budget fiscal year\) until the end of the demand budget fiscal year.
        -   Start of the demand budget fiscal year until the end of the demand budget fiscal year.
    -   If the demand does not have a cost plan and a start date but has a due date, then demand budget is distributed from either:
        -   Current month until due date \(if due date falls in the given budget fiscal year\).
        -   Current month until the end of demand budget fiscal year.
    If the demand has a cost plan associated, then demand budget is distributed by honoring the cost plan fiscal periods.


## Result

The demand budget for the selected year appears in the **Demand Budget** related list. You can click the amounts in the list to revise them.

**Parent Topic:**[Create a demand](t_CreatingDemands.md)

