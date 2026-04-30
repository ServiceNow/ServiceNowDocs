---
title: Reusable tests
description: Leverage reusable tests to simplify test maintenance and streamline the management of large tests and test suites. Reusable tests reduce redundancy, ensuring consistent and reliable test execution across your system.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Automated Test Framework \(ATF\) tests types and testing ways, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Reusable tests

Leverage reusable tests to simplify test maintenance and streamline the management of large tests and test suites. Reusable tests reduce redundancy, ensuring consistent and reliable test execution across your system.

**Note:** A reusable test can be invoked only from another test \(a regular test or a reusable test\). The reusable test can’t be added to test suites individually.

Use the following related lists to pass variables from one test to another. Select **New** to create either the reusable input or output.

-   Reusable Input Variables: Contains the reusable input variables that are passed in from the parent test. The variable is passed from the test calling the current reusable test.
-   Reusable Output Variables: Contains the reusable output variables that are passed in from the child test. The variable is intended to be passed back up to the parent test calling the current reusable test.

![Screenshot showing input/output variables](../image/atf-reusable-test-i:o.png)

**Note:** The reusable input and output variables that you create for the test are shown under the Reusable Input Variables and Reusable Output Variables related lists. The input variables are passed in from the parent test that is calling the current reusable test and is used by the reusable test. The output variables are passed back to the parent test and are used only by its test steps.

Use the Reusable Test test step category to access the created reusable test records. See [Reusable Tests category](../reference/test-steps-reusable-tests-category.md) for more information.

-   **[Create a reusable test](../task/atf-create-reusable-tests.md)**  
Create a reusable test to avoid redundancy, ensuring better test maintenance and reliable test execution across the instance.
-   **[Invoke a reusable test](../task/atf-invoke-reusable-tests.md)**  
Implement the following steps to invoke a reusable test in a test \(regular or reusable test\) or a test in a test suite.

**Parent Topic:**[Automated Test Framework \(ATF\) tests types and testing ways](atf-test-type-testing.md)

**Related topics**  


[Mutually exclusive tests](mutual-exclusion-rule.md)

[Quick start tests](quick-start-tests.md)

[Parallel testing](parallel-testing.md)

[Performance profiling](atf-perf-prof.md#)

