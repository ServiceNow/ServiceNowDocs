---
title: Test results
description: Each time you run a test, the automated test framework creates a record of the test results. Use the Test Results module to view details about the results of individual tests and individual steps within a test. If the test generated screenshots, they appear as attachments on the test results record.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Test results

Each time you run a test, the automated test framework creates a record of the test results. Use the Test Results module to view details about the results of individual tests and individual steps within a test. If the test generated screenshots, they appear as attachments on the test results record.

Each Test Results record displays detailed results information about one test execution, and contains links to detailed step results and test logs. Step results records display information about one step in a test result, while test log \(test results item\) records contain detailed console logging and test execution information.

By default, the system deletes test and test suite results data 30 days after creation. You can modify this default retention policy as needed in the Table Cleanup module.

-   **[Test results record](../reference/atf-test-results-record.md)**  
A Test Results record contains detailed results information about one test execution. Client Error Details and Failure Details sections appear when a test fails due to error conditions, and include detailed error information you can use for troubleshooting purposes.
-   **[Step results record](../reference/atf-step-result-record.md)**  
The Step Results record contains information about one step in a test result. You access specific step results from the Step Results related list in the Test Results record.
-   **[Test logs record](../reference/atf-test-log-record.md)**  
The Test Results Item \(test log\) record contains console logging and test execution information.

**Parent Topic:**[Automated Test Framework \(ATF\) reference](atf-ref-overview.md)

**Related topics**  


[Modify data retention policy for ATF test results](../task/atf-edit-table-cleanup.md)

[Table Cleanup module](table-cleanup.md)

