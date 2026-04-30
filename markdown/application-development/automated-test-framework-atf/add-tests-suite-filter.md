---
title: Add tests to a suite with a filter
description: Automate the creation of test suites by using a filter to dynamically add tests to a test suite when they match the filter conditions. Reduce the time that your test designers spend manually creating and maintaining test suites.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Building and running automated test suites, Test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Add tests to a suite with a filter

Automate the creation of test suites by using a filter to dynamically add tests to a test suite when they match the filter conditions. Reduce the time that your test designers spend manually creating and maintaining test suites.

## Before you begin

The tests you want to include in the test suite must exist.

Role required: atf\_test\_admin or atf\_test\_designer

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Suites**.

2.  Click **New**.

    The system displays the [Test Suite New Record](../reference/atf-test-suite-record.md) form.

3.  In the **Name** field, enter a name for this suite.

4.  For **Filter**, use the condition builder to specify the conditions a test must meet to be added to the test suite.

    **Note:** If you don't have a filter condition set, it is ignored and you can build the suite manually.

5.  Click **Save**.


## Result

All tests that match the filter conditions appear in the **Test Suite Tests** related list. Because the suite is dynamic, any new test that matches the conditions is automatically added to the suite.

**Parent Topic:**[Building and running automated test suites](../concept/atf-suites-overview.md)

