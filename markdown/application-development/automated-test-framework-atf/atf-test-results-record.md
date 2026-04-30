---
title: Test results record
description: A Test Results record contains detailed results information about one test execution. Client Error Details and Failure Details sections appear when a test fails due to error conditions, and include detailed error information you can use for troubleshooting purposes.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Test results, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Test results record

A Test Results record contains detailed results information about one test execution. Client Error Details and Failure Details sections appear when a test fails due to error conditions, and include detailed error information you can use for troubleshooting purposes.

<table id="table_fmz_nxp_scb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Test

</td><td>

Name of the test.

</td></tr><tr><td>

Status

</td><td>

Result of the Test execution:-   **Success**

Test passed.

-   **Failure**

Test failed.

-   **Success with warning\(s\)**

Test run passed but encountered client error\(s\) that were allowed as warnings in the Allowed Client Error table.

-   **Waiting**

Test waiting to start.

-   **Running**

Test is running.

-   **Skipped**

Occurs if an earlier test in the suite failed and **Abort on failure** is set to **true**.

-   **Error**

An error occurred in the test framework. For example, the test runner halted, or the server encountered an unintended scenario. The error message appears in the Summary field of the steps results record for the step that threw the error.

-   **Cancelled**

User canceled the Test.


</td></tr><tr><td>

Retain indefinitely

</td><td>

Check box to keep this record even after the specified data retention period has passed. For more information, see [Table Cleanup](../concept/table-cleanup.md).

</td></tr><tr><td>

Start time

</td><td>

Date and time of day at which this test started executing.

</td></tr><tr><td>

End time

</td><td>

Date and time of day at which this test finished executing.

</td></tr><tr><td>

Duration

</td><td>

Elapsed time it took to execute this test.

</td></tr><tr><td>

Previous test result

</td><td>

Results of the previous test execution, indicating if the test passed or failed. Only appears if this test result is for a re-run of a failed test and you are logged on with the admin, atf\_test\_admin, or atf\_test\_designer role. Click the information icon \(![Reference field icon](../image/atf-test-results-item.png)\) to navigate to the original test result. ![Previous test result](../image/atf-prev-test-results.png)

</td></tr></tbody>
</table>**Note:** If this test created screenshots, they appear as attachments in **Manage attachments**.

## Client Error Details

This section only displays when a test fails due to a client error.

<table id="table_inr_tr3_2db"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Failing step

</td><td>

Reference to the first test step result that failed during this test. Click the information icon \(![Reference field icon](../image/atf-test-results-item.png)\) to view detailed step results and error information in the Step Results form.

</td></tr><tr><td>

Summary

</td><td>

The following text indicates that a client error occurred at this step, and includes the detailed error message:`This step failed because the client error 'DETAILED ERROR MESSAGE' was detected on the page being tested. See failing Test Logs. To ignore these errors in the next test run, use ‘Add all client errors to warning/ignored list’ links.`

 Test designers and developers should always investigate client errors to determine if there are issues with your business process. For more details, see [Identify and resolve client errors](../task/identify-and-resolve-client-errors.md#).

</td></tr><tr><td>

First failing client error

</td><td>

Reference to the first client error that failed during the test. Click the information icon \( ![Reference field icon](../image/atf-test-results-item.png)\) to view detailed test results and error information in the Test Logs form.**Note:** For details on how to allow client errors as ignored or warning entries, refer to [Allowed client errors](../concept/whitelisted-client-errors.md)

</td></tr><tr><td>

Failing step screenshot

</td><td>

Screenshot of the step that failed. Click ![Reference field icon](../image/atf-test-results-item.png) to download the screenshot.

</td></tr></tbody>
</table>## Failure Details

This section only displays when a test fails due to a cause other than a client error.

|Field|Description|
|-----|-----------|
|Failing step|Reference to the first step result that failed during this test. Click ![Reference field icon](../image/atf-test-results-item.png) to download the screenshot.|
|Summary|Output of the step that failed.|
|Failing screenshot|Screenshot of the step that failed.|

## Additional information

This section is visible for all test results.

<table id="table_ixy_jkf_rdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Output

</td><td>

Output generated for the test step.-   Test result \(often `Passed` or `Failed`\).
-   For failed tests, includes the same error message detail displayed in the Summary field for the first test step that failed. See Client Error Details above.

</td></tr><tr><td>

Browsers involved

</td><td>

User agent strings returned by browsers that ran the test.

</td></tr></tbody>
</table><table id="table_wpw_syp_scb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Step Results

</td><td>

Record for each step result and log entry for this test.

</td></tr><tr><td>

Test Log

</td><td>

Record for each test log related to this test results record.

</td></tr><tr><td>

Test Transactions

</td><td>

Record for each transaction \(from the system transaction log \[syslog\_transaction\] related to this record\).To view the step results associated with a transaction, click the appropriate link in the **Step Results** column.

 To view the transaction logs associated with a transaction, click the appropriate link in the **Transaction** column.

 **Note:** The system may not be able to log some transactions with short durations.

</td></tr><tr><td>

Warnings

</td><td>

List of test logs containing client errors with a warning status. The Warnings related list only appears on test results with warnings.

</td></tr></tbody>
</table>**Parent Topic:**[Test results](../concept/atf-test-results-module.md)

**Related topics**  


[View test results and automated test results](../task/atf-view-results-consolidated.md)

[Test logs record](atf-test-log-record.md)

[Step results record](atf-step-result-record.md)

[Allowed client errors](../concept/whitelisted-client-errors.md)

[Allow client errors from step results](../task/whitelist-errors-from-step-results-related-list.md)

[Allow client errors from the test logs](../task/whitelist-errors-from-test-log-related-list.md)

