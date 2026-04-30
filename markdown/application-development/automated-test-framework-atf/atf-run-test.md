---
title: Run an automated test
description: After creating an automated test, run it on a non-production instance.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Building and running automated tests with the Automated Test Framework, Test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Run an automated test

After creating an automated test, run it on a non-production instance.

## Before you begin

You must have created the test you want to run.

The [test execution property](../reference/atf-admin-properties.md) must be enabled. You must have an admin or atf\_test\_admin role to do so.

**Note:** The test execution property is disabled by default to prevent running tests on a production system. Run tests only on development, test, and other sub-production instances.

Role required: atf\_test\_admin, atf\_test\_designer, or admin

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  If necessary to view the tests list, click **Tests**.

3.  Click the row containing the test that you want to run.

    The system displays the **Test** form.

4.  Click **Run Test**.

    **Note:** If the test execution property is not enabled, the **Run Test** button does not appear. In this case, see the annotation at the top of the form, and click the link to enable running tests.

    If the test includes a form step \(any step involving a UI\), or other kinds of [UI test steps](../concept/ui-test-steps.md), the [Pick a browser](atf-pick-a-browser.md) dialog appears before executing the tests. Use it to choose among any currently running test clients, or start a new runner. For more information, review [Browser recommendations for all tests and suites](../concept/atf-test-runners.md#kvv_h25_gx). If the test only includes [server test steps](../concept/server-test-steps.md), the system executes the tests without displaying the Pick a Browser dialog.


## What to do next

Monitor the progress of the test in the Run Test progress dialog. When complete, click **Go to Results** \(on the Run Test progress dialog\) to display the **Test Results** list, where you can [view and analyze test results.](atf-view-results-consolidated.md)

**Note:** If your test creates data, the system rolls back that data after all steps in the test complete.

**Parent Topic:**[Building and running automated tests with the Automated Test Framework](../concept/atf-build-overview.md)

**Related topics**  


[Cancelling automated tests and test suites](../concept/atf-cancelling.md#)

