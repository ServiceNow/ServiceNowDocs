---
title: Import your badge reader data from an Excel spreadsheet
description: Import your badge reader data from an Excel spreadsheet into the Badge Access Register table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/contact-tracing/import-badge-register-data.html
release: zurich
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Collecting user badge data, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Import your badge reader data from an Excel spreadsheet

Import your badge reader data from an Excel spreadsheet into the Badge Access Register table.

## Before you begin

Ensure that you have added all your [user badge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contact-tracing/add-user-badge.md) and [badge reader](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contact-tracing/add-badge-reader.md) data.

Role required: sn\_imt\_tracing.badge\_manager

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Badge Management** &gt; **Badge Access Register**.

2.  Click **Import Badge Data**.

3.  In the Scheduled Data Imports list, open **Badge Access Register Scheduled Import**.

4.  Attach the Excel file and load data in the Import Set table.

    1.  Click the preview icon \(\[Omitted image "icon-preview.png"\] Alt text: Preview icon\) next to the **Data source** field, and then click **Open Record**.

    2.  On the Data Source form, click the manage attachments icon \(\[Omitted image "icon-paperclip.png"\] Alt text: Manage attachments icon\).

    3.  Click **Choose File** and select the source Excel file.

    4.  Click **Download All**.

        The Excel file is attached to the data source record.

    5.  Click the **Load All Records** related link to load the Excel data.

        The imported data is available in the new Import Set table, Badge Access Register Stage \[sn\_imt\_tracing\_badge\_access\_register\_stage\].

5.  Click **Execute Now**.

    The process runs in the background to load data from the Badge Access Register Stage table to the Badge Access Register table.

    **Note:** Depending on the number of records in the source Excel file, it might take a longer time for the imported data to be available in the Badge Access Register table.

6.  Verify that the data records were imported into the Badge Access Register table by navigating to **Contact Tracing** &gt; **Badge Management** &gt; **Badge Access Register**.


**Parent Topic:**[Collecting user badge data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contact-tracing/badge-management.md)

**Related topics**  


[Importing data using import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/system-import-sets/t_ScheduleADataImport.md)

[Schedule a data import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/system-import-sets/t_ScheduleADataImport.md)

