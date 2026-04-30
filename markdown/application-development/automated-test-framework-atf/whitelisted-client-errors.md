---
title: Allowed client errors
description: Add known client errors to the allowed client errors list to allow tests and steps to continue running when a specific error occurs. Set the report level to specify what the Automated Test Framework does when the error occurs in future tests.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Building and running automated tests with the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Allowed client errors

Add known client errors to the allowed client errors list to allow tests and steps to continue running when a specific error occurs. Set the report level to specify what the Automated Test Framework does when the error occurs in future tests.

## Scenarios for allowing client errors

Test designers and developers typically allow client-side JavaScript errors to prevent certain types of known failures from impacting test design and results. Scenarios to allow client errors include:

-   **Timing constraints**

    Temporarily allow a client error until your developers have time to investigate and resolve the issue. For example, when testing an old form containing a longstanding bug.

-   **Minimizing the impact of old libraries**

    Ignore client errors that cannot be fixed or are unimportant to your operations to eliminate their impact on future test runs. For example, when you find a bug in an old library.

-   **Test design time**

    Temporarily allow client errors until you finish writing tests and have time to investigate the error. For example, one of your developers modifies a UI policy and the change generates an error.

-   **Possible platform bug**

    Temporarily allow client errors until a fix is available. Prior to reporting a platform bug to ServiceNow Technical Support, investigate the error, verify it is not a customization error, and identify the type of platform bug involved. For example, a UI policy generates an error during a test. Your investigation verifies that the issue is not a customization error and identifies a platform issue with the UI policy.


**Note:** While adding client errors to the allowed client errors list allows the test framework to continue testing, it does not guarantee that your tests pass. Test designers and developers should always investigate client errors to determine if there are issues with your business process. For more details, see [Identify and resolve client errors](../task/identify-and-resolve-client-errors.md#).

## Report levels for allowed client errors

The report level indicates whether the test framework reports future occurrences of the error as a warning or ignores them altogether. You can change the report level of an allowed error at any time. For example, if you originally add an error as a warning, you can later change the report level to ignored.

|Report level|Description|
|------------|-----------|
|Warning|Test steps containing the allowed client error report a status of `Success with warning(s)`. The error message appears in the test result output, and is recorded in the test logs with the status `Warning`.|
|Ignored|Test steps containing the allowed client error report a status of `Success`. The error is recorded in the test logs with an `Ignored` status.|

## Matching process

The Automated Test Framework identifies allowed client errors using a contains search rather than an exact string match. A match occurs when a client error contains a message from an Allowed Client Error \[sys\_atf\_whitelist\] record. For example, if you create an Allowed Client Error record for the error message "`Test message`" with a report level of Ignored, then any client error containing this string is ignored.

**Note:** When you create or modify an Allowed Client Error record, the Client Test Runner automatically gets the update.

## Identifying and resolving client errors

When client errors occur, the Automated Test Framework fails the test on the step that was executing when the error occurred.

-   **[Allow client errors from test results](../task/whitelist-errors-from-test-results.md)**  
Allow client errors as you review test results.
-   **[Allow client errors from step results](../task/whitelist-errors-from-step-results-related-list.md)**  
Allow client errors as you review step results.
-   **[Allow client errors from the test logs](../task/whitelist-errors-from-test-log-related-list.md)**  
Allow client errors as you review test logs.
-   **[Manually allow client errors](../task/atf-view-manually-add-whitelisted-browser-errors.md)**  
Manually create allowed client error entries as needed in the Allowed Client Errors table.

**Parent Topic:**[Building and running automated tests with the Automated Test Framework](atf-build-overview.md)

