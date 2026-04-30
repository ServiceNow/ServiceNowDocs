---
title: Test Management 2.0 overview
description: Test Management 2.0 helps you deliver software products more efficiently and with fewer defects by managing and streamlining testing processes for both testers and managers. You can create multiple versions of a test and integrate with Agile Development 2.0.
locale: en-US
release: yokohama
product: Test Management
classification: test-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Test Management 2.0, Test Management applications, Strategic Portfolio Management]
---

# Test Management 2.0 overview

Test Management 2.0 helps you deliver software products more efficiently and with fewer defects by managing and streamlining testing processes for both testers and managers. You can create multiple versions of a test and integrate with Agile Development 2.0.

To learn about the different versions of Test Management and to choose the version that helps you meet your testing requirements, see [Test Management applications](test-management-overview.md).

**Important:**

Test Management 2.0 is not active by default on all instances. To use Test Management 2.0, activate the `com.snc.test_management.2.0` plugin. For more information, see [Activate Test Management 2.0](../task/activate-test-management2.md).

<table id="table_y12_nws_jdb"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tester

</td><td>

Can run tests and track defects for a software product by: -   Creating tests and test sets.
-   Performing tests and recording test results.
-   Updating status of tests.
-   Creating defect records manually and linking them to failed tests for retesting.

 **Important:**

To record a defect for a failed test in Test Management 2.0, create a defect record manually and reference the test in the defect description.

</td></tr><tr><td>

Test Manager

</td><td>

Can set up and monitor the manual testing process of a software product by:-   Creating and maintaining tests and test sets.
-   Evaluating the tests, test steps, and test sets created by testers.
-   Facilitating test execution by creating test plans, fragmenting a test plan into test cycles, and test cycles into test execution suites.
-   Initiating a testing process by assigning tests to testers and then monitoring overall progress.
-   Assessing test results and closing a test plan.

</td></tr></tbody>
</table>## Key terminology

The following section describes the key terms used in Test Management 2.0.

<table id="table_axc_m2g_hdb"><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Test

</td><td>

A collection of conditions or steps used to determine whether a feature is working correctly. A test can also include an expected result, which is used to determine if the test case passes or fails. You can use the [Tests](../task/create-test2.md) module to create and maintain different versions of a test.

</td></tr><tr><td>

Test set

</td><td>

A collection of related tests. A test can be a part of one or more test sets.You can use the [Test Sets](../task/create-test-set.md) module to create a test set and group related tests into that test set.

</td></tr><tr><td>

Test plan

</td><td>

Plan describing how a product or a feature is to be tested and the time frame in which it must be executed. A test plan can be further broken into test cycles, and test cycles into test execution suites.You can use the [Test Plans](../task/create-test-plan.md#) module to create test plans.

</td></tr><tr><td>

Test cycle

</td><td>

A subdivision of a test plan that represents a phase or iteration of testing, such as a regression cycle or a sprint cycle. A test plan can contain multiple test cycles, and each test cycle can be further divided into test execution suites. Use the Planning tab on the Test Board to create and manage test cycles.

</td></tr><tr><td>

Test case

</td><td>

A collection of related tests. A test case is saved as part of a test suite and can be added to a test plan. Each test case within a test plan has an assigned tester.

</td></tr><tr><td>

Runs

</td><td>

Detailed report of tests results, such as start time and end time of test execution, environment details, result of test execution.You can use the Run module to view the test results.

</td></tr></tbody>
</table>## Getting started with Test Management 2.0

1.  Activate the Test Management 2.0 plugin. For more information, see [Activate Test Management 2.0](../task/activate-test-management2.md).
2.  Create your first test. For more information, see [Create a test in Test Management 2.0](../task/create-test2.md).
3.  Create a test set to organize related tests. For more information, see [Create a test set in Test Management 2.0](../task/create-test-set.md).
4.  Create a test plan and assign tests to testers. For more information, see [Create a test plan using Test Board in Test Management 2.0](../task/create-test-plan.md#).
5.  Run your assigned tests. For more information, see [Run your test assignments in Test Management 2.0](../task/run-your-test-assignments.md).

**Parent Topic:**[Test Management 2.0](../reference/test-management2-landing-page.md)

