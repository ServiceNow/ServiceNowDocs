---
title: Import Crisis Task data
description: As a crisis task administrator, upload a spreadsheet of self-reported health statuses to create crisis tasks in bulk.
locale: en-US
release: yokohama
product: Emergency Self Report
classification: emergency-self-report
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Emergency Self Report, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Import Crisis Task data

As a crisis task administrator, upload a spreadsheet of self-reported health statuses to create crisis tasks in bulk.

## Before you begin

You need a spreadsheet \(.csv or .xlsx file\) with data in the following columns: Person, User name, and Health Status. You can download a template from the Import Crisis Task Data data source record.

Role required: sn\_imt\_quarantine.humanResourceTeam

## About this task

The Bulk Import Crisis Task Data scheduled job is installed with the Emergency Self Report application. When you upload the spreadsheet, you can manually execute the job to import data into the Crisis Task table. HR tasks and their associated crisis tasks are created for each user based on their reported health status.

## Procedure

1.  Navigate to **All** &gt; **Emergency Self Report** &gt; **HR Tasks**.

2.  Click the **Import Crisis Task Data** button.

3.  In the Scheduled Data Imports list, open the **Bulk Import Crisis Task Data** scheduled data import job.

4.  In the **Data Source** field, open the **Import Crisis Task Data** record.

    1.  Click the attachments icon \(![Manage attachments icon.](../image/icon-manage-attachments.png)\).

    2.  Click **Choose file** and select the source Excel file.

    3.  Close the Attachments window.

5.  Click **Update**.

    The Scheduled Data Import record appears with the attachment.

6.  Click **Execute Now**.

    The process runs in the background to copy data from the Bulk Import Crisis Tasks table to the Crisis Task table.

    **Note:** The number of records in the source Excel file affect the time needed before the imported data is available in the Crisis Task table.


## Result

Records are imported to the Bulk Import Crisis Tasks table and copied to the Crisis Task table. New HR tasks are created with their associated crisis tasks. Records are not copied to the Crisis Task table in the following situations:

-   The user name is invalid or blank.
-   The health status is invalid or blank.
-   The user has an active case.
-   The user is a duplicate.

**Parent Topic:**[Emergency Self Report](../concept/emergency-self-report.md)

