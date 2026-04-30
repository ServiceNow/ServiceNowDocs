---
title: Export a responsive dashboard to PDF
description: Export a dashboard as a PDF so you can archive, print, or distribute it.It's possible to export any dashboard or homepage to PDF using your browser's print functionality.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-06-18"
reading_time_minutes: 3
breadcrumb: [Working with responsive dashboards, Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Export a responsive dashboard to PDF

Export a dashboard as a PDF so you can archive, print, or distribute it.

## Before you begin

This topic refers to Dashboards in the Core UI.

Roles required: No role is required to export dashboards to PDF, however, an admin has to configure the instance for PDF export. See [Enable PDF export of dashboards](../../dashboards/task/enable-pdf-export.md) for more information.

## About this task

Interactive filters that are applied to the dashboard are also applied to the PDF. However, applied breakdowns are not included in the export.

**Note:** To generate the PDF locally, set the interactive filters, click the user icon, and select **Printer Friendly Version**. The dashboard opens in a new window or tab. Export the dashboard using the print settings of the browser.

![Opening printer friendly version.](../image/polaris-printer-friendly.png)

If you do not have Next Experience activated, select **Printer Friendly Version** from the **Settings** menu.

![](../image/settings-icon.png)

Limitations:

-   Custom content may not generate as expected when exported to PDF. For more information, see [Custom content PDF export limitations](../../dashboards/reference/custom-content-pdf-export-limitations.md).
-   Dashboards that are exported to PDF do not include the dashboard layout. Widgets are stacked on top of each other and take up the full page width.
-   Widgets are exported to a fixed height. Large widgets, such as workbench or list widgets, are truncated.
-   Calendar reports exported from a dashboard may be truncated because exporting calendar reports to PDF is not supported.
-   Breakdowns applied to a dashboard are not included in the PDF.
-   Widgets may appear in a different order than on the dashboard.
-   Widget legends may not appear.
-   Exports do not include data tables associated with report visualizations. You can export individual reports separately, including their data tables. To include data tables in scheduled reports, check **Display data table** on the report's Configure tab in Report Designer.
-   Coloring on the delta text for single score report widgets is not preserved.
-   PDFs do not reflect the selected time frame when you select the **Show date range selector** at the widget level.
-   It is not possible to export responsive dashboards as templates.

**Note:** PDFs that are sent as emails may not be generated immediately.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  From the dashboard picker in the upper left, select the dashboard that you want to export.

3.  Click the context menu \(![Context menu icon](../../../common/image/Form_MenuIcon.png)\) and select **Export to PDF**.

    ![Context menu with Export to PDF highlighted](../../dashboards/image/export-resp-db-pdf.png)

4.  Configure your print and delivery options.

    ![Export to PDF pop-up with print and delivery options: Print all dashboard tabs, orientation, paper size, and delivery options, generate now and send as email](../../dashboards/image/export-pdf-print-del-options.png)

5.  Click **Export**.


## Result

The content is exported to PDF according to the print and delivery options. If the PDF does not generate, identify and resolve any JavaScript errors.

## Export a dashboard using the browser's print function

It's possible to export any dashboard or homepage to PDF using your browser's print functionality.

### Before you begin

Roles required: No role is required to export dashboards to PDF using the browser's print function.

### About this task

You can use your browser's print functionality to export a PDF on demand, and to export a PDF with applied breakdowns. In scheduled PDFs, breakdowns are not applied to the data.

### Procedure

1.  Open the dashboard that you want to export.

2.  Set the interactive filters.

3.  Select your user icon to show the Settings menu.

    ![User settings menu with Printer friendly version menu item outlined](../../dashboards/image/user-menu-printer-friendly.png)

    A browser tab opens with the dashboard's widgets stacked one on top of another.

4.  In the new browser tab, select the tab to print, the page size, and the page orientation.

5.  Select **Print**.

6.  In your browser's Print dialogue, select PDF as the print destination or output.


### Result

The dashboard tab is exported to PDF with your chosen page size and orientation.

