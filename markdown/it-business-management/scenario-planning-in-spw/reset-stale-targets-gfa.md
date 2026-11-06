---
title: Reset the check-in frequency of stale targets
description: Clear the check-in frequency of stale targets in a date range after a goal calendar change, so that the owners can select a frequency again.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/scenario-planning-in-spw/reset-stale-targets-gfa.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 2
audience: admin
breadcrumb: [Managing stale targets, Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Reset the check-in frequency of stale targets

Clear the check-in frequency of stale targets in a date range after a goal calendar change, so that the owners can select a frequency again.

## Before you begin

Role required: sn\_gf.goal\_admin

## About this task

Run this task after you change the goal calendar. Only targets with breakdowns can become stale. A target becomes stale when its stored breakdowns no longer match the goal calendar that is set in the **sn\_gfa.calendar\_type** system property. Targets without breakdowns don't become stale when the goal calendar changes. A stale target can't be changed until its check-in frequency is cleared.

**Note:** Clearing the check-in frequency deletes all existing breakdowns of the target. However, the total actuals are retained.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for and open the **Goal calendar alignment - Reset check-in frequency for stale targets** scheduled job.

    The record runs on demand. It doesn't run on a schedule.

3.  In the **Run this script**, set the required details.

    1.  Set `startDate` and `endDate` in the format YYYY-MM-DD.

        The job processes only the targets whose start date is on or after `startDate` and whose end date is on or before `endDate`.

        ```
        var startDate = '2026-01-01';
        var endDate = '2026-12-31';
        ```

    2.  Set `extraQuery` to narrow the targets further.

        Enter an encoded query to limit the targets by target type, goal, or other criteria. The query applies together with the date range. Leave the value empty to process every target in the date range.

        ```
        var extraQuery = '';
        ```

4.  Select **Execute Now**.

    Invalid dates, or unknown fields in the encoded query, stop the job before it checks any target. The job writes an error to the system log.

5.  Review the summary message in the system log.

    The job writes one summary line at the end of the run. A line with the info level means all stale targets in the range were reset. A line with the warning level lists up to 20 failed target numbers and the reason for each failure.

    ```
    CheckInFrequencyReset: finished in 2.4 s. Checked 120 Targets, reset 118, failed 2. Failed: TGT0012345 (rejected by business rule "...")
    ```

6.  For each failed target, fix the cause named in the log message, then run the job again for that target.

    The log message names the business rule that rejected the update. The job doesn't print field values.


## Result

Each reset target has an empty check-in frequency. Its owner must select a frequency again, which rebuilds its breakdowns to match the goal calendar. Until then, the target stays locked for value and structure changes. Instead of running this task, a goal owner or target owner can duplicate the stale target and set a check-in frequency on the copy. The copy doesn't include the remarks, work notes, or history of the stale target.

**Parent Topic:**[Managing stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/managing-stale-targets.md)

**Related topics**  


[Stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/stale-targets.md)

