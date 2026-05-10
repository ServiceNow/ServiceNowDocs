---
title: Add, edit, or delete demand cost plans
description: Create a cost plan for a required duration to track your planned and actual expenses. Edit cost plans to adjust your planned expenses and delete any descoped forecasts.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage financials for demands, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Add, edit, or delete demand cost plans

Create a cost plan for a required duration to track your planned and actual expenses. Edit cost plans to adjust your planned expenses and delete any descoped forecasts.

## Before you begin

Role required: it\_demand\_manager

## About this task

The application automatically creates cost plan breakdown records when you save the cost plan. The cost plan breakdowns are records that specify the estimated and actual costs and the budget at a granular level for specific fiscal periods, such as FY16: M04 and FY16: M05. The demand cost plans are added to the parent program and portfolio.

If you want to use multiple currencies, create a cost plan for another currency.

If you’re creating a cost plan for a demand with the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin activated and Demand Currency view enabled, the fields in the **Financials** section differ from the Default view. For more information about the fields that are available only in the Demand Currency view, see [Multicurrency in Next Experience for Demand Management reference](../reference/multicurrency-in-dw-reference.md).

**Note:** For projects, the cost plan breakdowns specify the estimated cost and actual cost at a granular level for a fiscal period of the demand cost plan. These breakdowns are recalculated in the project currency. Similarly, the estimated breakdown amounts of the planned benefit and actual benefit of the demand benefit plans are recalculated in the project currency. The project currency amounts are then rolled up to the cost plan, benefit plan, and the project records.

## Procedure

1.  Open a demand from the home page of Next Experience for Demand Management.

    For more information, see [Access demands](access-demand-workspace.md).

2.  Select **Details** from the L-2 \(level 2\) navigation menu.

3.  Select **Cost Plans**.

    **Note:** If the **Cost Plans** tab isn’t visible, select **More** and then select **Cost Plans**.

<table id="choicetable_w3k_syh_pyb"><thead><tr><th align="left" id="d190937e136">

Choice

</th><th align="left" id="d190937e139">

Description

</th></tr></thead><tbody><tr><td id="d190937e145">

**To create a cost plan**

</td><td>

1.  Select **New**.
2.  On the Create New Cost Plan form, fill the fields.

For a description of the field names, see [Create cost plan form](../reference/cost-plan-form-dw.md).

3.  Select **Save**.


</td></tr><tr><td id="d190937e181">

**To edit a cost plan**

</td><td>

Select the name of the cost plan, edit the required details and select **Save**.

</td></tr><tr><td id="d190937e193">

**To view and manage cost plan breakdowns**

</td><td>

1.  Select the name of the cost plan.
2.  Select **Cost Plan Breakdowns**.
3.  Select a fiscal period.
    -   To edit a fiscal period record, edit the name and select **Save**.
    -   To delete a fiscal record, select **Delete** from the More Actions option in the fiscal period record form.


</td></tr><tr><td id="d190937e231">

**To create cost plan breakdowns**

</td><td>

1.  Select the name of the cost plan.
2.  Select **Cost Plan Breakdowns**.
3.  Select **New**. For more information about the fields, see [Create cost plan breakdown form](../reference/create-cost-plan-breakdown-form-dw.md).
4.  Select **Save**.


</td></tr><tr><td id="d190937e272">

**To delete a cost plan**

</td><td>

Delete a cost plan in one of the following ways:-   Select a record from the **Cost Plans** tab and select **Delete**.
-   Select **Delete** from the More Actions option in the cost plan form.
**Note:** Deleted cost plans and the associated expense lines can’t be recovered.

</td></tr></tbody>
</table>    **Tip:** [Create financial baselines](create-compare-financial-baselines-dw.md) immediately after capturing the initial planned costs to have a snapshot of your planned costs. Use this baseline to compare it against the baselines from later dates, as the work progresses, to identify the variance between initial planned costs and actual expenses.

    This step helps you to plan for the future expenses and re-forecast the planned costs.

    Alternatively, you can create, edit, or delete cost plans and cost plan breakdowns using the **Estimate financial cost** playbook activity. For more information, see [Use Playbooks](use-playbooks-in-dw.md).


**Related topics**  


[Use Playbooks](use-playbooks-in-dw.md)

[Demand default playbook stages and activities](../reference/demand-default-playbook-stages.md)

[Create cost plan form](../reference/cost-plan-form-dw.md)

[Create cost plan breakdown form](../reference/create-cost-plan-breakdown-form-dw.md)

