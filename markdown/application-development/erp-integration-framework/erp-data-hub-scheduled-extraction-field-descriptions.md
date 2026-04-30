---
title: ERP Data Hub scheduled extraction field descriptions
description: The Scheduled extraction form in ERP Data Hub enables you to create and edit jobs to extract data at regular intervals.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2024-10-17"
reading_time_minutes: 2
breadcrumb: [ERP Data Hub field descriptions, ERP Data Hub reference, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# ERP Data Hub scheduled extraction field descriptions

The Scheduled extraction form in ERP Data Hub enables you to create and edit jobs to extract data at regular intervals.

<table id="table_rgs_xr5_bdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name that identifies this scheduled extraction.

</td></tr><tr><td>

ERP system

</td><td>

ERP system that the extraction table is linked to. The system must already be configured.

</td></tr><tr><td>

Extraction table

</td><td>

Name of the ERP extraction table from which to pull data.

</td></tr><tr><td>

Frequency

</td><td>

When to run the extraction.-   Hourly: Specify the next scheduled start in hours, minutes, and seconds to repeat hourly. For example, adding 20:30:00 starts the scheduled extraction the next time the clock reaches 20:30:00 \(9:30 pm\) and then hourly after that \(21:30:00, 22:30:00, 23:30:00, and so on\).
-   Daily: Specify the next scheduled start in hours, minutes, and seconds to repeat daily. For example, adding 20:30:00 starts the scheduled extraction the next time the clock reaches 20:30:00 \(9:30 pm\) and then every subsequent day at 20:30:00.
-   Weekly: In **Weekday**, select the day of the week to run the scheduled extraction. Specify the next scheduled start in hours, minutes, and seconds to repeat weekly. For example, selecting Sunday and specifying 03:00:00 starts the scheduled extraction the next Sunday at 3:00 am and then every subsequent week on Sunday at 3:00 am.
-   After Completed Job: In **After job**, select an existing job that, when it completes, the new job you're creating should start. The job you specify must be active.

**Note:** If you don't see the job that you want to use listed in **After job**, check if the job is already scheduled before or after another job. Only jobs that won't create a loop are permitted.


</td></tr><tr><td>

Next scheduled start

</td><td>

Time, in 24-hour format, for when the scheduled extraction should run.

</td></tr><tr><td>

Active

</td><td>

Option that indicates the scheduled extraction is active and should be executed at the specified frequency and time.

</td></tr><tr><td>

Maximum no of retries on error

</td><td>

If the job fails, set the maximum number of retries \(from 0 through 10\) the scheduled job should attempt before stopping.**Note:** Each retry uses the same query and retries the entire job. For example, if the total job contains 5000 records and the job fails after 2000 records are successfully processed, the entire job is rerun again on the next retry. For more information, see [Import sets key concepts](https://www.servicenow.com/docs/access?context=c_ImportSetsKeyConcepts&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

</td></tr><tr><td>

Extraction will retry after

</td><td>

If the **Maximum no of retries on error** field is set to a number between 1-10, specify the amount of time \(in days, hours, minutes, and seconds\) the system should wait before attempting the extraction again.

</td></tr><tr><td>

Generate encoded query script

</td><td>

Generate an encoded query script to use on the extraction table to fetch the data. For example:![Sample generated encoded query script.](../image/erpc-schedule-extraction-generate-query.png)

The script entered in **Generate encoded query script** takes precedence over information entered into the **Encoded query** field. You can append the encoded query to the script \(as in the example\).

</td></tr><tr><td>

Encoded query

</td><td>

Create an encoded query string using a filter on the extraction table list and paste the string into this field. For example:![Sample encoded query.](../image/erpc-schedule-extraction-encoded-query.png)

For more information, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[ERP Data Hub field descriptions](erp-canvas-field-descriptions.md)

