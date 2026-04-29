---
title: Re-run failed tests in an automated test suite
description: Re-run failed tests within a test suite without rerunning the entire suite.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Building and running automated test suites, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Re-run failed tests in an automated test suite

Re-run failed tests within a test suite without rerunning the entire suite.

## Before you begin

Role required: atf\_test\_admin, atf\_test\_designer, or admin

## About this task

The **Re-run failed tests** button appears on the Suite Result form and on the Suite Execution Progress Viewer after a suite with failed tests completes. It does not appear if test execution is disabled, the suite is deactivated, the suite passed, or the user does not have one of the required roles.

The **Re-run failed tests** button re-runs all non-passing tests, which includes tests with the following status: canceled, skipped, failure, and error. It does not include the test results with a Success with warning\(s\) status.

## Procedure

1.  Navigate to either the suite result form or suite execution progress viewer for the completed suite that had failed tests.

2.  Click **Re-run failed tests**.

    If the re-run tests include a form step \(any step involving a UI\) or other kinds of [UI test steps](../concept/ui-test-steps.md), the [Pick a Browser](atf-pick-a-browser.md) dialog appears before executing the tests.

3.  In the dialog box, choose among any currently running test clients or start a new runner.

    If the re-run tests include only server test steps, the system executes the tests without displaying the Pick a Browser dialog. For more information, review [Browser recommendations for all tests and suites](../concept/atf-test-runners.md#kvv_h25_gx) and [Server test steps](../concept/server-test-steps.md).


## Result

The system re-runs the failed tests.

-   The system creates a new suite result hierarchy for the re-run tests. The Progress Workers, Test Result, and Test Suite Result forms show the same suite hierarchy as the previous test suite. They do not include the tests or suites that passed in a previous run.
-   If you delete or deactivate a child suite or test that failed, and then re-run it, the system does not execute that suite or test in the re-run.
-   If you add a child suite or test to the suite to a failed test, and then re-run it, the system does not execute the added suite or test in the re-run.

## What to do next

To view the results from the previous run of a test or suite, click **Previous test result** on the [test result form](../reference/atf-test-results-record.md) or **Previous suite result** on the test [suite result form](../reference/atf-test-suite-results-record.md). These fields only appear for tests and suites that have been re-run.

**Parent Topic:**[Building and running automated test suites](../concept/atf-suites-overview.md)

