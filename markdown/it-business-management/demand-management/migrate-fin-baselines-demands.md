---
title: Migrate financial baselines of demands to Next Experience
description: Migrate the financial baselines of demands to Next Experience to manage the financial using Project Workspace.
locale: en-US
release: australia
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a demand, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Migrate financial baselines of demands to Next Experience

Migrate the financial baselines of demands to Next Experience to manage the financial using Project Workspace.

## About this task

Next Experience uses new data model that has two new tables Investment Baselines `(sn_invst_pln_invst_investment_baseline)` and Investment Baseline Header `(sn_invst_pln_invst_investment_baseline_header)` which are used to capture financial baselines. The financial baselines created for demands in classic experience aren’t visible in Next Experience. You can migrate the existing baselines from classic to Next Experience as an on-demand activity for the required demands, or as bulk by activating and running a scheduled job.

Baselines view in the Next Experience provides better insights to view and analyze the financial performance of your demands.

Unlike the financial baselines created using Next Experience, the financial baselines created in the Classic UI don’t capture the actual expenses along with planned costs as a default behavior. To have relevant information for baselines comparison, the actual costs are captured as part of the baseline migration using the processed expense lines as of the baseline creation date of the financial baseline.

For detailed information and use cases on using financials in Next Experience, see [Managing financials for planning items in Portfolio Planning](../../portfolio-planning/concept/using-financials-pp.md).

**Note:** Starting March 2026 release, for customers using multicurrency, migration of financial baselines updates the baseline data in project currency to investment currency.

1.  Existing demands that have only financial baselines but no investment baselines. With the migration, financial baseline will be migrated to investment baseline and you can view the migrated baseline from the `sn_invst_pln_invst_investment_baseline` table list view.
2.  Existing demands that have both project and investment baselines, you need to run the scheduled job to populate the fields for investment currency in the baselines with the values from project currency. For more information, see [Activate scheduled job to populate to multicurrency fields](../../spw-financials/task/multi-currency-scheduled-job-spw.md).

![Flow chart explaining the logical flow of migrating a financial baseline from classic to Next Experience.](../../pw-financials/images/fin_baseline_migration_logical_flow_no_background.png)

## Before you begin

The data in project currency fields will be migrated to investment currency fields on migrating baselines for customers using multicurrency.

Role required: it\_demand\_manager

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.

2.  Migrate baselines using one of the following options.

<table id="choicetable_v4j_f5z_d1c"><thead><tr><th align="left" id="d93684e164">

Choice

</th><th align="left" id="d93684e167">

Description

</th></tr></thead><tbody><tr><td id="d93684e173">

**Using list actions**

</td><td>

1.  Select the required demands from the projects list.
2.  Select the **Actions on selected rows...** list and select **Migrate Financial Baselines**.
3.  Select **OK** on the Migrate Financial Baselines confirmation window.


</td></tr><tr><td id="d93684e203">

**Using related links**

</td><td>

1.  Open the required demand.
2.  Select the **Migrate Financial Baselines** related link.


</td></tr><tr><td id="d93684e224">

**Activate a scheduled job**

</td><td>

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
2.  Filter the Name field to locate the **Migrate financial baselines to Next Experience** scheduled job and open it.
3.  Select **Active** and on the Scheduled Script Execution form, fill the fields.

For a description of the field names, see [Scheduled Script Execution Form](../../project-management/reference/scheduled-script-execution-form.md).

4.  Select **Update**.


</td></tr></tbody>
</table>    **Tip:** After migration, you're encouraged to create financial baselines using the Financials in Next Experience.


## Result

Financial baselines for the selected demands are migrated to Next Experience and you can view them in the [Baselines view](../../portfolio-planning/concept/using-financials-pp.md#section_bkp_g2l_2zb).

## What to do next

[View and compare the migrated baselines](../../portfolio-planning/task/create-compare-baselines-pp.md) with any existing baselines or current baseline \(![Flag icon to indicate current baseline.](../../spw-financials/images/fin-current-baseline-flag.png)\).

**Parent Topic:**[Create a demand](t_CreatingDemands.md)

