---
title: View test results and automated test results
description: View test results from completed test and test suite runs. Carefully consider the results of automated test runs and perform any corrective actions required to resolve any revealed issues.When viewing test results, step results or test logs, you can allow client errors as ignored or warning entries in the Allowed Client Errors table. This allows test executions to continue past client errors in future test runs.If the test has a UI component, the system takes screenshots of the UI. View these screenshots to gain further insight into the test results.View results from an automated test suite.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# View test results and automated test results

View test results from completed test and test suite runs. Carefully consider the results of automated test runs and perform any corrective actions required to resolve any revealed issues.

## Before you begin

Role required: none

## About this task

Test and test suite results show how long it took the system to execute a test and which steps failed. They can include screenshots of form steps. You can also view reports comparing different runs of the same test suites.

You have multiple options for navigating to the test results, depending on where you are in the user interface. For example, if the Run Test progress dialog is displayed, you can select **Go to Result**. This procedure enables you to view test results from any location in the user interface.

## Procedure

1.  Navigate to **Automated Test Framework** &gt; **Test Results**.

2.  Click a row to access the results for a specific test.

    The system displays the [Test results record](../reference/atf-test-results-record.md).

3.  View step results for the selected test.

    1.  Click the Step Results related list.

    2.  Scroll down and click the row for the step result you want to view.

        The system displays the [Step results record](../reference/atf-step-result-record.md).

4.  View test logs for this test result.

    1.  Click the Test Log related list.

    2.  Scroll down and click the row for the test log you want to view.

        The system displays the [Test logs record](../reference/atf-test-log-record.md).


**Parent Topic:**[Building and running automated tests with the Automated Test Framework](../concept/atf-build-overview.md)

## View automated test results

When viewing test results, step results or test logs, you can allow client errors as ignored or warning entries in the Allowed Client Errors table. This allows test executions to continue past client errors in future test runs.

## View results screenshots from an automated test

If the test has a UI component, the system takes screenshots of the UI. View these screenshots to gain further insight into the test results.

### Before you begin

You must have run the test whose results screenshots you want to view.

**Note:** For best results with screen shots, leave the browser zoom level set to 100%.

Role required: atf\_test\_admin or atf\_test\_designer

### Procedure

1.  Navigate to **Automated Test Framework** &gt; **Test Results**.

2.  Click the row containing the test whose results you want to view.

    The system displays the **Test Results**form.

3.  View a screenshot taken during the test by finding the screenshot you want in the attachments list.

    Screenshots are named with the word **screenshot** followed by the timestamp \(always in UTC time\) for when the system recorded the shot. You can match the screenshot to the test step by comparing the step and screenshot timestamps.


## View automated test suite results

View results from an automated test suite.

### About this task

**Note:** You have multiple options for navigating to the test suite results, depending on where you are in the user interface. For example, if the Run Test progress dialog is displayed, you can click **Go to Result** instead. The procedure described here enables you to view test suite results from any location in the user interface.

### Procedure

1.  Navigate to **Automated Test Framework** &gt; **Suite Results**.

2.  Click the row containing the test whose results you want to view.

    The system displays the [Test suite results record](../reference/atf-test-suite-results-record.md).


**Related topics**  


[Identify and resolve client errors](identify-and-resolve-client-errors.md#)

[Allow client errors from test results](whitelist-errors-from-test-results.md)

[Allow client errors from step results](whitelist-errors-from-step-results-related-list.md)

[Allow client errors from the test logs](whitelist-errors-from-test-log-related-list.md)

