---
title: Active scheduled test runners
description: View the client test runners table filtered to show only those runners available to run tests to be started by a schedule.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Run, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Active scheduled test runners

View the client test runners table filtered to show only those runners available to run tests to be started by a schedule.

When you start a [scheduled client test runner,](../concept/atf-sched-suites.md#) the system registers that runner in the Active Scheduled Test Runners table.

The Active Scheduled Test Runner module is useful when you create a scheduled suite run. For scheduled suite runs, you can specify the browser to use. To determine the name and version of a browser you want to use, start a scheduled test runner with that browser, then inspect that runner's record in the Active Scheduled Test Runners module.

The data in this table is transient. While the runner is active, it reports in to the system at a specified interval. If the runner does not report in at the expected time, the system marks the runner as inactive. After a period of time the system deletes the runner.

You can [modify these intervals](../task/atf-modify-retention-test-clients.md) on the [Automated Test Framework properties](atf-admin-properties.md) page.

![Scheduled Client Test Runners](../image/atf-active-sched-runners.png "Example Scheduled Client Runner Test table")

|Field / UI Element|Description|
|------------------|-----------|
|Type|Whether this test runner is for manual or scheduled tests. In the Active Scheduled Test Runners module, Type is always **Scheduled**.|
|User|The user logged into the browser session.|
|Browser name|The browser name.|
|Browser version|The browser version.|
|OS name|The name of the operating system running the browser.|
|OS version|The version of the operating system running the browser.|
|Status|Whether this runner is currently online or offline. In the Active Manual Test Runners module, Status is always Online.|
|Last checkin|The time/date this runner most recently reported in to the system.|
|Status reason|If the Status is Offline, the reason why. In the Active Scheduled Test Runners module, Status reason is always empty.|

**Parent Topic:**[Run](../concept/run-module.md)

