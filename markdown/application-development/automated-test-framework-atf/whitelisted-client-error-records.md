---
title: Allowed client error records
description: Review the list of existing Allowed Client Error \[sys\_atf\_whitelist\] records to see which client errors produce warnings and which are ignored. Modify existing Allowed Client Error records as needed or create new ones.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Run, Automated Test Framework reference, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Allowed client error records

Review the list of existing Allowed Client Error \[sys\_atf\_whitelist\] records to see which client errors produce warnings and which are ignored. Modify existing Allowed Client Error records as needed or create new ones.

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

Check box to enable or disable allowing of a client error.

</td></tr><tr><td>

Error message

</td><td>

Message of the client error you want to allow.

</td></tr><tr><td>

Description

</td><td>

Description of the error you want to allow. If this client error was allowed from a test result, step result, or a test log, the test log description is copied into this field.

</td></tr></tbody>
</table>**Parent Topic:**[Run](../concept/run-module.md)

**Related topics**  


[Allowed client errors](../concept/whitelisted-client-errors.md)

