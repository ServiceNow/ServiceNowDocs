---
title: Modify the scheduled data import job
description: As an administrator, review and modify the scheduled data import jobs used for importing badge access and Wi-Fi access data from an Excel file into the Contact Tracing application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/contact-tracing/configure-badge-sched-import-job.html
release: zurich
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Modify the scheduled data import job

As an administrator, review and modify the scheduled data import jobs used for importing badge access and Wi-Fi access data from an Excel file into the Contact Tracing application.

## Before you begin

Role required: admin

## About this task

The following scheduled jobs are installed with the Contact Tracing application:

-   **Badge Access Register Scheduled Import**
-   **Wi-Fi Access Register Scheduled Import**

These jobs are set for manual execution to import the [badge access data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contact-tracing/import-badge-register-data.md) or [Wi-Fi access data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contact-tracing/import-wifi-data.md) from an Excel file. You can modify the settings based on when and how you want to import the data.

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Administration** &gt; **Data Import Jobs**.

2.  Open a Scheduled Import record.

3.  Review and modify the settings as required.

    For more information on configuring a scheduled data import, see [Schedule a data import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/system-import-sets/t_ScheduleADataImport.md).

4.  Click **Update**.


**Parent Topic:**[Setting up Contact Tracing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contact-tracing/set-up-contact-tracing.md)

**Related topics**  


[Importing data using import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/system-import-sets/t_ScheduleADataImport.md)

