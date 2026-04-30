---
title: View job tracker details from Workday
description: Track every pull that has been performed from ServiceNow to Workday either by schedule job or manual reconciliation process. View details of the job, such as when did the job begin and end, when did the records start loading into staging tables, or did the job run completely or fail in between.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using HR Service Delivery Integration with Workday, HR Service Delivery Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# View job tracker details from Workday

Track every pull that has been performed from ServiceNow to Workday either by schedule job or manual reconciliation process. View details of the job, such as when did the job begin and end, when did the records start loading into staging tables, or did the job run completely or fail in between.

## Before you begin

Role required: sn\_hr\_workday.admin

## Procedure

1.  Navigate to **All** &gt; **Workday Worker Profile Sync** &gt; **Job Tracker** &gt; **Workday Integration Job Tracker**.

2.  View job details.

    |Field|Description|
    |-----|-----------|
    |Job name|Name of the job that has run.|
    |Job started at|Date and time when the job started.|
    |Job ended at|Date and time when the job ended.|
    |State|Current state of the job, such as **Complete** and **Failed**.|
    |Error message|Message displayed when the job has failed.|

3.  Select a job record.

    In the **Workday Integration Service Job Trackers** related list, view the service job details.

    |Field|Description|
    |-----|-----------|
    |Number|Unique identifier for the service job run.|
    |Workday Integration Service|Name of the service job that has run. For example, Worker Profiles integration service.|
    |Job state|Current state of the service job. For example, Completed or Failed.|
    |Job started at|Date and time when the service job run started.|
    |Job ended at|Date and time when the service job run ended.|
    |Error Source|Phase during which the error has occurred: API Error, Transformation Error, or Configuration Error.|
    |Error Message|Message displayed when the job has failed.|
    |Start Date Time-API Parameter|Date after which the modified records are pulled from Workday into ServiceNow.|
    |End Date Time-API Parameter|Date until which the modified records are pulled from Workday into ServiceNow.|
    |Import Set|Name of the import set that is pulled.|


**Parent Topic:**[Using HR Service Delivery Integration with Workday](../concept/config-hrsd-int-workday.md)

**Related topics**  


[Use transform maps](../reference/transform-maps-w.md)

[View tasks from Workday](view-to-dos-wd.md)

