---
title: Create a demand cost plan
description: Demand cost plans capture the costs of demands. Create a cost plan to specify the unit cost of a cost type for a fiscal period.
locale: en-US
release: australia
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a demand, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a demand cost plan

Demand cost plans capture the costs of demands. Create a cost plan to specify the unit cost of a cost type for a fiscal period.

## Before you begin

Role required: it\_demand\_manager

## About this task

The application automatically creates cost plan breakdown records when you save the cost plan. The cost plan breakdowns are records that specify the estimated and actual costs and the budget at a granular level for specific fiscal periods, such as FY16: M04 and FY16: M05. The demand cost plans are added to the parent program and portfolio.

The cost plan breakdowns that specify the estimated cost and actual cost at a granular level for a fiscal period of the demand cost plan are recalculated in the project currency. Similarly, the estimated breakdown amounts of the planned benefit and actual benefit of the demand benefit plans are recalculated in the project currency. The project currency amounts are then rolled up to the cost plan, benefit plan, and the project records.

If you want to use multiple currencies, create a cost plan for another currency.

If you’re creating benefit plan for a demand with the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin activated and Demand Currency view enabled, the fields in the **Financials** section differ from the Default view. For more information about the fields that are available only in the Demand Currency view, see [Multicurrency fields in demand-related forms](../reference/multicurrency-fields-demand.md).

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All** and open the required demand form.

2.  In the related links, select **Cost Plans**.

3.  To view the Financials Summary page in a grid, select **Manage**.

4.  Add or edit a cost plan from the Cost Plans related list:

    -   To add a cost plan, select **New**.
    -   To update the details of an existing cost plan, select the record and then select **Manage**.
5.  In the cost plan form, fill in the fields.

    For a description of the field names, see [Cost plan form](../reference/demand-plan-form.md).

    **Note:** When you change the planned start date of a demand, the associated cost plans and resource assignments also change. The [project property](../../project-management/reference/r_InstalledWithProjectManagement.md#project_application_properties) **Change Resource Plan and Cost Plan Start Date with Demand or Project Start Date Change** controls the behavior for demand date change.

6.  Select **Submit**.


## What to do next

-   On the Demand form, view the breakdowns by fiscal period in the **Cost Breakdown** related list.
-   To recalculate the value in the **Forecast** field, use the **Calculate Forecast Amount** related link.

**Parent Topic:**[Create a demand](t_CreatingDemands.md)

