---
title: Building and running automated tests with the Automated Test Framework
description: Basic tasks in the Automated Test Framework.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Building and running automated tests with the Automated Test Framework

Basic tasks in the Automated Test Framework.

To build and run any test, you always perform certain operations:

-   [Create a new automated test](../task/atf-create-test.md)
-   [Add steps to an automated test](../task/atf-create-step.md)
-   [Run an automated test](../task/atf-run-test.md)
-   [View the progress of automated tests](../task/atf-view-progress.md)
-   [View test results and automated test results](../task/atf-view-results-consolidated.md)

You perform other operations often, but not necessarily for every test.

-   For tests involving form steps, you might need to [View results screenshots from an automated test](../task/atf-view-results-consolidated.md).
-   For some tests, you might need to know about [Passing data from one automated test step to another](atf-passing-data.md).
-   Some steps frequently occur in the same sequence in many different tests, so you can [Add a predefined list of steps \(template\) to an automated test](../task/atf-use-template.md).

-   **[Create a new automated test](../task/atf-create-test.md)**  
Create a named automated test containing a series of steps to execute.
-   **[Copy automated test](../task/atf-copy-test.md)**  
Copy an existing test, which you can then re-name and modify.
-   **[Run an automated test](../task/atf-run-test.md)**  
After creating an automated test, run it on a non-production instance.
-   **[Implementing breakpoints](atf-breakpoints-rollback.md)**  
Breakpoints allow you to pause your test at any step of a test run in order to troubleshoot and test authoring.
-   **[View test results and automated test results](../task/atf-view-results-consolidated.md)**  
View test results from completed test and test suite runs. Carefully consider the results of automated test runs and perform any corrective actions required to resolve any revealed issues.
-   **[Identify and resolve client errors](../task/identify-and-resolve-client-errors.md#)**  
Identify client errors and resolve them in client-side scripts.
-   **[UI test steps](ui-test-steps.md)**  
Test user interfaces by mimicking user actions and interacting with the visible components of a page.
-   **[Server test steps](server-test-steps.md)**  
Test business logic and background processes by performing operations on the server.
-   **[Attachment test steps](attachment-test-steps.md)**  
Test an attachment-dependent business rule by uploading an attachment either from a form or from a server-side API call. For example, you can have a business rule that doesn't let you close an incident without an attachment such as a screenshot.
-   **[List UI actions test steps](atf-list-ui-actions-test-step.md)**  
Select a UI action from a list to perform different actions on a list or a related list.
-   **[Parameterized tests](parameterized-tests.md)**  
Run a test multiple times with different test data for each run. Create parameters to store test data for each test run.
-   **[Allowed client errors](whitelisted-client-errors.md)**  
Add known client errors to the allowed client errors list to allow tests and steps to continue running when a specific error occurs. Set the report level to specify what the Automated Test Framework does when the error occurs in future tests.
-   **[View the progress of automated tests](../task/atf-view-progress.md)**  
When an automated test is running, view its progress in the Run Test progress dialog.
-   **[Passing data from one automated test step to another](atf-passing-data.md)**  
Some automated test steps create data that you can use as an input to a subsequent step.

**Parent Topic:**[Automated Test Framework \(ATF\) test building and execution](atf-test-build-execution.md)

**Related topics**  


[Building and running automated test suites](atf-suites-overview.md)

[Auto-generate ATF tests](../task/atf-auto-generate-tests.md)

[Cancelling automated tests and test suites](atf-cancelling.md#)

