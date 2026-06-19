---
title: Import your Wi-Fi access logs spreadsheet
description: Import Wi-Fi access logs from an Excel spreadsheet into the Wi-Fi Access Register table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contact-tracing/import-wifi-data.html
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Retrieving Wi-Fi access log data, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Import your Wi-Fi access logs spreadsheet

Import Wi-Fi access logs from an Excel spreadsheet into the Wi-Fi Access Register table.

## Before you begin

Role required: sn\_imt\_tracing.wifi\_manager

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Wi-Fi Access Management** &gt; **Wi-Fi Access Register**.

2.  Click **Import Wi-Fi Access Data**.

3.  In the Scheduled Data Imports list, open **Wi-Fi Access Register Scheduled Import**.

4.  In the **Data Source** field, open the **Wi-Fi Access Register Data Source** record.

    1.  Click the manage attachments icon \(\[Omitted image "icon-paperclip.png"\] Alt text: Manage attachments icon\).
    2.  Click **Choose File** and select the source Excel file.
    3.  Click the **Load All Records** related link to load the Excel data.
5.  Navigate to Scheduled Import record.

6.  Click **Execute Now**.

    The process runs in the background to load data from the Wi-Fi Access Register Stage table to the Wi-Fi Access Register table.

    **Note:** The number of records in the source Excel file affect the time needed before the imported data is available in the Wi-Fi Access Register table.

7.  Verify that the data records were imported into the Wi-Fi Access Register table by navigating to **Contact Tracing** &gt; **Wi-Fi Access Management** &gt; **Wi-Fi Access Register**.


**Parent Topic:**[Retrieving Wi-Fi access log data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contact-tracing/wifi-access-management.md)

