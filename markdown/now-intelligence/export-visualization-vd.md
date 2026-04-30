---
title: Export a visualization from the Visualization Designer
description: Export individual data visualizations to various formats and sizes. Download the exports or share them over email.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-02-01"
reading_time_minutes: 2
keywords: [export report, export pdf, export ppt, export image, export png]
breadcrumb: [Platform Analytics]
---

# Export a visualization from the Visualization Designer

Export individual data visualizations to various formats and sizes. Download the exports or share them over email.

## Before you begin

Exporting a data visualization 

Role required: You can export any visualization that you created or that was shared with you. Users with the admin or viz\_admin role can export any data visualizations.

## About this task

**Note:** You cannot export calendar reports or indicator scorecards.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select the **Data Visualizations** tab.

3.  Select the visualization that you want to export.

4.  From the More actions menu \(![](../../dashboards/image/icon-vert-3dot-p.png)\), select **Export**.

    ![Export option in More actions menu](../image/paw-vd-export.png)

    The Export Visualization dialog opens.

5.  In the File to export section, configure the following information.

<table id="table_fsx_mlr_rwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File type

</td><td>

Export data visualizations in PDF, PNG, or JPEG format. Select **Embedded PNG** to embed a PNG in the email body instead of sending it as an attached file or ZIP. You can edit the email around the image.List - Simple visualizations can be exported as PDF or Excel files.

</td></tr><tr><td>

Page format

</td><td>

Select Letter, A4, or A3 to correspond to the paper dimensions of the printed visualization. If you are exporting a pivot table, you can select Dynamic to resize the visualization to the page being viewed.You cannot set page format for List - Simple visualizations.

</td></tr><tr><td>

Orientation

</td><td>

Choose Portrait or Landscape. You cannot select the orientation for Pivot tables with Dynamic format or for List - Simple visualizations.

</td></tr></tbody>
</table>6.  Under **Delivery**, select **Download file** or **Send file via email.**

    -   When you choose to download the file, a **Download** button is available after the export is complete. The file, named `<visualization-name>.<filetype>`, is downloaded to your default local destination.
    -   When you send the file by email, you can select users and groups on your instance or any allowed email address. Security constraints may restrict who you can email. You also must specify a subject, and you can add a message. When you are done, select **Export**.

        **Note:** To send email to persons who are not on your instance, you need to have outbound email configured. See [Outbound Email Configuration](https://developer.servicenow.com/dev.do#!/learn/courses/xanadu/app_store_learnv2_automatingapps_xanadu_automating_application_logic/app_store_learnv2_automatingapps_xanadu_notifications/app_store_learnv2_automatingapps_xanadu_outbound_email_configuration) in the Developer Site.


-   **[Schedule data visualization export](schedule-visn-export-vd.md)**  
Automate the export and mailing of data visualizations. Help colleagues build presentations, share information with external users, or track data over time.

**Parent Topic:**[Platform Analytics](../../performance-analytics/concept/c_performanceAnalyticsAndReporting.md)

