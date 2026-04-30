---
title: Create a report
description: Create a report to visualize and analyze current instance data or temporary data that you have imported.Enter a question on the Report Designer form, and Analytics Q&amp;A generates a report. Analytics Q&amp;A gives you a choice of data sources and picks an appropriate visualization.When you edit a form, you can also choose to save, share, run, delete, or view more information about the report.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-11-17"
reading_time_minutes: 6
breadcrumb: [Core UI Reporting, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a report

Create a report to visualize and analyze current instance data or temporary data that you have imported.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

This topic refers to Reporting in the Core UI. If your instance is migrated to Platform Analytics experience, see [Creating data visualizations](../concept/creating-data-visualizations.md).

## Procedure

1.  Follow one of these paths.

<table id="choicetable_urt_hlc_5w"><tbody><tr><td id="d173553e75">

**Create a report**

</td><td>

Navigate to **Reports** &gt; **Create New**.

</td></tr><tr><td id="d173553e93">

**Edit an existing report**

</td><td>

Navigate to **Reports** &gt; **View / Run** and click the edit icon \(![The edit icon](../image/Pencil.png)\) beside the report name.

</td></tr><tr><td id="d173553e115">

**Create a report on a dashboard**

</td><td>

Navigate to the dashboard where you want to add the report, click the Add Widgets icon \(![Plus sign button](../../dashboards/image/AddWidgetButton.png)\), and select **Reports**.

</td></tr><tr><td id="d173553e133">

**Edit a report on a dashboard**

</td><td>

Navigate to the dashboard where the report resides and click **Edit**. To edit a report, click its edit icon \(![Pencil](../image/Pencil.png)\).

</td></tr></tbody>
</table>2.  On the **Configure** and **Style** tabs, fill in the fields, as appropriate.

3.  Click **Save**.

    The report is generated.

    **Note:** For details on creating a specific report type, see [Report types](../reference/report-types-creation-details-rd.md).


**Parent Topic:**[Using reporting](../concept/c_GenerateReports.md)

## Create a report with Analytics Q&amp;A

Enter a question on the Report Designer form, and Analytics Q&amp;A generates a report. Analytics Q&amp;A gives you a choice of data sources and picks an appropriate visualization.

### Before you begin

Analytics Q&amp;A requires Natural Language Query \(NLQ\).

NLQ also must be enabled for use with the Report Designer, in [Reporting properties](../reference/reporting-properties.md). Check with your administrator.

**Note:** This topic refers to Reporting in the Core UI. This functionality is not available if your instance is migrated to Platform Analytics experience. For more information, see [Data visualizations in Platform Analytics](../../performance-analytics/concept/analytics-center-data-visualizations.md).

Analytics Q&amp;A is not available when using Microsoft Internet Explorer.

Role required: None

### About this task

Analytics Q&amp;A supports the following languages:

-   English
-   French
-   Canadian French
-   Spanish
-   German
-   Japanese

The feature is not available in sessions that use an unsupported language.

### Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **Create New**.

2.  Start typing what information you want in the report into the Analytics Q&amp;A field.

    Analytics Q&amp;A uses keywords in your query to determine what kind of information you are looking for. It displays suggestions while you type based on these keywords. To see a full list of keywords and their uses, click **How can I improve my results?**.

3.  Click **Ask**.

    Analytics Q&amp;A generates the report, including an appropriate visualization.![Animation showing a report being generated with Analytics Q&A](../image/nlq-generates-report.gif)


### What to do next

You can modify the report, such as changing the visualization, in the left-margin menu. If you enter a new query and click **Ask**, you generate a new report. Any custom visualizations you added are cleared, but other settings persist in the new report.

**Related topics**  


[Analytics Q&amp;A](../../performance-analytics/concept/analytics-q-and-a.md)

## Report options

When you edit a form, you can also choose to save, share, run, delete, or view more information about the report.

**Note:**

On net new Yokohama instances and instances migrated to Platform Analytics experience, Reporting functionality is replaced with Data Visualizations. For more information, see [Data visualizations in Platform Analytics](../../performance-analytics/concept/analytics-center-data-visualizations.md).

All actions are available from the upper right side of the form, from the **Save** and **Share** lists and the **Info**, **Delete**, and **Run** buttons. Available report options vary depending on the role of the user working with the report.

![report options icons](../image/report-sources-icons.png)

<table id="table_uj5_mny_5r"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Link \(![Link icon](../image/link-icon.png)\)

</td><td>

Displays the URL of a saved report that you can copy into other documents.

</td></tr><tr><td>

Info \(![Info icon](../../../common/image/Form_ReferenceLookupIcon.png)\)

</td><td>

Displays general and statistical information for the report. General information includes the base table, type, creator, users, groups, and last modification date of the report. Statistical information includes when the report was last run, the number of runs, and run time.

</td></tr><tr><td>

Sharing \(![Sharing icon](../../../common/image/Form_ShareIcon.png)\)

</td><td>

Displays several options for sharing the output of the report.

</td></tr><tr><td>

Share

</td><td>

Enables you to set the visibility of the report. Options are **Me**, **Everyone**, and **Groups and Users**. See [Share a report](t_ShareASetting.md) for more information on sharing.This option is available from the Sharing icon \(![Sharing icon](../../../common/image/Form_ShareIcon.png)\).

</td></tr><tr><td>

Schedule

</td><td>

Creates a schedule for running the report. **Note:** You cannot schedule calendar reports.

</td></tr><tr><td>

Add to Dashboard

</td><td>

Adds the current report to a dashboard. For details on how to edit reports and other dashboard content, see [Edit a responsive dashboard](../../dashboards/task/t_EditADashboard.md).

</td></tr><tr><td>

Export to PDF

</td><td>

Generates a PDF that you can download or email. This option is not available for calendar reports.**Note:** Drilldown reports do not export to PDF. If you select **Export to PDF** on a drilldown report, a PDF of the top-level report is generated.

</td></tr><tr><td>

Publish

</td><td>

Creates a URL for the report and displays the URL above the report form. You can email this URL to share the report.

</td></tr><tr><td class="sub-head" colspan="2">

Delete

</td></tr><tr><td>

Delete \(![Delete icon](../../../common/image/Form_DeleteIcon.png)\)

</td><td>

Deletes the report.

</td></tr><tr><td class="sub-head" colspan="2">

Save

</td></tr><tr><td>

Save

</td><td>

Saves your changes to the report and leaves the form open.

</td></tr><tr><td>

Update

</td><td>

Saves your changes to the report and returns to the Reports list.

</td></tr><tr><td>

Insert

</td><td>

Duplicates the report record, inserts it into the Reports list, and opens the Reports list. Use this option to create a report quickly by changing values in an existing report. Be sure to give the new report a unique name.

</td></tr><tr><td>

Insert and Stay

</td><td>

Duplicates the report record, inserts it into the Reports list, and opens the new record. Use this option to create a report quickly by changing values in an existing report. Be sure to give the new report a unique name.

</td></tr><tr><td>

Save as data source

</td><td>

Opens the [Create new report source](../concept/c_ReportSources.md#) window in which you can save the report conditions as a report source that can be reused for other reports.

</td></tr><tr><td class="sub-head" colspan="2">

Run

</td></tr><tr><td>

Run

</td><td>

Creates the report based on the conditions and layout you select.

</td></tr></tbody>
</table>**Related topics**  


[Administering reports](../concept/c_AdminsteringReports.md)

