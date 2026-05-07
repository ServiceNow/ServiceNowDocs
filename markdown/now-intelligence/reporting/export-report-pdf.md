---
title: Export a report to PDF
description: Export a report to PDF to use it outside of your ServiceNow instance.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-04-01"
reading_time_minutes: 1
breadcrumb: [Distribute reports, Core UI Reporting, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Export a report to PDF

Export a report to PDF to use it outside of your ServiceNow instance.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. The information in the exported report is only the information that you have the right to access.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select the Core UI report you want to export.

2.  From the More actions menu ![](../../par-for-workspace/image/icon-paw-more-actions.png), select **Export**.

    ![Export option in More actions menu](../../par-for-workspace/image/paw-vd-export.png)

3.  In the File to export section, configure the following information.

<table id="table_fsx_mlr_rwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File type

</td><td>

Export data visualizations in one of their supported formats. \(See [Supported export formats for different data visualization](../../par-for-workspace/task/export-visualization-vd.md#table_jlh_tr2_3fc).\) Select **Embedded PNG** or **Embedded LIST** to embed the exported file in the email body instead of sending it as an attached file or ZIP. You can edit the email around the image.

</td></tr><tr><td>

Page format

</td><td>

For PDF, PNG, Embedded PNG, and JPEG, select Letter, A4, or A3 to correspond to the paper dimensions of the printed visualization.You cannot set the page format when exporting a List.

</td></tr><tr><td>

Orientation

</td><td>

Choose Portrait or Landscape. Not available when exporting to Microsoft PowerPoint, Microsoft Excel, or CSV formats.

</td></tr></tbody>
</table>4.  Under **Delivery**, select **Download file** or **Send file via email**.

    -   When you choose to download the file, a **Download** button is available after the export is complete. The file, named `<visualization-name>.<filetype>`, is downloaded to your default local destination.
    -   When you send the file by email, you can select users and groups on your instance or any allowed email address. Security constraints may restrict who you can email. You also must specify a subject, and you can add a message. When you are done, select **Export**.

        **Note:** To send email to persons who are not on your instance, make sure outbound email is configured. See [Outbound Email Configuration](https://developer.servicenow.com/dev.do#!/learn/courses/xanadu/app_store_learnv2_automatingapps_xanadu_automating_application_logic/app_store_learnv2_automatingapps_xanadu_notifications/app_store_learnv2_automatingapps_xanadu_outbound_email_configuration) in the Developer Site.


## Result

When the export is complete, you see either a download link or a message that the export will be delivered to the recipient.

**Parent Topic:**[Distribute reports](../concept/c_DistributeReports.md)

