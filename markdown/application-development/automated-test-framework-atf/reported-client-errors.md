---
title: Reported client errors
description: The Reported Client Error module lists test logs across all tests that are client errors and have failed. You can review individual test log records, and allowed client errors as needed to prevent them from adversely impacting future test executions.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Run, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Reported client errors

The Reported Client Error module lists test logs across all tests that are client errors and have failed. You can review individual test log records, and allowed client errors as needed to prevent them from adversely impacting future test executions.

<table id="table_blw_q24_sbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start time

</td><td>

Time at which this test step started executing.

</td></tr><tr><td>

Step

</td><td>

Name of the step executed.

</td></tr><tr><td>

Status

</td><td>

The result of the test log.Failure: Test step run failed.

</td></tr><tr><td>

Output

</td><td>

Output generated for the test log. For a client error, the actual client error is displayed.

</td></tr><tr><td>

Duration

</td><td>

Time duration it took to execute this test step.

</td></tr><tr><td id="type">

Type

</td><td>

Type of test log. Client Error

**Note:** You can optionally add client errors as an ignored or warning entry in the Allowed Client Errors. Doing so prevents the allowed client errors from affecting ATF test executions when they recur in future test runs. For more details, see [Allowed client errors](../concept/whitelisted-client-errors.md).

</td></tr><tr><td>

Recorded at

</td><td>

Time at which this step or log entry was recorded.

</td></tr></tbody>
</table>**Parent Topic:**[Run](../concept/run-module.md)

**Related topics**  


[Allowed client errors](../concept/whitelisted-client-errors.md)

[Manually allow client errors](../task/atf-view-manually-add-whitelisted-browser-errors.md)

[Identify and resolve client errors](../task/identify-and-resolve-client-errors.md#)

