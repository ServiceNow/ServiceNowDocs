---
title: Add test to an existing automated test suite
description: Add a test to a test suite that already exists.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Building and running automated test suites, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Add test to an existing automated test suite

Add a test to a test suite that already exists.

## Before you begin

The tests you want to include and the test suite must exist.

Role required: atf\_test\_admin or atf\_test\_designer

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Suites**.

2.  Click the row containing the test suite you want.

    The system displays the [Test Suite](../reference/atf-test-suite-record.md) form.

3.  In the **Test Suite Tests** related list, click **Insert a new row...**.

4.  In the **Test** field, enter the name of the test to add to this test suite.

5.  In the **Order** field for this row, enter a value to determine the order in which this test should execute within the test suite.

    By default, the system assigns a value to this field according to the order in which you add the tests.

6.  In the **Abort on Failure** field for this row, enter a value that indicates whether you want the test suite to stop or continue if this individual test fails.

    By default, the system assigns the value **false** to this field. **False** means that if this test fails, the system still executes any further tests in the test suite.

7.  Repeat steps 3 - 6 for every test you want to include in this test suite.

8.  Click **Submit**.


**Parent Topic:**[Building and running automated test suites](../concept/atf-suites-overview.md)

