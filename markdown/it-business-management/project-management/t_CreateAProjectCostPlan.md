---
title: Create a project cost plan
description: Project cost plans capture the costs of projects. Create a cost plan to specify the unit cost of a cost type for a fiscal period.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Define a project, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a project cost plan

Project cost plans capture the costs of projects. Create a cost plan to specify the unit cost of a cost type for a fiscal period.

## Before you begin

Role required: it\_project\_manager

Application required: Project Portfolio Management with Financials

## About this task

The application automatically creates [cost plan breakdown records](../concept/cost-plan-breakdown.md#) when you save the cost plan. Cost plans can also have associated [expense lines](t_CreateAExpenseLine.md).

**Note:** Cost plans are automatically created for resource plans that are associated to projects and project tasks.

To use multiple currencies, create a new cost plan for another currency.

## Procedure

1.  Open the project form.

2.  In the related links, click **Cost Plans**.

3.  Click **New**.

    **Note:** To create a cost plan from the **Financials** tab in Project Workspace, click **Manage**.

4.  On the form, fill in the fields.

<table id="table_mb3_rfw_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name of the cost plan.

</td></tr><tr><td>

Project/Demand

</td><td>

Project or demand to which the cost plan belongs.

</td></tr><tr><td>

Start fiscal period

</td><td>

Indicates the starting fiscal period.When you change the start fiscal period, the associated cost plan breakdowns also change. Start fiscal period also changes when you create cost plan breakdowns earlier than the start fiscal period.

</td></tr><tr><td>

End fiscal period

</td><td>

Indicates the ending fiscal period.When you change the end fiscal period, the associated cost plan breakdowns also change. End fiscal period also changes when you create cost plan breakdowns later than the end fiscal period.

</td></tr></tbody>
</table><table id="table_uq5_1pz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entered currency

</td><td>

Currency in which you want the cost plan to be created. If the selected currency is different from the functional currency, the corresponding [budget reference rate](../concept/c_BudgetReferenceRates.md) is used to calculate the total planned cost, planned capital, planned operating of the project.

</td></tr><tr><td>

Unit cost

</td><td>

Cost of a single unit of the resource, which is in terms of entered currency.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of the resource that is required.

</td></tr><tr><td>

Recurring

</td><td>

Option to indicate that the cost is recurring for each fiscal period. **Quantity** x **Unit cost** incurred for every fiscal period.

</td></tr><tr><td>

Cost type

</td><td>

[Cost type definition](t_CreateAResourceTypeDefinition.md).

</td></tr><tr><td>

Investment

</td><td>

Name of the investment created for the project.

 This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Source type

</td><td>

Funding entity to associated with the project investment for funding.

 This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Source

</td><td>

Funding entity value from which you request fund.

 The field is available when you select a value in the **Source type** field.

 This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Total planned cost

</td><td>

Total estimated cost of the cost plan. If the cost is recurring, the calculation is **Quantity** x **Unit cost** x **number of fiscal periods**. If the cost is non-recurring, the calculation is **Quantity** x **Unit cost**.

</td></tr><tr><td>

Functional currency

</td><td>

Currency that is obtained from the [**glide.system.locale** property](https://www.servicenow.com/docs/access?context=currency-properties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).For upgraded customers, if the selected currency is different from the functional currency configured in the Financial Management application, the corresponding [budget reference rate](../concept/c_BudgetReferenceRates.md) is used to calculate the total planned cost, planned capital, planned operating of the project.

 **Note:** If budget reference rates are not defined, then exchange rate is considered as 1. For example, if functional currency is USD, entered cost is EUR, and no exchange rate is defined, then 1000 USD equals to 1000 EUR.

</td></tr><tr><td>

Cost in functional currency

</td><td>

Value that is rolled up from the **Functional cost** field of all cost plan breakdowns.

</td></tr><tr><td>

Total actual cost

</td><td>

Value that is rolled up from the **Actual cost** field of all cost plan breakdowns.

</td></tr><tr><td>

Estimate at Completion

</td><td>

Sum of all actuals for past fiscal periods added to the functional cost for future fiscal periods.For example, the duration of a project is from January 01 to December 31, and if you check the Estimate at Completion in the month of May, it is calculated as: `Sum of actuals from Jan to April + Sum of functional cost from May to December`.

</td></tr></tbody>
</table>    **Note:** When you change the planned start date of a project, the associated cost plans and resource plan also change. The [project property](../reference/r_InstalledWithProjectManagement.md#project_application_properties) **Change Resource Plan and Cost Plan Start Date with Demand or Project Start Date Change** controls the behavior for project start date change.

5.  Click **Submit**.


## What to do next

To recalculate the values in the **Estimate at Completion** field, use the **Calculate Estimate at Completion** related link. To view the cost plan breakdowns, click the **Cost Plan Breakdowns** related list.

-   **[Cost plan breakdown](../concept/cost-plan-breakdown.md#)**  
A cost plan breakdown captures the estimated cost and actual cost for every fiscal period. Cost plan, project, demand, program, and portfolio are the breakdowns types that are available.
-   **[System-generated cost plans](../concept/system-generated-costplan.md)**  
When an expense line is created without populating the **Cost Plan** field, system-generated cost plans are created automatically.

**Parent Topic:**[Define a project](t_CreateAProject.md)

**Related topics**  


[Create and manage waterfall projects](../../project-portfolio-suite/concept/c_CreateAndManageWaterfallProjects.md)

[Copy a project](t_CopyAProject.md)

[Create baseline of a project](t_CreateAProjectBaseline.md)

[Assign a project schedule](t_UseAProjectSchedule.md)

[Create a monetary benefit plan for a project](create-project-benefit-plan.md)

[Create a non-monetary benefit plan for a project](create-a-non-monetary-benefit-plan-for-a-project.md)

[Associate monetary and non-monetary benefit plans](associate-monetary-and-non-monetary-benefit-plans-project.md)

[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)

[Create an expense line](t_CreateAExpenseLine.md)

[Generate labor costs](gen-cost-pln-prj-wrkspc.md)

[Migrate budget of active projects to Next Experience](fin-migrate-budget-project-ppm.md)

[Migrate financial baselines of projects to Next Experience](migrate-fin-baselines-projects.md)

[Create a project status report](t_CreateAProjectStatusReport.md)

[View project status reports](project-status-report.md)

[Create a cost type definition](t_CreateAResourceTypeDefinition.md)

[Allocate budget to a project](allocate-budget-to-project.md)

[RIDAC records for a project in Project Workspace](../concept/ridac-entries-for-project.md)

