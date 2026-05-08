---
title: Starting a project
description: Initiate a project by changing the project state to Work in Progress. Define important aspects of your Agile, Waterfall, or Hybrid project such as the duration, estimated cost, and net value to your organization to efficiently track the project's progress.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Starting a project

Initiate a project by changing the project state to **Work in Progress**. Define important aspects of your Agile, Waterfall, or Hybrid project such as the duration, estimated cost, and net value to your organization to efficiently track the project's progress.

## Before you begin

Role required: it\_project\_manager

## About this task

When you change the **State** field on the Project form to **Work in Progress**, the Actual start date of the project changes to the planned start date.

You can create a project from the Projects list or from the Project Workspace. You must have the Agile Development 2.0 plugin to create an Agile or Hybrid project and the Test Management plugin to create a test phase for your project.

**Note:** You can also create a project from the [demand workbench](../../planning-and-policy/task/t_CrtArtftDmdMnu.md).

After you start the project:

-   The read-only **Actual start date** field of the project is populated with the planned date.
-   If a task or set of tasks are scheduled to start immediately upon project start \(meaning that their time constraints are set to **Start ASAP** and they have no other start dependencies\), the actual start dates of those tasks also get populated with the planned date.
-   The planned start dates of all other tasks adjust accordingly based on the time you started the project. Their new planned start dates depend on several factors, including dependent relationships with other tasks and the duration for each task.

    **Note:** Once a project is in the **Work in Progress** state, it does not mean that the state of every task will start updating automatically based on planned start date. Other than the project tasks that you schedule to start **ASAP** when the project starts, project tasks are not started automatically. Continue to manage the project and change the state of each task to **Work in Progress**.


You can also use the multi-currency feature to create a project in a local currency different from your functional currency. You must enable the PPM Standard Multicurrency plugin \(com.snc.ppm\_multicurrency\) and switch to the Project Currency view for the additional fields in the **Financials** tab of the Project form. For more information, see [Multi-currency in project financials](../../project-portfolio-suite-with-financials/concept/multicurrency-pps.md).

## Procedure

1.  Create a project in any of the following ways.

<table id="choicetable_whk_swd_tw"><thead><tr><th align="left" id="d244821e150">

Location

</th><th align="left" id="d244821e153">

Steps

</th></tr></thead><tbody><tr><td id="d244821e159">

**From the Projects list**

</td><td>

Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **Create New**.

</td></tr><tr><td id="d244821e185">

**From the project workspace**

</td><td>

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **Project Workspace**.
2.  From Projects page, select the **New**.
3.  In the Create a project modal, fill in the details and select **Confirm**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

    For field information, see [../reference/create-a-project-form.md](../reference/create-a-project-form.md).

3.  Select **Submit**.


