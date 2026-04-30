---
title: Migrate financial baselines of projects to Next Experience
description: Migrate the financial baselines of your project to Next Experience to manage the financial using Project Workspace.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Define a project, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Migrate financial baselines of projects to Next Experience

Migrate the financial baselines of your project to Next Experience to manage the financial using Project Workspace.

## About this task

Next Experience uses new data model which has two new tables Investment Baselines \(sn\_invst\_pln\_invst\_investment\_baseline\) and Investment Baseline Header \(sn\_invst\_pln\_invst\_investment\_baseline\_header\) which are used to capture financial baselines. The financial baselines created for demands in classic experience are not visible in Next Experience. You can migrate the existing baselines from classic to Next Experience as an on-demand activity for the required projects, or as bulk by activating and running a scheduled job.

Baselines view in the Next Experience provides better insights to view and analyze the financial performance of your projects.

Unlike the financial baselines created using Next Experience, the financial baselines created in the Classic UI do not capture the actual expenses along with planned costs as a default behavior. To have relevant information for baselines comparison, the actual costs will be captured as part of the baseline migration using the processed expense lines as of the baseline creation date of the financial baseline.

For detailed information and use cases on using financials in Next Experience, see [Managing financials for planning items in Portfolio Planning](../../portfolio-planning/concept/using-financials-pp.md).

**Note:** Migration of financial baselines is not applicable for demands or projects with multi-currency.

![Flow chart explaining the logical flow of migrating a financial baseline from classic to Next Experience.](../../pw-financials/images/fin_baseline_migration_logical_flow_no_background.png)

## Before you begin

Role required: it\_project\_manager

## Procedure

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **All**.

2.  Migrate baselines using one of the following options.

<table id="choicetable_v4j_f5z_d1c"><thead><tr><th align="left" id="d44461e137">

Choice

</th><th align="left" id="d44461e140">

Description

</th></tr></thead><tbody><tr><td id="d44461e146">

**Using list actions**

</td><td>

1.  Select the required projects from the projects list.
2.  Select the **Actions on selected rows...** list and select **Migrate Financial Baselines**.
3.  Select **OK** on the Migrate Financial Baselines confirmation window.


</td></tr><tr><td id="d44461e176">

**Using related links**

</td><td>

1.  Open the required project.
2.  Select the **Migrate Financial Baselines** related link.


</td></tr><tr><td id="d44461e197">

**Activate a scheduled job**

</td><td>

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
2.  Filter the Name field to locate the **Migrate financial baselines to Next Experience** scheduled job and open it.
3.  Select **Active** and on the Scheduled Script Execution form, fill the fields.

For a description of the field names, see [Scheduled Script Execution Form](gen-labor-costs-scheduled-job-ppm.md#).

4.  Select **Update**.


</td></tr></tbody>
</table>    **Tip:** After migration, you're encouraged to create financial baselines using the Financials in Next Experience.


## Result

Financial baselines for the selected projects will be migrated to Next Experience and you can view them in the [Baseline view](../../pw-financials/concept/using-financials-prj-wrkspc.md#section_bkp_g2l_2zb).

## What to do next

[View and compare the migrated baselines](../../pw-financials/task/create-compare-baselines-pws.md) with any existing baselines or current baseline \(![Flag icon to indicate current baseline.](../../spw-financials/images/fin-current-baseline-flag.png)\).

**Parent Topic:**[Define a project](t_CreateAProject.md)

**Related topics**  


[Create and manage waterfall projects](../../project-portfolio-suite/concept/c_CreateAndManageWaterfallProjects.md)

[Copy a project](t_CopyAProject.md)

[Create baseline of a project](t_CreateAProjectBaseline.md)

[Assign a project schedule](t_UseAProjectSchedule.md)

[Create a project cost plan](t_CreateAProjectCostPlan.md)

[Create a monetary benefit plan for a project](create-project-benefit-plan.md)

[Create a non-monetary benefit plan for a project](create-a-non-monetary-benefit-plan-for-a-project.md)

[Associate monetary and non-monetary benefit plans](associate-monetary-and-non-monetary-benefit-plans-project.md)

[Project and portfolio funding](../../project-portfolio-suite-with-financials/concept/c_ProjectAndPortfolioFunding.md)

[Create an expense line](t_CreateAExpenseLine.md)

[Generate labor costs](gen-cost-pln-prj-wrkspc.md)

[Migrate budget of active projects to Next Experience](fin-migrate-budget-project-ppm.md)

[Create a project status report](t_CreateAProjectStatusReport.md)

[View project status reports](project-status-report.md)

[Create a cost type definition](t_CreateAResourceTypeDefinition.md)

[Allocate budget to a project](allocate-budget-to-project.md)

[RIDAC records for a project in Project Workspace](../concept/ridac-entries-for-project.md)

