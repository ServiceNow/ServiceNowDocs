---
title: Manage status and retention policies for automated test client runners
description: Modify how often active client test runners report in to the system and how long the system retains records for inactive client test runners.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administering the Automated Test Framework \(ATF\), Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Manage status and retention policies for automated test client runners

Modify how often active client test runners report in to the system and how long the system retains records for inactive client test runners.

## Before you begin

Role required: atf\_test\_admin

## About this task

When you start a [client test runner](../concept/atf-test-runners.md), the system registers that runner as active, meaning that it is either running a test or is available to run a test. While the runner is active, it reports in to the system at a specified interval. If the runner does not report in at the expected time, the system marks the runner as inactive. After a period of time the system deletes the runner. This task enables you to modify the [Automated Test Framework properties](../reference/atf-admin-properties.md) that control these intervals.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Administration** &gt; **Properties**.

2.  Navigate to the Test Runner Properties section.

3.  To set the interval at which active client test runners report in to the system, enter the reporting interval in seconds in the **Test runner heartbeat interval** field.

4.  To set the period of time a test runner can remain inactive before the system deletes it, enter the period of time in seconds in the **Test runner timeout** field.

5.  Click **Save**.


**Parent Topic:**[Administering the Automated Test Framework \(ATF\)](../concept/atf-admin-overview.md)

**Related topics**  


[Working with client test runners](../concept/atf-test-runners.md)

[Active manual test runners](../reference/atf-active-manual-runners-module.md)

[Active scheduled test runners](../reference/atf-active-sched-runners-module.md)

