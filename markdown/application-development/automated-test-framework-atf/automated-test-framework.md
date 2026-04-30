---
title: Exploring Automated Test Framework
description: The Automated Test Framework helps you ensure the integrity of your instance by enabling the creation and execution of automated tests following any changes.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Exploring Automated Test Framework

The Automated Test Framework helps you ensure the integrity of your instance by enabling the creation and execution of automated tests following any changes.

## Benefits

Automated Test Framework provides these benefits for change managers and developers.

-   Reduce upgrade and development time by replacing manual testing with automated testing.
-   Design tests once and reuse them in different contexts and with different test data sets.
-   Keep test instances clean by rolling back test data and changes made after each test run.
-   Create test suites to organize and run tests in batches.
-   Schedule test suite runs.
-   Enable non-technical test designers to create tests of standard ServiceNow AI Platform functionality.
-   Reduce test design time by copying quick start tests and test suites.
-   Create custom test steps to expand test coverage.

## Automated Test Framework records and components

The Automated Test Framework consists of these records and components.

## Test

A test is a logical grouping of related automated test steps that verify some functionality or feature. Each test is a record in the Test \[sys\_atf\_test\] table. Test designers typically create a test to verify one feature or a group of related features. For example, the **CSM: Create Product Case** test validates the creation of Product Case records. Each test has a related list of test steps and test results.

## Test suite

A test suite is a collection of tests that run in a specific order. Test designers typically create a test suite to test an application or a group of related features. For example, the **CSM: Case Management** test suite validates the functionality of the Customer Service Management application. Test designers can schedule running test suites and starting any required client test runners.

## Quick start test

A quick start test is a test or test suite installed with the demo data of an application. Use quick start tests as templates to build your own tests and test suites. See [this quick start test overview video](https://www.youtube.com/watch?v=-4DTeOGBCpI) for more information.

## Test step

A test step combines a step configuration with the runtime test data necessary to run a step. The test step always specifies the order in which it runs in the test. Test steps have their own related list of step results. Each test step is a record in the Test Step \[sys\_atf\_step\] table that specifies a test action, the step configuration, and an execution order. Test designers add test steps to tests to verify functionality. For example, the first test step of the **CSM: Create Product Case** test is to impersonate the demo user John Jason who is authorized for Case Management.

## Step configuration

A step configuration is a specific test action the Automated Test Framework can run. Step configurations do not contain any runtime test data and can only be run when test designers add them as part of a test step. Each step configuration is a record in the Test Step Config \[sys\_atf\_step\_config\] table that specifies the input variables used to run the step configuration and the output variables available to other step configurations. For example, the **Impersonate** step configuration allows a test to impersonate another user.

The Automated Test Framework provides a default list of step configurations for most use cases and allows test designers to create their own custom step configurations.

## Step variable

A step variable stores step-specific input and output values. For example, the **Open a New Form** step configuration has variables to specify the table and form view names. Use step variables to specify a particular test step target or to pass information to other test steps.

## Test result

A test result stores the output of a test or test suite run. Each test result is a record in the Test Result \[sys\_atf\_test\_result\] table that specifies the duration of the test run, the status of the test, and screenshots where available. Use test results to identify failing or non-running tests, and use the test logs to see more information about test results. By default, the system deletes test and test suite results 30 days after creation unless you enable the option to retain the test result indefinitely.

## Step result

A step result stores the output of a test step run. Each step result is a record in the Step Result \[sys\_atf\_test\_result\_step\] table that specifies the status of the test step, a summary of the output, and a complete log of the output generated by the test step. Use step results to identify failures and functionality needing review.

## Assert type

The **Assert type** field specifies the conditions that must be met for a test to pass. Test designers can use assertions to specify whether the results of an operation are expected or unexpected. For example, suppose you want to test that a record cannot be updated. In this case, you would add a Record Insert test step and set the **Assert type** field to **Record was not inserted**. The test passes when the record insert fails.

Some test step categories that include steps with an **Assert type** field include:

-   [Server category](../reference/test-steps-server-category.md#): Assert which CRUD operations cause a test to pass or fail.
-   [Custom UI category](../reference/test-steps-custom-ui-category.md#): Assert which component states cause a test to pass or fail, and whether visible text causes a test to pass or fail.
-   [Forms in Service Portal category](../reference/test-steps-forms-portal-category.md#): Assert whether a form canceled in the browser due to validation errors, or a form successfully submitted to the server causes a test to pass.

## Client test runners

A client test runner is a browser tab that runs client-side test steps within a ServiceNow AI Platform user interface. Client test runners require a browser tab to function. If no client test runner is available when you run a test, the system prompts you to open one. Testers can manually start a client test runner or select an existing client test runner. Test designers can schedule starting client test runners when they schedule running a test suite.

## User roles

Assign roles to define Automated Test Framework permissions.

<table id="table_spv_zx5_5fb"><thead><tr><th>

Role Title \[name\]

</th><th>

Role Description

</th></tr></thead><tbody><tr><td>

atf\_test\_admin

</td><td>

Create or edit Automated Test Framework properties. Has permission to:

 -   View the tests page
-   Create/edit/delete tests
-   Create/edit/delete test steps
-   View the step config page
-   View the test runner page
-   View the test suite results, test results and result items pages
-   Execute user tests
-   View, create, edit, delete and execute test suites
-   Create/edit step config records
-   Create/edit Automated Test Framework properties

</td></tr><tr><td>

atf\_test\_designer

</td><td>

View Automated Test Framework properties only \(cannot create or edit properties\). Has permission to:

 -   View the tests page
-   Create/edit/delete tests
-   Create/edit/delete test steps
-   View the step config page
-   View the test runner page
-   View the test suite results, test results and result items pages
-   Execute user tests
-   View, create, edit, delete and execute test suites
-   View Automated Test Framework properties

</td></tr><tr><td>

atf\_ws\_designer

</td><td>

View or set basic authentication profiles needed for REST endpoints that require authentication. See [REST category](../reference/test-steps-rest-category.md#) for more information.

</td></tr></tbody>
</table>ATF doesn't support these elements of Next Experience, but support for these features is planned for future releases:

-   Pages built with UI Builder, including pages with lists and form components.
-   Landing pages

**Note:** ATF still supports the Core UI, including Classic Environment \(such as classic lists and forms\).

