---
title: Manually allow client errors
description: Manually create allowed client error entries as needed in the Allowed Client Errors table.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Allowed client errors, Building and running automated tests with the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Manually allow client errors

Manually create allowed client error entries as needed in the Allowed Client Errors table.

## Before you begin

Role required: atf\_admin, atf\_test\_designer, or admin

## About this task

You normally allow client errors directly from a test result, step result, or test log, but you can manually allow them.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Run** &gt; **Allowed Client Errors**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_kxg_qzk_ddb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Report level

</td><td>

Report action to take when the client error is encountered. Options include:-   **Warning – Step &amp; Test will report Success with Warning\(s\)**: Test steps containing the allowed client error report a status of `Success with warning(s)`. The error message appears in the test result output, and is recorded in the test logs with the status `Warning`.
-   **Ignored – Step &amp; Test will report Success**: Test steps containing the allowed client error report a status of `Success`. The error is recorded in the test logs with an `Ignored` status.


</td></tr><tr><td>

Active

</td><td>

Check box to enable or disable allowing a client error.

</td></tr><tr><td>

Error message

</td><td>

Message of the client error you want to allow.

</td></tr><tr><td>

Description

</td><td>

Description of the error you want to allow. If this client error was allowed from a test result, step result, or a test log, the test log description is copied into this field.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Allowed client errors](../concept/whitelisted-client-errors.md)

**Related topics**  


[Allowed client errors](../concept/whitelisted-client-errors.md)

