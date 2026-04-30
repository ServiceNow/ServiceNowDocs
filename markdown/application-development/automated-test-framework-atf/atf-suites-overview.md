---
title: Building and running automated test suites
description: Run a group of tests in a specific order to test an application or a group of related features.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Building and running automated test suites

Run a group of tests in a specific order to test an application or a group of related features.

A test suite can contain both individual tests and other test suites. A test suite that contains another test suite is called a parent, and the test suite contained within the parent is called a child. While a test suite can have both individual tests and test suites as children, tests cannot have other tests as children. Tests can only contain test steps.

## Benefits

Grouping tests into test suites offers these benefits.

-   Allows testers to run every test in a test suite with one action.
-   Allows testers to run all child test suites in a parent test suite.
-   Allows testers to see test results for every test in a test suite.
-   Allows test designers and testers to schedule when to run test suites.
-   Allows test designers and testers to schedule starting client test runners to support test runs.

## Hierarchies

Automated Test Framework supports building a multi-level hierarchies where a test suite can be both a parent and child. For example, this figure illustrates Test Suite 1 as the parent at the top of the hierarchy. Test Suite 1.3 is a child of Test Suite 1 and also a parent of Test Suite 1.3.1 and Test Suite 1.3.2.

![Diagram of example test suite hierarchy](../image/test-suite-hierarchy.png "Example of Test Suite Hierarchy")

## Schedules

To schedule a test suite, you need three components:

-   a test suite record
-   a schedule record specifying when you want the system to run the test suite
-   a scheduled suite run record that associates the test suite to run with the schedule for running it

With this model, you can associate a schedule with many different test suites, and vice versa.

**Note:** You can schedule only test suites, not individual tests. Scheduled tests will run only if there is an open Scheduled Client Test Runner page matching the scheduled suite's browser conditions. Scheduled tests cannot run on a machine that is locked, powered down, or does not already have the browser open.

The watchlist on the test suite run record also allows you to specify users to receive an email when the system finishes executing the test suite run.

If the test suite contains one or more form steps \(steps involving a user interface\), you must ensure that a scheduled client test runner is actively running in a browser when the schedule triggers the suite run.

**Note:** See [Browser recommendations and requirements](atf-test-runners.md#kvv_h25_gx) for recommendations and requirements for running the client test runner.

For step-by-step instructions on how to schedule a test suite, see [Schedule an automated test suite](../task/atf-sched-suite-steps.md).

## Filters

Automate the creation of test suites by using a filter to dynamically add tests to a test suite when they match the filter conditions. Reduce the time that your test designers spend manually creating and maintaining test suites.

-   **[Create an automated test suite](../task/atf-create-suite.md)**  
Group automated tests into a suite you can execute as a batch.
-   **[Copy an automated test suite](../task/atf-copy-test-suite.md)**  
Reduce time when creating tests by copying an entire test suite. Rename and modify the test suite after copying. The **Copy Test Suite** button on the Test Suite form copies all the nested tests and child test suites within the text suite.
-   **[Add tests to a suite with a filter](../task/add-tests-suite-filter.md)**  
Automate the creation of test suites by using a filter to dynamically add tests to a test suite when they match the filter conditions. Reduce the time that your test designers spend manually creating and maintaining test suites.
-   **[Add test to an existing automated test suite](../task/atf-add-test-to-suite.md)**  
Add a test to a test suite that already exists.
-   **[Add child test suite to parent test suite](../task/atf-add-child-suite.md)**  
Add to a multi-level test suite by including a child test suite within a parent test suite.
-   **[Run an automated test suite](../task/atf-run-suite.md)**  
After creating an automated test suite, run it in a non-production instance.
-   **[Schedule an automated test suite](../task/atf-sched-suite-steps.md)**  
Schedule one or more test suites to run at a specific date and time.
-   **[Run a scheduled test suite using a script](run-scheduled-test-suite-script.md)**  
Execute a scheduled UI test suite immediately using a script without having to wait for the scheduled time. You can use this method while trying to automate the process of running a test.
-   **[Re-run failed tests in an automated test suite](../task/atf-rerun-tests.md)**  
Re-run failed tests within a test suite without rerunning the entire suite.

**Parent Topic:**[Automated Test Framework \(ATF\) test building and execution](atf-test-build-execution.md)

**Related topics**  


[Building and running automated tests with the Automated Test Framework](atf-build-overview.md)

[Auto-generate ATF tests](../task/atf-auto-generate-tests.md)

[Cancelling automated tests and test suites](atf-cancelling.md#)

[Suites](suites-module.md)

[Step results record](../reference/atf-step-result-record.md)

