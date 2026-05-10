---
title: Special cases in job schedules
description: Some special cases require care in job scheduling.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Scheduled jobs, System scheduler, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Special cases in job schedules

Some special cases require care in job scheduling.

## End of the month schedules

Because months have different lengths, take care when scheduling jobs for the end of the month.

-   Scheduling an event for the 29th or 30th is not recommended, because the scheduled job is executed in months \(like February\) which are shorter than those dates.
-   If an event is scheduled for the 31st, it executes on the last day of the month, even if the month is shorter.

For example, something scheduled to run on the 31st of the month runs on February 28 or February 29 in a leap year.

## Weekday schedules

For scheduled scripts, use the following script to run only on weekdays:

**Warning:** Conditional scripts for scheduled report emails are executed in the sandbox. Therefore, function definitions are not allowed. Some API calls and keywords are also not allowed.

```

var isWeekday;
var today = new Date();
var dayOfWeek = today.getDay(); // Get day of the week(0 = Sunday, 1 = Monday, ... , 6 = Saturday)
switch (dayOfWeek) {
case 0: // Sunday
case 6: // Saturday
isWeekday = false;
break;
default:
isWeekday = true;
}
answer=isWeekday;
```

If the conditional script on a Scheduled Report is more complex and you need to make use of our Glide classes, then please use the following steps as a workaround:

1.  Create a Scheduled Job and complete all the conditional logic of the Scheduled Report inside the Scheduled Job.
2.  If all the conditional logic is satisfied, you can trigger the Scheduled Report with the following script inside the Scheduled Job.

    ```
    var schRpGr = new GlideRecord("sysauto_report");
    schRpGr.get("<sys_id of the scheduled report>");
    gs.executeNow(schRpGr);
    ```


## Scheduled jobs from scripts

To execute a scheduled job triggered by an event, use the following script:

```
//Execute a scheduled script job
var rec = new GlideRecord('sysauto_script');
rec.get('name', 'YOUR_JOB_NAME_HERE');
SncTriggerSynchronizer.executeNow(rec);
```

You can run the script using one of several tables:

-   scheduled\_import\_set \(Scheduled Import Sets\)
-   sysauto\_script \(Scheduled Script Execution\)
-   sysauto\_template \(Scheduled Template Generation\)
-   sysauto\_report \(Scheduled Report\)

**Note:** `SncTriggerSynchronizer` does not provide methods to execute scheduled jobs in the future.

## Running scheduled scripts and jobs imported from another instance

Scheduled Script Execution and Scheduled Jobs are categorized as data records in the ServiceNow AI Platform, which means they are excluded from update sets. To determine if a table is included, navigate to **All** &gt; **System Definition** &gt; **Dictionary** and view the **Attribute** value for the table in question. Only tables with the attribute update\_sync=true are included in update sets.

You can optionally export and import data records via XML. However, to prevent unexpected data changes, Schedule Item \[sys\_trigger\] records are not created for data records imported from an XML file such as an update set. To run scheduled jobs or scripts imported from another instance, update the corresponding job or script record in the target instance.

**Parent Topic:**[Scheduled jobs](../../reference-pages/concept/c_ScheduledJobs.md)

**Related topics**  


[Advanced options for scheduled jobs](../task/advanced-options-for-scheduled-jobs.md)

[Create a scheduled job](../task/t_CreateAScheduledJob.md)

[Enable run types for scheduled job child tables](../task/customize-run-times-for-scheduled-jobs.md#)

[Personalize the system date format](../task/t_PersonalizeTheSystemDateFormat.md)

[Set a system time zone](../task/t_SetASystemTimeZone.md)

[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

