---
title: Import your badge reader data from an Excel spreadsheet
description: Import your badge reader data from an Excel spreadsheet into the Badge Access Register table.
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Collecting user badge data, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Import your badge reader data from an Excel spreadsheet

Import your badge reader data from an Excel spreadsheet into the Badge Access Register table.

## Before you begin

Ensure that you have added all your [user badge](add-user-badge.md) and [badge reader](add-badge-reader.md) data.

Role required: sn\_imt\_tracing.badge\_manager

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Badge Management** &gt; **Badge Access Register**.

2.  Click **Import Badge Data**.

3.  In the Scheduled Data Imports list, open **Badge Access Register Scheduled Import**.

4.  Attach the Excel file and load data in the Import Set table.

    1.  Click the preview icon \(![Preview icon](../../safe-workplace-dashboard/image/icon-preview.png)\) next to the **Data source** field, and then click **Open Record**.

    2.  On the Data Source form, click the manage attachments icon \(![Manage attachments icon](../image/icon-paperclip.png)\).

    3.  Click **Choose File** and select the source Excel file.

    4.  Click **Download All**.

        The Excel file is attached to the data source record.

    5.  Click the **Load All Records** related link to load the Excel data.

        The imported data is available in the new Import Set table, Badge Access Register Stage \[sn\_imt\_tracing\_badge\_access\_register\_stage\].

5.  Click **Execute Now**.

    The process runs in the background to load data from the Badge Access Register Stage table to the Badge Access Register table.

    **Note:** Depending on the number of records in the source Excel file, it might take a longer time for the imported data to be available in the Badge Access Register table.

6.  Verify that the data records were imported into the Badge Access Register table by navigating to **Contact Tracing** &gt; **Badge Management** &gt; **Badge Access Register**.


**Parent Topic:**[Collecting user badge data](../concept/badge-management.md)

**Related topics**  


[bundle-crint.t_ScheduleADataImport]

[bundle-crint.t_ScheduleADataImport]

