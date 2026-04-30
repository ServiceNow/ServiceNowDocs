---
title: Create a monetary benefit plan for a demand
description: Demand benefit plans capture the potential benefits accrued by the demand when the demand is executed. Create a monetary benefit plan to specify the estimated benefit in a category for a fiscal period.
locale: en-US
release: yokohama
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a demand, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a monetary benefit plan for a demand

Demand benefit plans capture the potential benefits accrued by the demand when the demand is executed. Create a monetary benefit plan to specify the estimated benefit in a category for a fiscal period.

## Before you begin

Role required: it\_demand\_manager

## About this task

The monetary benefit plan breakdown records are automatically created when you save the benefit plan. The monetary benefit plan breakdown records specify the estimated and actual benefits at a granular level for specific fiscal periods, such as FY16: M04 and FY16: M05. The Monetary Benefit Plan Breakdowns related list shows the aggregated benefits for estimated and actual benefits for each fiscal period for the demand.

**Note:** Converting a demand to a project or EAP entity transfers the benefit plan from the demand to the target project or EAP entity.

If you’re creating benefit plan for a demand with the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin activated and Demand Currency view enabled, the fields in the **Financials** section differ from the Default view. For more information about the fields that are available only in the Demand Currency view, see [Multicurrency fields in demand-related forms](../reference/multicurrency-fields-demand.md).

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.

2.  Open the required demand form.

3.  Select the Monetary Benefit Plans related list.

4.  To create a monetary benefit plan, select **New**.

    **Note:** To create a monetary benefit plan from the **Financials Summary** page, select **Manage**.

5.  On the Monetary Benefit Plan form, fill in the fields.

    For a description of the field names, see [Monetary Benefit Plan form](../reference/monetary-benefit-plan-form.md).

    **Note:** When you move the demand dates, the associated benefit plans also change accordingly based on whether the benefit plan is tied to the demand start date, or end date. The [project property](../../project-management/reference/r_InstalledWithProjectManagement.md#project_application_properties) **Change Resource Plan, Cost Plan and Benefit Plan Start Date with Demand or Project Start Date Change** controls the behavior for demand date changes.

6.  Select **Submit**.


## What to do next

On the Benefit Plan form, view the benefit breakdown by fiscal period in the Monetary Benefit Plan Breakdowns related list.

-   **[Update a monetary benefit plan breakdown for a demand](update-a-monetary-benefit-plan-breakdown-for-a-demand.md)**  
Update a monetary benefit plan breakdown record that specifies the estimated and actual benefits, at a granular level, for specific fiscal periods.

**Parent Topic:**[Create a demand](t_CreatingDemands.md)

