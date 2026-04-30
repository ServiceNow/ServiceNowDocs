---
title: Download a data visualization from a dashboard
description: As a viewer, download individual data visualizations from a dashboard or the Visualization Designer. Output formats differ between Lists and other data visualizations. The available output formats are CSV, Excel, PNG and JPEG.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [View, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Download a data visualization from a dashboard

As a viewer, download individual data visualizations from a dashboard or the Visualization Designer. Output formats differ between Lists and other data visualizations. The available output formats are CSV, Excel, PNG and JPEG.

## Before you begin

**Important:**

-   The options to export data visualizations other than List to CSV or Excel are available only if you install the Data Visualizations Bundle version 6.2 or later from the ServiceNow® Store.
-   Indicator scorecards and calendar reports cannot be downloaded from the visualization.
-   Pivot tables and single score data visualizations can only be downloaded as CSV or Excel \(.xls\) files.
-   Boxplots can only be downloaded as JPEG or PNG files.
-   List visualizations support several export formats but not graphic files.

Role required: Anyone viewing a data visualization can export that visualization from a dashboard or the Visualization Designer through the visualization's **More actions** menu.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Open the desired dashboard.

3.  Select the More options 3-dot menu in the visualization you want to export.

4.  For supported data visualizations other than Lists, select the export format:

5.  For lists, follow these steps on the visualization's More options 3-dot menu:

    1.  Select **Export**.

        ![Export option under More Options for a data visualization.](../../par-for-workspace/image/dv-moreoptions-list.png)

    2.  Select the desired file type from the Export list.

        -   Excel
        -   CSV
        -   JSON
        -   PDF
        ![Export file type options](../../par-for-workspace/image/list-export-from-db.png)

    3.  Select the delivery type.

        All file types support download and email. PDF also supports an Accessible PDF format.

    4.  If you chose to email the file, specify the email address.


## Result

The file is saved to the download folder of your browser, unless you are emailing a list.

**Parent Topic:**[View data visualizations](../concept/view-data-visualizations.md)

