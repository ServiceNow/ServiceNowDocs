---
title: Suite schedule record
description: The Suite Results record displays information about one test suite schedule.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Suite schedules, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Suite schedule record

The Suite Results record displays information about one test suite schedule.

|Field / Element|Description|
|---------------|-----------|
|Name|A name for this test suite schedule.|
|Description|A description for this test suite schedule.|
|Active|If this schedule is active **true**. Otherwise, **false**.|
|Application|The application scope for this test suite schedule.|
|Run|The frequency with which the system runs test suites belonging to this schedule.|
|Run as tz|The timezone used for the **Time** field.|
|Time|The time of day at which the system runs test suites belonging to this schedule.|
|Day|If **Run** is set to Weekly, the day of the week on which the system runs test suites belonging to this schedule. If **Run** is set to monthly, the day of the month.|
|Repeat interval|If Run is set to **Periodically,**the number of days and hours that constitute the repeat interval for running suites in this schedule.|
|Conditional|Check to enable a script to define conditions under which the system should run the test suites in this schedule.|
|Condition|If **Conditional** is checked, the script to execute for determining the conditions under which the system should run the test suites in this schedule.|
|Scheduled Suite Runs \(related list\)|The test suites the system should run on this schedule.|

**Parent Topic:**[Suite schedules](../concept/suite-schedules-module.md)

**Related topics**  


[Schedule an automated test suite](../task/atf-sched-suite-steps.md)

