---
title: Export a report to PDF
description: Export a report to PDF to use it outside of your ServiceNow instance.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Distribute reports, Core UI Reporting, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Export a report to PDF

Export a report to PDF to use it outside of your ServiceNow instance.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. The information in the exported report is only the information that you have the right to access.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run** and select the report you want to export.

    On instances with Unified Analytics enabled, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and follow the instructions in the topic [Export a data visualization from the Visualization Designer](../../par-for-workspace/task/export-visualization-vd.md).

2.  Select the **Sharing** icon \(![](../../../reuse/icons/product-icons/square-share-fill-24.svg)\) and choose **Export to PDF**.

    ![Export visualization to PDF menu](../image/export-vis-pdf.png)

    1.  Choose the orientation of the PDF, **Portrait** or **Landscape**.

    2.  Choose to generate the PDF or to send it in an email to one recipient.

3.  Choose the delivery method.

    Select **Generate now** to create the PDF and receive a download.

    Select **Send as an email**, to send the PDF to one recipient. To schedule delivery of an exported report to multiple addresses, see [Schedule emails of Core UI reports](t_ScheduleAReport.md#).

4.  Select **Export**.


## Result

When the export is complete, you see either a download link or a message that the export will be delivered to the recipient.

**Parent Topic:**[Distribute reports](../concept/c_DistributeReports.md)

