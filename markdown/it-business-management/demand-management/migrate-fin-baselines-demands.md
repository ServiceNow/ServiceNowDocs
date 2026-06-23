---
title: Migrate financial baselines of demands to Next Experience
description: Migrate the financial baselines of demands to Next Experience to manage the financial using Project Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/demand-management/migrate-fin-baselines-demands.html
release: yokohama
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a demand, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Migrate financial baselines of demands to Next Experience

Migrate the financial baselines of demands to Next Experience to manage the financial using Project Workspace.

## About this task

Next Experience uses new data model which has two new tables Investment Baselines \(sn\_invst\_pln\_invst\_investment\_baseline\) and Investment Baseline Header \(sn\_invst\_pln\_invst\_investment\_baseline\_header\) which are used to capture financial baselines. The financial baselines created for demands in classic experience are not visible in Next Experience. You can migrate the existing baselines from classic to Next Experience as an on-demand activity for the required demands, or as bulk by activating and running a scheduled job.

Baselines view in the Next Experience provides better insights to view and analyze the financial performance of your demands.

Unlike the financial baselines created using Next Experience, the financial baselines created in the Classic UI do not capture the actual expenses along with planned costs as a default behavior. To have relevant information for baselines comparison, the actual costs will be captured as part of the baseline migration using the processed expense lines as of the baseline creation date of the financial baseline.

For detailed information and use cases on using financials in Next Experience, see [Managing financials for planning items in Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/portfolio-planning/using-financials-pp.md).

**Note:** Migration of financial baselines is not applicable for demands or projects with multi-currency.

\[Omitted image "fin\_baseline\_migration\_logical\_flow\_no\_background.png"\] Alt text: Flow chart explaining the logical flow of migrating a financial baseline from classic to Next Experience.

## Before you begin

Role required: it\_demand\_manager

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.

2.  Migrate baselines using one of the following options.

<table id="choicetable_v4j_f5z_d1c"><thead><tr><th align="left" id="d44568e137">

Choice

</th><th align="left" id="d44568e140">

Description

</th></tr></thead><tbody><tr><td id="d44568e146">

**Using list actions**

</td><td>

1.  Select the required demands from the projects list.
2.  Select the **Actions on selected rows...** list and select **Migrate Financial Baselines**.
3.  Select **OK** on the Migrate Financial Baselines confirmation window.


</td></tr><tr><td id="d44568e176">

**Using related links**

</td><td>

1.  Open the required demand.
2.  Select the **Migrate Financial Baselines** related link.


</td></tr><tr><td id="d44568e197">

**Activate a scheduled job**

</td><td>

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
2.  Filter the Name field to locate the **Migrate financial baselines to Next Experience** scheduled job and open it.
3.  Select **Active** and on the Scheduled Script Execution form, fill the fields.

For a description of the field names, see [Scheduled Script Execution Form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/project-management/scheduled-script-execution-form.md).

4.  Select **Update**.


</td></tr></tbody>
</table>    **Tip:** After migration, you're encouraged to create financial baselines using the Financials in Next Experience.


## Result

Financial baselines for the selected demands will be migrated to Next Experience and you can view them in the [Baselines view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/portfolio-planning/using-financials-pp.md).

## What to do next

[View and compare the migrated baselines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/portfolio-planning/create-compare-baselines-pp.md) with any existing baselines or current baseline \(\[Omitted image "fin-current-baseline-flag.png"\] Alt text: Flag icon to indicate current baseline.\).

**Parent Topic:**[Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/demand-management/t_CreatingDemands.md)

