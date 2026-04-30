---
title: Step results record
description: The Step Results record contains information about one step in a test result. You access specific step results from the Step Results related list in the Test Results record.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Test results, Reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Step results record

The Step Results record contains information about one step in a test result. You access specific step results from the Step Results related list in the Test Results record.

<table id="table_zhx_ck5_pcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

Result of the step:-   **Success**

Test step passed.

-   **Failure**

Test step failed.

-   **Success with warning\(s\)**

Test step passed but encountered client error\(s\) that were allowed as warnings in the Allowed Client Error table.

-   **Skipped**

Occurs if an earlier test in the suite failed and **Abort on failure** is set to **true**.

-   **Error**

An error occurred in the test framework. For example, the test runner halted or the server encountered an unintended scenario.

-   **Cancelled**

User canceled the test or suite.


</td></tr><tr><td id="type">

Type

</td><td id="type-text">

Type of test result item: Step Result

</td></tr><tr><td>

Summary

</td><td>

Summarized version of the Output field.If an error occurred in the test step, the following text indicates that a client error occurred at this step, and includes a detailed exception/error message.

 `This step failed because the client error 'DETAILED ERROR MESSAGE' was detected on the page being tested. See failing Test Logs. To ignore these errors in the next test run, use ‘Add all client errors to warning/ignored list’ links.`

 Test designers and developers should always investigate client errors to determine if there are issues with your business process. For more details, see [Identify and resolve client errors](../task/identify-and-resolve-client-errors.md#).

 For a Send REST Request - Inbound step, the URL for the request endpoint, and a response code. For example:

 `The HTTP request has been sent to the endpoint 'https://demonightlyus.service-now.com/api/now/table/kb_knowledge'`

</td></tr><tr><td>

Output

</td><td>

Generated output for the test step.-   For a step result, the outputs from the step, including any explanation why a step failed or was skipped.
-   For a Send REST Request - Inbound step, the REST request and response including the response body. The output field is truncated at 4096 characters.
    -   The REST request and response headers are filtered to prevent sensitive information from being added to the log. A filtered header text is replaced with the text "Header redacted for security."
    -   See [Filter REST request and response headers](../concept/atf-filter-rest-headers.md) for information on how to add a list of REST request and response headers to be filtered.

 For additional console logging and test execution information for a test step, see the Test Logs record.

</td></tr><tr><td>

Step

</td><td>

Name of the step executed.

</td></tr><tr><td>

Test Result

</td><td>

Reference to the test result associated with this step result. Click the information icon \( ![Reference field icon](../image/atf-test-results-item.png)\) to view detailed test results information.

</td></tr><tr><td>

Description

</td><td>

Description of the specific actions performed \(for example, Open Create Incident Report Producer, Validate that the form matches the following condition\) for this test step. For a client log, blank.

</td></tr><tr><td>

Start Time

</td><td>

Date and time of day at which this step or log entry started.

</td></tr><tr><td>

End Time

</td><td>

Date and time of day at which this step or log entry ended.

</td></tr><tr><td>

Duration

</td><td>

Elapsed time it took to execute this test.

</td></tr><tr><td>

Step Transactions \(related list\)

</td><td>

Record for each transaction \(from the system transaction log \[syslog\_transaction\] related to this step result\).

</td></tr></tbody>
</table>**Parent Topic:**[Test results](../concept/atf-test-results-module.md)

**Related topics**  


[Test results record](atf-test-results-record.md)

[Test logs record](atf-test-log-record.md)

[Allowed client errors](../concept/whitelisted-client-errors.md)

[Allow client errors from step results](../task/whitelist-errors-from-step-results-related-list.md)

