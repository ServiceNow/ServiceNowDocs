---
title: Active manual test runners
description: View the client test runners table filtered to show only those runners available to run manually-started tests.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Run, Automated Test Framework reference, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Active manual test runners

View the client test runners table filtered to show only those runners available to run manually-started tests.

When you start a manual [client test runner](../concept/atf-test-runners.md), the system registers that runner in the Test Runners table as active.

The data in this table is transient. While the runner is active, it reports in to the system at a specified interval. If the runner does not report in at the expected time, the system marks the runner as inactive. After a period of time the system deletes the runner. You can [modify these intervals](../task/atf-modify-retention-test-clients.md) on the [Automated Test Framework properties](atf-admin-properties.md) page.

![Active Manual Test Runners](../image/atf-active-man-runners.png)

|Field / UI Element|Description|
|------------------|-----------|
|Type|Whether this test runner is for manual or scheduled tests. In the Active Manual Test Runners module, Type is always **Manual**.|
|User|The user logged into the browser session.|
|Browser name|The browser name.|
|Browser version|The browser version.|
|OS name|The name of the operating system running the browser.|
|OS version|The version of the operating system running the browser.|
|Status|Whether this runner is currently online or offline. In the Active Manual Test Runners module, Status is always **Online**.|
|Last checkin|The time/date this runner most recently reported in to the system.|
|Status reason|If the Status is Offline, the reason why. In the Active Manual Test Runners module, Status reason is always empty.|

**Parent Topic:**[Run](../concept/run-module.md)

