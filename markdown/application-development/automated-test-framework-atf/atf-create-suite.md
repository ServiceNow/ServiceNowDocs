---
title: Create an automated test suite
description: Group automated tests into a suite you can execute as a batch.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Building and running automated test suites, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Create an automated test suite

Group automated tests into a suite you can execute as a batch.

## Before you begin

The tests you want to include in the test suite must exist.

Role required: atf\_test\_admin or atf\_test\_designer

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Suites**.

2.  Click **New**.

    The system displays the [Test Suite New Record](../reference/atf-test-suite-record.md) form.

3.  In the **Name** field, enter a name for this suite.

4.  Select the tests to be included in this suite.

<table id="choicetable_tzr_ryh_5fb"><tbody><tr><td id="d310893e104">

**Filter**

</td><td>

Add tests dynamically using a filter:1.  In the **Filter** field, use the condition builder to create the conditions a test must match for inclusion in the test suite.
2.  Click **Save**.
 All tests that match the filter conditions appear in the **Test Suite Tests** related list. Because the suite is dynamic, any new test that matches the conditions is automatically added to the suite.

</td></tr><tr><td id="d310893e134">

**Test Suite Tests**

</td><td>

Add tests manually:

 1.  In the **Test Suite Tests** related list, click **Insert a new row...**.
2.  In the **Test** field, enter the name of the test to add to this test suite.


</td></tr></tbody>
</table>5.  In the **Description** field, enter a description for this test suite.

6.  In the **Test Suite Tests** related list, specify options for a test.

<table id="choicetable_hmg_313_5fb"><tbody><tr><td id="d310893e186">

**Execution order**

</td><td>

Enter a value to specify the order in which this test should execute within the test suite.

</td></tr><tr><td id="d310893e195">

**Abort on Failure**

</td><td>

Enter a value that indicates whether you want the test suite to stop or continue if this test fails. -   By default, the system assigns the value **false** to this field. If this test fails, the system still executes any further tests in the test suite.
-   Set the value to **true** to stop the test suite if this test fails.


</td></tr></tbody>
</table>7.  Repeat steps 4 - 6 for every test you want to include in this test suite.

8.  Click **Submit**.


**Parent Topic:**[Building and running automated test suites](../concept/atf-suites-overview.md)

