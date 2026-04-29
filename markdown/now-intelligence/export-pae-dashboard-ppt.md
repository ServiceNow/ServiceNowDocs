---
title: Export a Platform Analytics dashboard
description: Export a Platform Analytics experience dashboard to PDF or Microsoft PowerPoint.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Export a Platform Analytics dashboard

Export a Platform Analytics experience dashboard to PDF or Microsoft PowerPoint.

## Before you begin

Role required: Any, if the user has access to the dashboard.

**Note:**

-   This task only applies to dashboards created in the inline editor. Technical dashboards do not have the **Export** option in the **More actions** menu. For more information, see [Technical dashboards compared to inline dashboards](../../performance-analytics/reference/technical-vs-in-line-dashboards.md).
-   Pivot, calendar report, geomap, and indicator scorecard visualizations are not supported for export. Lists are not supported for export to PowerPoint. These visualization types will not appear in the exported file.
-   Only the supported data visualizations and Lists \(PDF\) are exported, not Headings or Rich Text or any other element.
-   Content is not necessarily exported in the order it appears on the dashboard.
-   Depending on your entitlements, you may be able export a dashboard conversationally through the Now Assist panel. See [Export dashboards and data visualizations from the Now Assist panel](../../par-for-workspace/task/export-db-dv-now-assist-panel.md).
-   Dashboards exported to PowerPoint include the title above and the description below each visualization in an editable format if this information is provided in the source visualization.

-   You can also export individual data visualizations from a dashboard to a PNG or JPEG file. For more information, see [Download a data visualization from a dashboard](../../performance-analytics/task/export-data-vis-from-dboard.md).

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Select the dashboard that you want to export.

3.  Select the dashboard's **More actions** menu ![More action icon](../../../product/customer-service-management/image/csm-ws-dashboards-more-actions-icon.png) and choose **Export**.

    ![More actions menu with Export item highlighted](../image/export-pae-db-menu-option.png)

4.  In **File type**, select PDF or PowerPoint.

    1.  If you are exporting to PDF, specify the page format and orientation.

        Any filter values set on the dashboard at the time of export apply to the export.

    2.  If you are exporting to PowerPoint, you can set the following options:

<table id="table_vxw_nnz_d2c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Export all tabs

</td><td>

If the dashboard has more than one tab, you can select whether to export them all or only a subset.Default: On

</td></tr><tr><td>

Export all visualizations in the top layout

</td><td>

If the dashboard has more than one tab and you are not exporting them all, you can set whether to export any visualizations that are in the layout outside the tabs.![Dashboard with visualizations in a tab and in the top layout.](../../par-for-workspace/image/db-top-level-layout-mini.png)

</td></tr><tr><td>

Select tabs:

</td><td>

If you are not exporting all tabs, select each tab to export.

</td></tr><tr><td>

Export with applied filters

</td><td>

You can select whether to apply to the export any values that have been set in filters on the dashboard. For example, say your dashboard has an Incident Category filter and a single-score visualization showing the number of incidents. With nothing chosen in the filter, the visualization shows 6884 incidents. With the Software category chosen in the filter, it shows only 5278 incidents. Now you export the dashboard with Software chosen in the filter. If **Export with applied filters** is on, the slide for that visualization shows 5278 incidents; with it turned off, it shows 6884.Default: On

</td></tr></tbody>
</table>        **Note:** For PowerPoint, the export creates a separate slide for each visualization in the dashboard, not one slide for each tab on the dashboard.

5.  Choose the delivery method, **Download file** or **Send via email**.

    |Delivery method|Result|
    |---------------|------|
    |Download file|When the export is complete, you are prompted to download the export.|
    |Send via email|Choose the users to send it to. You can select only users on your instance. Security constraints may restrict who you can email. You must specify a subject, and you can add a message.|

6.  Select **Export**.


## Result

The dashboard with selected tabs and filters is exported to a PDF or PowerPoint file and delivered by the chosen method.

**Parent Topic:**[Common dashboard tasks in the in-line editor](../concept/common-dashboard-tasks.md)

**Related topics**  


[Create a dashboard with the in-line editor](create-db-in-ac.md)

[Edit Platform Analytics dashboards](edit-db-in-ac.md)

[Share a Platform Analytics dashboard](share-db-in-ac.md)

[Duplicate a Platform Analytics dashboard](../../reporting/task/duplicate-db.md#)

[Print a Platform Analytics dashboard](printer-friendly-db-ac.md)

[Schedule the export of dashboards and data visualizations](../../par-for-workspace/task/schedule-export-dboards-data-viz.md)

[Bookmark a Platform Analytics dashboard](bookmark-dashboard-ac.md)

[Delete a Platform Analytics dashboard](delete-db-in-ac.md)

