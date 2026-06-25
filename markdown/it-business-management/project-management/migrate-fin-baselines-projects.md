---
title: Migrate financial baselines of projects to Next Experience
description: Migrate the financial baselines of your project to Next Experience to manage the financial using Project Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/migrate-fin-baselines-projects.html
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Starting a project, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Migrate financial baselines of projects to Next Experience

Migrate the financial baselines of your project to Next Experience to manage the financial using Project Workspace.

## About this task

Next Experience uses new data model that has two new tables Investment Baselines `(sn_invst_pln_invst_investment_baseline)` and Investment Baseline Header `(sn_invst_pln_invst_investment_baseline_header)` which are used to capture financial baselines. The financial baselines created for demands in classic experience aren’t visible in Next Experience. You can migrate the existing baselines from classic to Next Experience as an on-demand activity for the required projects, or as bulk by activating and running a scheduled job.

Baselines view in the Next Experience provides better insights to view and analyze the financial performance of your projects.

Unlike the financial baselines created using Next Experience, the financial baselines created in the Classic UI don’t capture the actual expenses along with planned costs as a default behavior. To have relevant information for baselines comparison, the actual costs are captured as part of the baseline migration using the processed expense lines as of the baseline creation date of the financial baseline.

For detailed information and use cases on using financials in Next Experience, see [Managing financials for planning items in Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/using-financials-pp.md).

**Note:** Starting March 2026 release, for customers using multicurrency, migration of financial baselines updates the baseline data in project currency to investment currency.

1.  Existing projects that have only project baselines but no investment baselines. With the migration, project baseline will be migrated to investment baseline and you can view the migrated baseline from the `sn_invst_pln_invst_investment_baseline` table list view.
2.  Existing projects that have both project and investment baselines, you need to run the scheduled job to populate the fields for investment currency in the baselines with the values from project currency. For more information, see [Activate scheduled job to populate to multicurrency fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/multi-currency-scheduled-job-spw.md).

## Before you begin

The data in project currency fields will be migrated to investment currency fields on migrating baselines for customers using multicurrency.

Role required: it\_project\_manager

## Procedure

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **All**.

2.  Migrate baselines using one of the following options.

<table id="choicetable_v4j_f5z_d1c"><thead><tr><th align="left" id="d50976e165">

Choice

</th><th align="left" id="d50976e168">

Description

</th></tr></thead><tbody><tr><td id="d50976e174">

**Using list actions**

</td><td>

1.  Select the required projects from the projects list.
2.  Select the **Actions on selected rows...** list and select **Migrate Financial Baselines**.
3.  Select **OK** on the Migrate Financial Baselines confirmation window.


</td></tr><tr><td id="d50976e204">

**Using related links**

</td><td>

1.  Open the required project.
2.  Select the **Migrate Financial Baselines** related link.


</td></tr><tr><td id="d50976e225">

**Activate a scheduled job**

</td><td>

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
2.  Filter the Name field to locate the **Migrate financial baselines to Next Experience** scheduled job and open it.
3.  Select **Active** and on the Scheduled Script Execution form, fill the fields.

For a description of the field names, see [Scheduled Script Execution Form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/scheduled-script-execution-form.md).

4.  Select **Update**.


</td></tr></tbody>
</table>    **Tip:** After migration, you're encouraged to create financial baselines using the Financials in Next Experience.


## Result

Financial baselines for the selected projects will be migrated to Next Experience and you can view them in the [Baseline view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/using-financials-prj-wrkspc.md).

## What to do next

[View and compare the migrated baselines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/create-compare-baselines-pws.md) with any existing baselines or current baseline \(\[Omitted image "fin-current-baseline-flag.png"\] Alt text: Flag icon to indicate current baseline.\).

**Parent Topic:**[Starting a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/t_CreateAProject.md)

**Related topics**  


[Create a project task from a project]()

[Create a parent-child relationship on the Project Task form]()

[Create a monetary benefit plan for a project]()

[Create a non-monetary benefit plan for a project]()

[Associate monetary and non-monetary benefit plans]()

[Create a project cost plan]()

[Recalculating costs of all resource plans in a project]()

[Create an expense line]()

[Create and manage waterfall projects]()

[Update a project]()

[Copy a project]()

[Assign a project schedule]()

[Create baseline of a project]()

[Create a milestone]()

[Activate project task email notifications]()

[Change the planned start date of a project]()

[Create a cost type definition]()

[Costing add-on in Project Management]()

[Generate labor costs]()

[Create a project status report]()

[Allocate budget to a project]()

[Migrate budget of active projects to Next Experience]()

[Migrate budget of active projects to Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/fin-migrate-budget-project-ppm.md)

