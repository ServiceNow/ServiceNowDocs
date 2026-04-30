---
title: Pick a browser
description: If the test or test suite you are running contains steps that work with a form \(any step involving a UI\), or any other UI test step element \(such as Automated Service Catalog test steps\), work with the Pick a Browser dialog.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [UI test steps, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Pick a browser

If the test or test suite you are running contains steps that work with a form \(any step involving a UI\), or any other UI test step element \(such as Automated Service Catalog test steps\), work with the Pick a Browser dialog.

## Before you begin

You must have created the test you want to run.

The [test execution property](../reference/atf-admin-properties.md) must be enabled. You must have an admin or atf\_test\_admin role to do so.

**Note:** The test execution property is disabled by default to prevent running tests on a production system. Run tests only on development, test, and other sub-production instances.

Role required: atf\_test\_admin, atf\_test\_designer, or admin

## About this task

The Pick a Browser dialog appears after you click **Run Test** or **Run Test Suite**. The dialog asks you to choose among any currently-running test clients or start a new test runner.

## Procedure

1.  Choose the browser in which the test or test suite should run or be rerun again in the case of failed tests.

    All registered client test runners that are currently active appear in the Pick a Browser dialog. \(Current session\) indicates that the browser is currently running. See [Working with client test runners](../concept/atf-test-runners.md).

2.  Click **Manage your test runners here** as needed to view all client test runners registered for the current user.

    See [Active manual test runners](../reference/atf-active-manual-runners-module.md).

3.  If you want to open a client test runner in this browser session, click **Start a new test runner**, which appears when client test runners are only available in other browsers for the current user.

4.  Click the appropriate button to run the test.

    -   If you are running a single test, click **Run Test**.
    -   If you are running a test suite, click **Run Test Suite**.
    -   If you are running failed tests again, click **Re-run failed tests**.

## Result

The test, test suite or failed tests run in the selected browser or client test runner. The Progress viewer appears for monitoring of the progress of the test run.

-   **[Cloud Runner browser](../concept/atf-cloud-runner-browser.md)**  
If you are running a test or a test suite, select the Cloud Runner browser option to run your tests in a cloud browser.

**Parent Topic:**[UI test steps](../concept/ui-test-steps.md)

