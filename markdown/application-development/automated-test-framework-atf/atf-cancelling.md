---
title: Cancelling automated tests and test suites
description: You can cancel automated tests and automated test suites that are running or are queued to run.You can cancel an automated test suite that is queued but has not yet run.Cancel running and pending tests in a running suite test.You can cancel a running test from the Run Test progress dialog.You can cancel a waiting automated test from the Waiting/Running Test Runs module.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Cancelling automated tests and test suites

You can cancel automated tests and automated test suites that are running or are queued to run.

How you cancel an automated test or automated test suite depends on whether the test or test suite is currently running or is queued to run.

**Parent Topic:**[Automated Test Framework \(ATF\) test building and execution](atf-test-build-execution.md)

**Related topics**  


[Building and running automated tests with the Automated Test Framework](atf-build-overview.md)

[Building and running automated test suites](atf-suites-overview.md)

[Auto-generate ATF tests](../task/atf-auto-generate-tests.md)

## Cancel queued automated test suite

You can cancel an automated test suite that is queued but has not yet run.

### Before you begin

Role required: atf\_test\_admin or atf\_test\_designer

### Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Run** &gt; **Waiting/Running Test Runs**.

2.  Select the action check boxes for the test suites to cancel.

3.  From the action choice list, select **Delete**.


## Cancel running and pending tests in an automated test suite

Cancel running and pending tests in a running suite test.

### Before you begin

Role required: atf\_test\_admin or atf\_test\_designer

### Procedure

1.  If necessary, [display the Run Test progress dialog](../task/atf-view-progress.md).

2.  Click **Cancel Pending Steps**.

    The system displays a dialog asking you to confirm that you want to cancel this test execution.

3.  In the Confirmation dialog, click **Yes**.


### Result

The system cancels any running and pending tests in this test suite and rolls back any data that tests in the test suite may have changed.

## Cancel running automated test

You can cancel a running test from the Run Test progress dialog.

### Before you begin

The system must be running a test.

Role required: atf\_test\_admin or atf\_test\_designer

### Procedure

1.  If necessary, [display the Run Test progress dialog](../task/atf-view-progress.md).

2.  Click **Cancel Pending Steps**.

    The system displays a dialog asking you to confirm that you want to cancel this test execution.

3.  In the Confirmation dialog, click **Yes**.


### Result

The system cancels the running test and rolls back any data changes the test made.

## Cancel waiting automated test

You can cancel a waiting automated test from the Waiting/Running Test Runs module.

### Before you begin

Role required: atf\_test\_admin or atf\_test\_designer

### Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Run** &gt; **Waiting/Running Test Runs**.

2.  Select the action check boxes for the tests to cancel.

3.  From the action choice list, select **Delete**.


