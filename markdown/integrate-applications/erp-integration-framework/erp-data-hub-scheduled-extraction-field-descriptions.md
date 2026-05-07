---
title: Zero Copy Connector for ERP scheduled extraction field descriptions
description: The Scheduled extraction form in Zero Copy Connector for ERP \(Enterprise Resource Planning\) enables you to create and edit jobs to extract data at regular intervals.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, schedule, extract, data, interval, pull]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP scheduled extraction field descriptions

The Scheduled extraction form in Zero Copy Connector for ERP \(Enterprise Resource Planning\) enables you to create and edit jobs to extract data at regular intervals.

For process details, see [Create a scheduled extraction in Zero Copy Connector for ERP](../task/erpc-create-a-scheduled-extraction.md).

<table id="table_rgs_xr5_bdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name that identifies this scheduled extraction.

</td></tr><tr><td>

Active

</td><td>

Option that indicates the scheduled extraction is active and should be executed at the specified frequency and time.

</td></tr><tr><td>

Extraction table

</td><td>

Name of the ERP extraction table from which to pull data.

</td></tr><tr><td>

ERP system

</td><td>

ERP system that the extraction table is linked to. The system must already be configured.

</td></tr><tr><td>

Application

</td><td>

This field is read only and is filled in automatically with Zero Copy Connector for ERP.

</td></tr><tr><td>

Maximum no of retries on error

</td><td>

If the job fails, set the maximum number of retries \(from 0 through 10\) the scheduled job should attempt before stopping.**Note:** Each retry uses the same query and retries the entire job. For example, if the total job contains 5000 records and the job fails after 2000 records are successfully processed, the entire job runs again on the next retry. For more information, see [Import sets key concepts](../../../administer/import-sets/concept/c_ImportSetsKeyConcepts.md).

</td></tr><tr><td>

Extraction will retry after

</td><td>

If the **Maximum no of retries on error** field is set to a number between 1-10, specify the amount of time \(in days, hours, minutes, and seconds\) the system should wait before attempting the extraction again.

</td></tr><tr><td>

Encoded query

</td><td>

Create an encoded query string using a filter on the extraction table list and paste the string into this field. For example:![Sample encoded query.](../image/erpc-schedule-extraction-encoded-query.png)

For more information, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Generate encoded query script

</td><td>

Generate an encoded query script to use on the extraction table to fetch the data. For example:![Sample generated encoded query script.](../image/erpc-schedule-extraction-generate-query.png)

The script entered in **Generate encoded query script** takes precedence over information entered into the **Encoded query** field. You can append the encoded query to the script \(as in the example\).

</td></tr><tr><td>

After extraction

</td><td>

Select an existing job that, when it completes, the new job you're creating should start. The job you specify must be active. **Note:** If you don't see the job that you want to use listed, check if the job is already scheduled before or after another job. Only jobs that won't create a loop are permitted.

</td></tr><tr><td>

Run as

</td><td>

Specify the user name to associate with the scheduled extraction.

</td></tr><tr><td>

Run

</td><td>

When to run the extraction.-   **Daily**: Specify the next scheduled start in hours, minutes, and seconds to repeat daily. For example, adding 20:30:00 starts the scheduled extraction the next time the clock reaches 20:30:00 \(9:30 pm\) and then every subsequent day at 20:30:00 in the time zone specified.
-   **Weekly**: In **Day**, select the day of the week to run the scheduled extraction. Specify the next scheduled start in hours, minutes, and seconds to repeat weekly. For example, selecting Sunday and specifying 03:00:00 starts the scheduled extraction the next Sunday at 3:00 am and then every subsequent week on Sunday at 3:00 am in the time zone specified.
-   **Monthly**: In **Day**, select the day of the month to run the scheduled extraction. Specify the next scheduled start in hours, minutes, and seconds to repeat monthly. For example, selecting 5 and specifying 03:00:00 starts the scheduled extraction the fifth day of the next month at 3:00 am and then every subsequent fifth of the month at 3:00 am in the time zone specified.
-   **Periodically**: In **Repeat Interval**, select the days, hours, minutes, and seconds to repeat periodically. For example, start the scheduled extraction every 3 days, 4 hours, 30 minutes, and 30 seconds.
-   **Once**: In **Starting**, click inside the field, select a day and type in a time for the extraction to run once.
-   **On Demand**: Select the **Run now** button \(next to the **Save** button\) to run the extraction immediately.
-   **Business Calendar:Entry Start**: Runs on the starting entry dates for the business calendar that you select in the Business Calendar field. A scheduled job runs for the starting date of each of the business entries that you defined for the business calendar. For example, if the business calendar represents a fiscal year, and the starting date of each entry is a fiscal month, the scheduled job runs on the first day of each month.
-   **Business Calendar:Entry End**: Runs for the ending date for the business calendar that you select in the **Business Calendar** field. This selection runs in the same manner as **Business Calendar:Entry Start**, but for the end dates of the associated business calendar entries.

**Note:** To learn more about creating and using business calendars and defining business calendar entries, see [Creating business calendars](https://www.servicenow.com/docs/access?context=business-calendars&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


</td></tr><tr><td>

Time

</td><td>

Time, in 24-hour format, for when the scheduled extraction should run.

</td></tr><tr><td>

Time zone

</td><td>

Specify the time zone for the scheduled extraction.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

