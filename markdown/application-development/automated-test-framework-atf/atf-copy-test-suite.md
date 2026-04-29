---
title: Copy an automated test suite
description: Reduce time when creating tests by copying an entire test suite. Rename and modify the test suite after copying. The Copy Test Suite button on the Test Suite form copies all the nested tests and child test suites within the text suite.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Building and running automated test suites, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Copy an automated test suite

Reduce time when creating tests by copying an entire test suite. Rename and modify the test suite after copying. The **Copy Test Suite** button on the Test Suite form copies all the nested tests and child test suites within the text suite.

## Before you begin

Role required: atf\_test\_admin or atf\_test\_designer

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Suites**.

2.  Select the row containing the test suite that you want to copy.

3.  Near the top corner of the Test Suite form, select **Copy Test Suite**.

    A progress tracker appears to confirm the status. If you select **Go to Copy**, the system displays a new test suite record identical to the copied record, except for the **Name**.

    **Note:** If you apply filter conditions, copied tests are added to the test suite if the conditions are met.

    If any tests or child test suites fail to copy, they are skipped and copying of the remaining tests and child test suites continues. A warning message showing a partial success appears below the progress bar.

    **Note:** You can copy a test suite only when it's in the same scope as the current scope. The **Copy Test Suite** button appears only when the test suite is in the same scope. The scopes of the tests in a suite are preserved when copying a test suite. See [Application Scope](../../../build/applications/concept/c_ApplicationScope.md) for more information.

    ![Progress tracker showing partial success.](../image/atf-partial-copy-test-suites.png)

    If the copy operation fails, an error message appears below the progress bar.

    ![Error message during copying of test suites.](../image/atf-copy-test-suites-error.png)

4.  In the **Name** field, enter the name that you want to assign to this new test suite.

5.  Edit the tests and test suites within the copied test suite.

6.  When you are finished making changes, select **Update**.


## Result

A copy of the test suite along with all the nested tests and child test suites is created.

**Parent Topic:**[Building and running automated test suites](../concept/atf-suites-overview.md)

