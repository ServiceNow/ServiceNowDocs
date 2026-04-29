---
title: Scheduled suite run record
description: A Scheduled Suite Run record associates a Suite Schedule record with a Test Suite.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Suite schedules, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Scheduled suite run record

A Scheduled Suite Run record associates a Suite Schedule record with a Test Suite.

|Field / Element|Description|
|---------------|-----------|
|Schedule|The schedule to use.|
|Test Suite|The test suite to run.|
|Application|The application scope for this scheduled suite run.|
|Watch list|Users the system notifies when this scheduled suite run completes.|
|Browser name|If the test suite has UI components, the browser that must be used. If no client test runner is available with this browser, the system does not run the suite.|
|Browser version starts with|If the test suite has UI components, the browser version for the client test runner must start with this string. If no client test runner is available with this browser version, the system does not run the suite.|
|OS name|If the test suite has UI components, the client test runner must run under this OS. If no client test runner is available with this OS, the system does not run the suite.|
|OS version starts with|If the test suite has UI components, the OS version for the client test runner must start with this string. If no client test runner is available with this OS version, the system does not run the suite.|
|Test Suite Results \(related list\)|All test suite results from this scheduled run.|

To determine the browser name and version of a browser you want to use, start a scheduled test runner with that browser, then inspect that runner's record in the [Active Scheduled Test Runners Module](atf-active-sched-runners-module.md).

**Parent Topic:**[Suite schedules](../concept/suite-schedules-module.md)

**Related topics**  


[Schedule an automated test suite](../task/atf-sched-suite-steps.md)

