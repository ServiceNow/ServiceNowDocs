---
title: Scheduled Script Execution form
description: The script to recalculate the scores of all indicators, the scoring profiles to which these indicators are attached, and the business applications that are associated to these scoring profiles.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enterprise Architecture \(formerly Application Portfolio Management\) reference, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Scheduled Script Execution form

The script to recalculate the scores of all indicators, the scoring profiles to which these indicators are attached, and the business applications that are associated to these scoring profiles.

## Scheduled script execution form fields

<table id="table_mpk_hqx_2wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify this scheduled script execution.

</td></tr><tr><td>

Active

</td><td>

Option to activate the script at the scheduled date and time. By default the job is inactive.

</td></tr><tr><td>

Run

</td><td>

The type of schedule to execute the script on. Choices are:-   Daily
-   Weekly
-   Monthly

</td></tr><tr><td>

Day

</td><td>

If you select Weekly or Monthly from the Run list, then the Day field appears. -   If Run is Weekly, then the day of the week.
-   If Run is Monthly, then the day of the month.

</td></tr><tr><td>

Time

</td><td>

Time at which the script runs on a 24-hour clock. If Run is Weekly or Monthly, the value includes the time of day.

</td></tr><tr><td>

Conditional

</td><td>

Option for executing only if certain conditions are met.

</td></tr><tr><td>

Run this script

</td><td>

The script to run at the scheduled date and time.You need not edit the script.

</td></tr><tr><td>

Run as

</td><td>

Select another user to run the script execution as. Configure the form to add this field if it is not present.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture \(formerly Application Portfolio Management\) reference](apm-reference.md)

**Related topics**  


[Schedule a job to compute application scores](../task/schedule-job-for-indicator-sourcing-score-cal.md)