-   **[Create a project task from a project](t_CreateATaskFromAProject.md)**  
Create tasks from the project form to break down project objectives into manageable units of work.
-   **[Create a parent-child relationship on the Project Task form](t_CreateParentChildRelationship.md)**  
Create a child task from any project task form.
-   **[Create a monetary benefit plan for a project](create-project-benefit-plan.md)**  
Create a monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods. Project benefit plans capture the potential benefits accrued by the project when the project is executed.
-   **[Create a non-monetary benefit plan for a project](create-a-non-monetary-benefit-plan-for-a-project.md)**  
Create a non-monetary benefit plan to specify the estimated benefit in a category spanning one or more fiscal periods. Project benefit plans capture the potential non-financial benefits accrued by the project when the project is executed.
-   **[Associate monetary and non-monetary benefit plans](associate-monetary-and-non-monetary-benefit-plans-project.md)**  
Associate monetary and non-monetary benefit plans, so that you can capture the potential benefits \(financial and non-financial\) accrued by the project for the hybrid benefit plans.
-   **[Create a project cost plan](t_CreateAProjectCostPlan.md)**  
Create a cost plan to specify the unit cost of a cost type for a fiscal period. Project cost plans capture the costs of projects.
-   **[Recalculating costs of all resource plans in a project](recalculate-resource-costs-of-a-project.md)**  
Recalculate the resource costs of all resource plans in a project whenever the hourly rates change in the associated rate model so that the plan costs are up to date.
-   **[Create an expense line](t_CreateAExpenseLine.md)**  
A project expense line is cost associated with a specific source, such as a user, fixed asset, or a CI. Expense lines are part of project cost plans.
-   **[Create and manage waterfall projects](../../project-portfolio-suite/concept/c_CreateAndManageWaterfallProjects.md)**  
Plan, create, and manage projects using the Waterfall methodology.
-   **[Schedule a project from a start date](schedule-a-project-pm.md)**  
Schedule a project from a start date and plan tasks and milestones based on your project requirements.
-   **[Apply or change a task constraint](change-task-constraint-project-management.md)**  
Apply a constraint to control when an automatically scheduled task starts or finishes. Set the constraint type and the associated constraint date if required.
-   **[Update a project](t_UpdateAProjectInProgress.md)**  
Update the project and make adjustments in fields to handle scope, cost, and schedule. While a project is underway, keep actual values as current as possible. Continue to measure actual values, analyze the impact of any potential project risks.
-   **[Copy a project](t_CopyAProject.md)**  
Another option for creating a project is to copy an existing project with all its tasks and relationships. After you specify the start date for the copy, the system adjusts all task start and end dates automatically.
-   **[Assign a project schedule](t_UseAProjectSchedule.md)**  
Without an assigned schedule, a project calculates a day as a full 24 work hours. To schedule tasks by a more realistic work day, assign a schedule to the project. If the schedules provided in the base system do not suit your needs, define a new one.
-   **[Create baseline of a project](t_CreateAProjectBaseline.md)**  
Create a schedule baseline and financial baseline of a project. A schedule baseline captures planned dates of all tasks and milestones at a particular moment in time. A financial baseline captures benefit and financial metric information \(snapshot of cost plan, benefit plan, and project-level financial metrics\) at a particular moment in time.
-   **[Create a milestone](t_CreateMilestones.md)**  
A milestone is a project task with a duration of zero \(0\). Use milestones to mark key dates in your project, such as key decision points, approvals, and holidays. Milestones are treated like any other project task and you can create dependencies between tasks and milestones.
-   **[Activate project task email notifications](t_ActivateProjTaskEmailNot.md)**  
The following email notifications for the Project Management application are available by default, but are inactive. You must activate them manually.
-   **[Change the planned start date of a project](change-planned-start-date-of-project.md)**  
Adjust the schedule of a project by changing the planned start date of a project and shifting it later or earlier than the current planned schedule.
-   **[Create a cost type definition](t_CreateAResourceTypeDefinition.md)**  
Create a cost type definition to associate a cost type, operating, or capital, to an account in the General Ledger from the Financial Management application. Create a cost type definition if you are using Project Portfolio Management with Financials.
-   **[Costing add-on in Project Management](../concept/c_ProjectManagementCostingAddOn.md)**  
The Project Management costing add-on connects the Project Management application to the Cost Management application to allow for estimating and tracking the costs associated with projects.
-   **[Generate labor costs](gen-cost-pln-prj-wrkspc.md)**  
Generate labor costs based on the planning attributes configured for financials in the planning attributes page for the resource assignments in a project.
-   **[Create a project status report](t_CreateAProjectStatusReport.md)**  
Create project status report from the related lists of the project form. The project status report created for the most recent status date updates the status of the project in portfolios.
-   **[Allocate budget to a project](allocate-budget-to-project.md)**  
Set the budget of a project according to the fiscal years.
-   **[Migrate budget of active projects to Next Experience](fin-migrate-budget-project-ppm.md)**  
Migrate the project budget to Next Experience to manage the financials using Project Workspace.
-   **[Migrate financial baselines of projects to Next Experience](migrate-fin-baselines-projects.md)**  
Migrate the financial baselines of your project to Next Experience to manage the financial using Project Workspace.

**Parent Topic:**[Using Project Management](../concept/using-project-management.md)

**Related topics**  


[../reference/create-a-project-form.md](../reference/create-a-project-form.md)

[Schedule a project from a start date](schedule-a-project-pm.md)

[Project Portfolio Management](../../project-portfolio-suite/concept/c_ProjectPortfolioSuite.md)

