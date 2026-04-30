---
title: Allow client errors from test results
description: Allow client errors as you review test results.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Allowed client errors, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Allow client errors from test results

Allow client errors as you review test results.

## Before you begin

Role required: atf\_test\_admin, atf\_test\_designer, or admin

## About this task

You can allow multiple or individual client errors. For each client error, you must decide how to report future instances of the client error. Report level options include:

-   Warning: Test steps containing the allowed client error report a status of `Success with warning(s)`. The error message appears in the test result output, and is recorded in the test logs with the status `Warning`.
-   Ignored: Test steps containing the allowed client error report a status of `Success`. The error is recorded in the test logs with an `Ignored` status.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Test Results**.

2.  Select the test result for a specific test.

    The system displays the Test Result record.

3.  From the Related links, select one of the following options:

    -   **Add all client errors to warning list**: Allow all client errors in this test with a report level of Warning.
    -   **Add all client errors to ignored list**: Allow all client errors in this test with a report level of Ignored.
    The Automated Test Framework allows the selected client errors and displays a status message at the top of the form.


**Parent Topic:**[Allowed client errors](../concept/whitelisted-client-errors.md)

**Related topics**  


[Allowed client errors](../concept/whitelisted-client-errors.md)

