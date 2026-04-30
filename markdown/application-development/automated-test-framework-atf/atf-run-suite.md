---
title: Run an automated test suite
description: After creating an automated test suite, run it in a non-production instance.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Building and running automated test suites, Test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Run an automated test suite

After creating an automated test suite, run it in a non-production instance.

## Before you begin

You must have created the test suite you want to run.

The [test execution property](../reference/atf-admin-properties.md) must be enabled. You must have an admin or atf\_test\_admin role to do so.

**Note:** The test execution property is disabled by default to prevent running tests on a production system. Run tests only on development, test, and other sub-production instances.

Role required: atf\_test\_admin, atf\_test\_designer, or admin

## About this task

This procedure outlines how to start a test suite manually. You can also schedule test suites to run at a later time. For more information, see [Working with scheduled test suites](../concept/atf-sched-suites.md#).

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Suites**.

2.  If necessary to view the Test Suites list, click **Test Suites**.

3.  Click the row containing the test suite you want to run.

    The system displays the [Test Suite](../reference/atf-test-suite-record.md) form.

4.  Click **Run Test Suite**.

    **Note:** If the test execution property is not enabled, the **Run Suite** button does not appear. In this case, see the annotation at the top of the form, and click the link to enable running tests.

    If the tests associated with the test suite include a form step \(any step involving a UI\), or other kinds of [UI test steps](../concept/ui-test-steps.md), the [Pick a Browser](atf-pick-a-browser.md) dialog appears before executing the tests.

5.  Choose among any currently running test clients, or start a new runner.

    For more information, review [Browser recommendations for all tests and suites](../concept/atf-test-runners.md#kvv_h25_gx).

    If the tests associated with the test suite only include [server test steps](../concept/server-test-steps.md), the system executes the tests without displaying the Pick a Browser dialog.


## What to do next

Monitor the progress of the tests. When complete, click **Go to results** on the progress dialog window to display the **Test Results** list, where you can [view](atf-view-results-consolidated.md) and analyze the results.

**Parent Topic:**[Building and running automated test suites](../concept/atf-suites-overview.md)

