---
title: Working with client test runners
description: If an automated test includes steps that involve a form or any other user-interface \(UI\) element, it runs those steps in a browser tab or window called a test runner or client test runner.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 5
breadcrumb: [UI test steps, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Working with client test runners

If an automated test includes steps that involve a form or any other user-interface \(UI\) element, it runs those steps in a browser tab or window called a test runner or client test runner.

The Automated Test Framework supports two types of client test runners: Client Test Runners for manually started tests and Scheduled Client Test Runners for tests started by a schedule.

When test execution is enabled, clicking the Client Test Runner module opens the client test runner in the current browser session. If tests are waiting to be run, the Client Test Runner runs a waiting test. If no test is running, the message Waiting for a test to run displays in the client test runner.

While the client test runner is idle, it checks every five seconds for waiting tests to start. This ensures that the system runs any tests it may have been unable to start because no client with the proper configuration was available.

**Note:** The client test runner monitors for tests from the current session and runs those tests as the logged-in user \(unless it executes an Impersonate User step\). If you start a client test runner, log out from the current session, and then log in again, the client test runner executes using the new session.

When the client runner is active, it displays the activity of the currently running test in the **Execution Frame**.

**Note:** You are now allowed to execute multiple tests at a given time.

## Test execution property

To work with the client test runner module, the [test execution property](../reference/atf-admin-properties.md) must be enabled.

**Note:** By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances.

If the test execution property is disabled when you select this module, the system displays a message and a link to the [automated test framework properties page](../reference/atf-admin-properties.md) where you can enable it.

## Additional debugging functionality

If you have enabled [additional debugging functionality](../reference/atf-admin-properties.md), the client test runner module displays two tabs: **Execution Frame** and **Debug Info**. The **Execution Frame** displays the information normally shown by the client test runner and the **Debug Info** displays additional debugging information.

The system takes screen shots from the tests in the **Execution Frame** tab and records them to the test result record.

## Browser recommendations for all tests and suites

-   Some browsers have memory-management limitations that make it necessary to occasionally close and restart the browser when running the client test runner. These browsers include Internet Explorer, Edge, and older versions of Firefox. How often you should close the browser depends on the memory allocation in the browser application.
-   Some browsers have features that throttle CPU time. To avoid problems, follow these guidelines:
    -   Run the client test runner in its own browser window.
    -   Keep the client test runner at least partially visible on the screen.
    -   Make certain the screen is not locked or shut off.
-   The client test runner takes screen shots as the tests run. For best results with screen shots, leave the browser zoom level set to 100%.

## Browser recommendations for scheduled suites

The client test runners for scheduled suites have additional browser requirements.

-   On OS X with the client test runner on Chrome or Safari: If the screen is locked or the client test runner tab is not shown, when the system attempts to run the test suite, tests run significantly slower and may time out. For best performance, run client test runners for scheduled suites in a virtual machine \(VM\) environment in which the screen does not become locked or disabled.
-   The browser must meet the criteria you specified on the [Scheduled suite run record](../reference/atf-suite-sched-run-record.md).
-   A client test runner meeting the criteria you specified on the [Scheduled suite run record](../reference/atf-suite-sched-run-record.md) must be available to run the test suite at the scheduled time. The system cannot automatically open a client test-runner session.

## Javascript window command intercepts

The Client Test Runner captures window object commands including console.log, console.error, alert, confirm, and prompt, with default responses where necessary.

-   Any script that calls **window.confirm** receives a boolean response of **true**.
-   Any script that calls **window.prompt** receives the string response **test value**.
-   Any script call to **alert** is ignored.

## Active Test Runners table

When you start a client test runner, the system registers that runner in the Active Test Runners table. You can view this table in the [Active Manual Test Runners](../reference/atf-active-manual-runners-module.md) module and the [Active Scheduled Test Runners](../reference/atf-active-sched-runners-module.md) module. These two modules provide views of the same table, filtered to show only manual or only scheduled test runners.

The Active Scheduled Test Runner module is useful when you create a scheduled suite run. For scheduled suite runs, you can specify the browser to use. To determine the name and version of a browser you want to use, start a scheduled test runner with that browser, then inspect that runner's record in the Active Scheduled Test Runners module.

The data in this table is transient. While the runner is active, it reports in to the system at a specified interval. If the runner does not report in at the expected time, the system marks the runner as inactive. After a period of time the system deletes the runner. You can [modify these intervals](../task/atf-modify-retention-test-clients.md) on the [Automated Test Framework properties](../reference/atf-admin-properties.md) page.

**Parent Topic:**[UI test steps](ui-test-steps.md)

**Related topics**  


[Client test runner](../reference/atf-client-test-runner-module.md)

[Scheduled client test runner](../reference/atf-sched-test-runner-module.md)

[Allowed client errors](whitelisted-client-errors.md)

