---
title: Building and running automated tests with the Automated Test Framework
description: Basic tasks in the Automated Test Framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/atf-build-overview.html
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Building and running automated tests with the Automated Test Framework

Basic tasks in the Automated Test Framework.

To build and run any test, you always perform certain operations:

-   [Create a new automated test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-create-test.md)
-   [Add steps to an automated test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-create-step.md)
-   [Run an automated test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-run-test.md)
-   [View the progress of automated tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-view-progress.md)
-   [View test results and automated test results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-view-results-consolidated.md)

You perform other operations often, but not necessarily for every test.

-   For tests involving form steps, you might need to [View results screenshots from an automated test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-view-results-consolidated.md).
-   For some tests, you might need to know about [Passing data from one automated test step to another](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-passing-data.md).
-   Some steps frequently occur in the same sequence in many different tests, so you can [Add a predefined list of steps \(template\) to an automated test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-use-template.md).

-   **[Create a new automated test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-create-test.md)**  
Create a named automated test containing a series of steps to execute.
-   **[Copy automated test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-copy-test.md)**  
Copy an existing test, which you can then re-name and modify.
-   **[Run an automated test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-run-test.md)**  
After creating an automated test, run it on a non-production instance.
-   **[Implementing breakpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-breakpoints-rollback.md)**  
Breakpoints allow you to pause your test at any step of a test run in order to troubleshoot and test authoring.
-   **[View test results and automated test results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-view-results-consolidated.md)**  
View test results from completed test and test suite runs. Carefully consider the results of automated test runs and perform any corrective actions required to resolve any revealed issues.
-   **[Identify and resolve client errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/identify-and-resolve-client-errors.md)**  
Identify client errors and resolve them in client-side scripts.
-   **[UI test steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/ui-test-steps.md)**  
Test user interfaces by mimicking user actions and interacting with the visible components of a page.
-   **[Server test steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/server-test-steps.md)**  
Test business logic and background processes by performing operations on the server.
-   **[Attachment test steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/attachment-test-steps.md)**  
Test an attachment-dependent business rule by uploading an attachment either from a form or from a server-side API call. For example, you can have a business rule that doesn't let you close an incident without an attachment such as a screenshot.
-   **[List UI actions test steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-list-ui-actions-test-step.md)**  
Select a UI action from a list to perform different actions on a list or a related list.
-   **[Parameterized tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/parameterized-tests.md)**  
Run a test multiple times with different test data for each run. Create parameters to store test data for each test run.
-   **[Allowed client errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/whitelisted-client-errors.md)**  
Add known client errors to the allowed client errors list to allow tests and steps to continue running when a specific error occurs. Set the report level to specify what the Automated Test Framework does when the error occurs in future tests.
-   **[View the progress of automated tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-view-progress.md)**  
When an automated test is running, view its progress in the Run Test progress dialog.
-   **[Passing data from one automated test step to another](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-passing-data.md)**  
Some automated test steps create data that you can use as an input to a subsequent step.

**Parent Topic:**[Automated Test Framework \(ATF\) test building and execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-test-build-execution.md)

**Related topics**  


[Building and running automated test suites]()

[Auto-generate ATF tests]()

[Cancelling automated tests and test suites]()

