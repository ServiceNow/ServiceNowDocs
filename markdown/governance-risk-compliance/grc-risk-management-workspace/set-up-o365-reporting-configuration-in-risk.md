---
title: Set up Microsoft 365 reporting configuration in risk
description: Set up the Microsoft 365 reporting configuration records to specify the data points and reports that you want to import in to a Microsoft Word document for risk reporting purposes.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating Microsoft 365 with Management Reporting of Risk, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Set up Microsoft 365 reporting configuration in risk

Set up the Microsoft 365 reporting configuration records to specify the data points and reports that you want to import in to a Microsoft Word document for risk reporting purposes.

## Before you begin

Role required: sn\_risk\_advanced.ara\_admin

## About this task

Data is imported into a Microsoft Word document for risk reporting purposes. You must specify which tables and reports from your ServiceNow instance must be used to import data into the Microsoft Word. You can also specify the columns from a table from which you want to import data. Only those reports that are either created by or shared with the Risk administrator are available for selection.

## Procedure

1.  Navigate to **All** &gt; **Management Reporting of Risk** &gt; **Microsoft 365 Reporting Integration** &gt; **Reporting Configurations**.

2.  From the Microsoft 365 reporting configurations list, select **New**.

3.  On the Microsoft 365 reporting configuration form, fill in the fields.

<table id="table_lh1_zzx_5vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business domain

</td><td>

Domain from where the configuration is created. This field is automatically set to **Risk**.

</td></tr><tr><td>

Reporting item

</td><td>

Name of the configuration. For example, if you want to get data about your Risk statement in your word document, you can provide a name such as `Risk statement`.

</td></tr><tr><td>

Source type

</td><td>

Source from which you want to fetch the data. The choices are as follows:-   **Table**: Select this option when you want to import data from a table.
-   **Report**: Select this option if you want to import data from a predefined report or chart. For more information on how to create a report, see [Create a report with Analytics Q&amp;A](https://www.servicenow.com/docs/access?context=t_CreateYourOwnReport&version=australia&pubname=australia-now-intelligence&section=create-report-nlq&ft:locale=en-US).
 **Note:** Only list reports, pivot reports, multi-level pivot reports, horizontal and vertical bar charts, and pie charts are available for selection. Stacked bar charts and grouped bar charts aren’t supported.

</td></tr><tr><td>

Source table

</td><td>

Source table to fetch data from. This field only appears when **Table** is selected from the **Source type** field.

</td></tr><tr><td>

Filter

</td><td>

Filter conditions to filter the records. This field only appears when **Table** is selected from the **Source type** field.

</td></tr><tr><td>

Columns

</td><td>

Column from the table whose values are to be inserted. This field only appears when **Table** is selected from the **Source type** field.

</td></tr><tr><td>

Source report

</td><td>

Available report to be inserted in the disclosure report. This field only appears when **Report** is selected from the **Source type** field.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the record is active. Only active records are available for selection in the document.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

Add additional reporting configuration filters to the reporting configuration. These filters help to fetch the data into your Microsoft Word disclosure report. For more information, see [Add additional reporting configuration filters for a Microsoft 365 configuration record in risk](add-additional-reporting-filters-risk-reporting.md).

