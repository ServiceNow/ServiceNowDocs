---
title: Test logs record
description: The Test Results Item \(test log\) record contains console logging and test execution information.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Test results, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Test logs record

The Test Results Item \(test log\) record contains console logging and test execution information.

During test execution, any information reported to the environment is recorded in the Test Log \(sys\_atf\_test\_result\_item\) table. This information can include browser console logging, results, and error messages recorded by step environments. You access specific test logs from the Test Log related list in the Test Results form.

<table id="table_blw_q24_sbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

The result of the test log:-   **Success**

Test step run passed.

-   **Failure**

Test step run failed.

-   **Success with warning\(s\)**

Test step passed but encountered client error\(s\) that were allowed as warnings in the Allowed Client Error table.

-   **Ignored**

Client error that has been allowed with a report level of Ignored.

-   **Warning**

Client error that has been allowed with a report level of Warning.

-   **Waiting**

Test or suite waiting to start.

-   **Running**

Test or suite is running.

-   **Skipped**

Occurs if an earlier test in the suite failed and **Abort on failure** is set to **true**.

-   **Error**

An error occurred in the test framework. For example, the test runner halted or the server encountered an unintended scenario. The error message appears in the Summary field of the Steps Results record for the step that threw the error.

-   **Cancelled**

User canceled the test or suite.


</td></tr><tr><td id="type">

Type

</td><td>

Type of test log: -   Step Result
-   Client Log
-   Client Error

 **Note:** If a Client Error, you can optionally add it as an ignored or warning entry in the Allowed Client Errors. Doing so prevents the allowed client errors from affecting ATF test executions when they recur in future test runs. For more details, refer to [Allowed client errors](../concept/whitelisted-client-errors.md).

</td></tr><tr><td>

Output

</td><td>

Output generated for the test log.-   For a step result, the console logging and test execution outputs from the step, including any explanation why a step failed or was skipped.
-   For a client log, the log entry text.
-   For a client error, the actual client error is displayed.

</td></tr><tr><td>

Step

</td><td>

Name of the step executed. This field may be blank for a client log.

</td></tr><tr><td>

Test Result

</td><td>

Reference to the test result associated with this step result. Click ![Reference field icon](../image/atf-test-results-item.png) to view detailed test result information.

</td></tr><tr><td>

Description

</td><td>

For a step result, the actions performed in this test step. For a client log, blank.

 For a client, this message displays: `This client error occurred on the page in Browser Type Browser Version` \(for example, Chrome 62.0.3202.62\).

</td></tr><tr><td>

Start time

</td><td>

Time at which this test step started executing.

</td></tr><tr><td>

End time

</td><td>

Time at which this test step finished executing.

</td></tr><tr><td>

Duration

</td><td>

Time duration it took to execute this test step.

</td></tr><tr><td>

Recorded at

</td><td>

Time at which this step or log entry was recorded.

</td></tr><tr><td>

Allow listed client error

</td><td>

Reference to the Allowed Client Error record \(if any\). Click ![Reference field icon](../image/atf-test-results-item.png) to view the Allowed Client Error record for this client error.

</td></tr></tbody>
</table>**Parent Topic:**[Test results](../concept/atf-test-results-module.md)

**Related topics**  


[Test results record](atf-test-results-record.md)

[Step results record](atf-step-result-record.md)

[Allow client errors from the test logs](../task/whitelist-errors-from-test-log-related-list.md)

[Allowed client errors](../concept/whitelisted-client-errors.md)

