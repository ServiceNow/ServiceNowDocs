---
title: View job tracker details
description: View details of the source job and service job, such as when did the job begin and end, when did the records start loading into staging tables, or did the job run completely or fail in between.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Enterprise Service Management Integrations Framework, Enterprise Service Management Integrations Framework, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# View job tracker details

View details of the source job and service job, such as when did the job begin and end, when did the records start loading into staging tables, or did the job run completely or fail in between.

## Before you begin

Role required: sn\_hr\_integr\_fw.admin

## About this task

Once a scheduled flow is triggered or the **Run job** button on source module is clicked, records are created in the Integration Job Tracker and Integration Service Job Tracker tables.

## Procedure

1.  Navigate to **All** &gt; **Integrations Framework** &gt; **Job Tracker**.

2.  View the job details.

    |Field|Description|
    |-----|-----------|
    |Job name|Name of the job with application name appended.|
    |Job start time|Date and time when the source job has begun.|
    |Job end time|Date and time when the source job has ended.|
    |Error message|Message displayed when the job fails. If the source job fails, you must run the job again.|
    |Source|Name of the source for which the transformation job is run. For example, Cornerstone On Demand, or Pluralsight.|
    |State|Current state of the job such as failed, completed, or running.|

<table id="table_agn_wxj_1nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration service

</td><td>

Name of the integration service.

</td></tr><tr><td>

Sets

</td><td>

Lists of import sets.

</td></tr><tr><td>

Load started at

</td><td>

Option indicating the date and time when records started loading into staging table.

</td></tr><tr><td>

Load ended at

</td><td>

Option indicating the date and time when the records finished loading into staging table.

</td></tr><tr><td>

Last run date

</td><td>

Option indicating the last time and date when the service was pulled correctly.

</td></tr><tr><td>

Error message

</td><td>

Message displayed when the service job fails. If the service job fails, you must run the job again.

</td></tr><tr><td>

State

</td><td>

State of the service job such as loaded, running, or completed.

</td></tr><tr><td>

Transform started at

</td><td>

Option indicating the date and time when the transformation has begun, and records are moved from staging table to target table.

</td></tr><tr><td>

Transform ended at

</td><td>

Option indicating the date and time when the transformation has ended.

</td></tr><tr><td>

Flow Execution ID

</td><td>

Unique identifier of the flow that is executed for integration service.**Note:** The reporting feature is turned off for the flows \(used for large integrations\) that are created for Enterprise Service Management Integrations Framework.

</td></tr><tr><td>

Sync token

</td><td>

Stores token returned by APIs for certain integration services.

</td></tr></tbody>
</table>
