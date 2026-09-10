---
title: Zero Copy Connector for ERP scheduled extraction field descriptions
description: The Scheduled extraction form in Zero Copy Connector for ERP \(Enterprise Resource Planning\) enables you to create and edit jobs to extract data at regular intervals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-data-hub-scheduled-extraction-field-descriptions.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-08-06"
reading_time_minutes: 4
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, schedule, extract, data, interval, pull]
breadcrumb: [Field descriptions, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP scheduled extraction field descriptions

The Scheduled extraction form in Zero Copy Connector for ERP \(Enterprise Resource Planning\) enables you to create and edit jobs to extract data at regular intervals.

For process details, see [Create a scheduled extraction in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-create-a-scheduled-extraction.md).

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

Option that, when selected, runs the scheduled extraction at the specified frequency and time.

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

Application associated with the scheduled extraction. Filled in automatically with Zero Copy Connector for ERP.

</td></tr><tr><td>

Maximum no of retries on error

</td><td>

Maximum number of retries \(from 0 through 10\) that the scheduled job attempts before stopping after a failure.**Note:** Each retry uses the same query and retries the entire job. For example, if the total job contains 5000 records and the job fails after 2000 records are successfully processed, the entire job runs again on the next retry. For more information, see [Import sets key concepts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/c_ImportSetsKeyConcepts.md).

</td></tr><tr><td>

Extraction will retry after

</td><td>

Amount of time \(in days, hours, minutes, and seconds\) that the system waits before attempting the extraction again. Applies when the **Maximum no of retries on error** field is set to a number from 1 through 10.

</td></tr><tr><td>

Encoded query

</td><td>

Encoded query string, created by applying a filter on the extraction table list and pasting the result into this field. For example:\[Omitted image "erpc-schedule-extraction-encoded-query.png"\] Alt text: Sample encoded query.

For more information, see [Encoded query strings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_EncodedQueryStrings.md).

</td></tr><tr><td>

Generate encoded query script

</td><td>

Encoded query script that runs on the extraction table to fetch the data. For example:\[Omitted image "erpc-schedule-extraction-generate-query.png"\] Alt text: Sample generated encoded query script.

The script entered in **Generate encoded query script** takes precedence over information entered into the **Encoded query** field. You can append the encoded query to the script \(as in the example\).

</td></tr><tr><td>

After extraction

</td><td>

Existing active job that must complete before this scheduled extraction starts. **Note:** If you don't see the job that you want to use listed, check if the job is already scheduled before or after another job. Only jobs that won't create a loop are permitted.

</td></tr><tr><td>

Run as

</td><td>

 

</td></tr><tr><td>

Run

</td><td>

When to run the extraction.-   **Daily**: Specify the next scheduled start in hours, minutes, and seconds to repeat daily. For example, adding 20:30:00 starts the scheduled extraction the next time the clock reaches 20:30:00 \(9:30 p.m.\) and every subsequent day at 20:30:00 in the time zone specified.
-   **Weekly**: In **Day**, select the day of the week to run the scheduled extraction. Specify the next scheduled start in hours, minutes, and seconds to repeat weekly. For example, selecting Sunday and specifying 03:00:00 starts the scheduled extraction the next Sunday at 3:00 a.m. and then every subsequent week on Sunday at 3:00 a.m. in the time zone specified.
-   **Monthly**: In **Day**, select the day of the month to run the scheduled extraction. Specify the next scheduled start in hours, minutes, and seconds to repeat monthly. For example, selecting 5 and specifying 03:00:00 starts the scheduled extraction the fifth day of the next month at 3:00 a.m. and then every subsequent fifth of the month at 3:00 a.m. in the time zone specified.
-   **Periodically**: In **Repeat Interval**, select the days, hours, minutes, and seconds to repeat periodically. For example, start the scheduled extraction every 3 days, 4 hours, 30 minutes, and 30 seconds.
-   **Once**: In **Starting**, select the field, select a day, and enter a time for the extraction to run once.
-   **On Demand**: Select the **Run now** button \(next to the **Save** button\) to run the extraction immediately.
-   **Business Calendar:Entry Start**: Runs on the starting entry dates for the business calendar that you select in the Business Calendar field. A scheduled job runs for the starting date of each of the business entries that you defined for the business calendar. For example, if the business calendar represents a fiscal year, and the starting date of each entry is a fiscal month, the scheduled job runs on the first day of each month.
-   **Business Calendar:Entry End**: Runs for the ending date for the business calendar that you select in the **Business Calendar** field. This selection runs in the same manner as **Business Calendar:Entry Start**, but for the end dates of the associated business calendar entries.

**Note:** To learn more about creating and using business calendars and defining business calendar entries, see [Creating business calendars](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/business-calendars.md).


</td></tr><tr><td>

Time

</td><td>

Time, in 24-hour format, when the scheduled extraction runs.

</td></tr><tr><td>

Time zone

</td><td>

Time zone for the scheduled extraction.

</td></tr></tbody>
</table>