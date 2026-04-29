---
title: Export a data visualization from the Visualization Designer
description: Export individual data visualizations to various formats and sizes. Download the exports or share them over email.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 2
keywords: [Export a visualization, Export a report, Export a visualization to PDF, Export a visualization to PNG, Export a visualization to JPEG, Export a list visualization to Excel]
breadcrumb: [Share, edit, or delete, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Export a data visualization from the Visualization Designer

Export individual data visualizations to various formats and sizes. Download the exports or share them over email.

## Before you begin

Role required: You can export any visualization that you created or that was shared with you. Users with the admin or viz\_admin role can export any data visualizations.

## About this task

Not all visualizations support all output types. Some export options shown in the UI for a visualization may not be valid. Consult the following table.

| |Supported data visualization export formats|
|---|-------------------------------------------|
|Calendar reports, Indicator scorecards, Pivot tables, Geomap|None|
|Lists|PDF, Microsoft Excel \(.xls or .xlsx\), Embedded LIST, CSV|
|Other data visualizations|PowerPoint, PDF, PNG, JPEG, Embedded PNG|
|Non-data visualization dashboard elements, like Headings|Not applicable|

Data visualizations exported to PowerPoint include the title and the description if this information is provided in the source visualization.

**Note:**

If you have any Now Assist applications installed, you can probably export a dashboard conversationally through the Now Assist panel. See [Export dashboards and data visualizations from the Now Assist panel](export-db-dv-now-assist-panel.md).

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

2.  Select the visualization that you want to export.

3.  From the More actions menu ![](../image/icon-paw-more-actions.png), select **Export**.

    ![Export option in More actions menu](../image/paw-vd-export.png)

4.  In the File to export section, configure the following information.

<table id="table_fsx_mlr_rwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File type

</td><td>

Export data visualizations in one of their supported formats. \(See [Supported export formats for different data visualization](export-visualization-vd.md#table_jlh_tr2_3fc).\) Select **Embedded PNG** or **Embedded LIST** to embed the exported file in the email body instead of sending it as an attached file or ZIP. You can edit the email around the image.

</td></tr><tr><td>

Page format

</td><td>

For PDF, PNG, Embedded PNG, and JPEG, select Letter, A4, or A3 to correspond to the paper dimensions of the printed visualization.You cannot set the page format when exporting a List.

</td></tr><tr><td>

Orientation

</td><td>

Choose Portrait or Landscape. Not available when exporting to Microsoft PowerPoint, Microsoft Excel, or CSV formats.

</td></tr></tbody>
</table>5.  Under **Delivery**, select **Download file** or **Send file via email**.

    -   When you choose to download the file, a **Download** button is available after the export is complete. The file, named `<visualization-name>.<filetype>`, is downloaded to your default local destination.
    -   When you send the file by email, you can select users and groups on your instance or any allowed email address. Security constraints may restrict who you can email. You also must specify a subject, and you can add a message. When you are done, select **Export**.

        **Note:** To send email to persons who are not on your instance, make sure outbound email is configured. See [Outbound Email Configuration](https://developer.servicenow.com/dev.do#!/learn/courses/xanadu/app_store_learnv2_automatingapps_xanadu_automating_application_logic/app_store_learnv2_automatingapps_xanadu_notifications/app_store_learnv2_automatingapps_xanadu_outbound_email_configuration) in the Developer Site.


**Parent Topic:**[Common data visualization tasks](../../reporting/concept/common-dv-tasks.md)

