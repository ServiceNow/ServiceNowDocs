---
title: Test Management applications
description: The ServiceNow Test Management application streamlines the management of testing processes to help you deliver software products more efficiently and with fewer errors.
locale: en-US
release: australia
product: Test Management
classification: test-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Strategic Portfolio Management]
---

# Test Management applications

The ServiceNow® Test Management application streamlines the management of testing processes to help you deliver software products more efficiently and with fewer errors.

Test Management is available in two versions.

-   Test Management 2.0 offers many enhancements, including integration with Agile Development 2.0 and Scaled Agile Framework \(SAFe\)
-   Test Management 1.0 may have specific capabilities that are useful for your organization.

Use the following comparison to make an informed decision for your organization.

## Differences between Test Management 1.0 and Test Management 2.0

Test Management 1.0 covers user acceptance testing. It does not include some key data model structures like test versions, test runs, or test results. In addition, you cannot structure test plans in Test Management 1.0.

Test Management 2.0 includes data model structures that match industry standards. It provides you with an intuitive user interface called the [Test Board](test-board.md) from which you can structure test plans and plan the phases of your testing effort.

**Tip:**

If you need Agile Development integration, test versioning, or detailed test run traceability, use Test Management 2.0. If your organization requires only basic user acceptance testing without Agile integration, Test Management 1.0 may be sufficient.

<table id="table_test_differences"><thead><tr><th>

Feature

</th><th>

Test Management 1.0

</th><th>

Test Management 2.0

</th></tr></thead><tbody><tr><td>

Integration with Project Portfolio Management

</td><td>

no

</td><td>

yes

</td></tr><tr><td>

Integration with Agile Development 2.0

</td><td>

no

</td><td>

yes

</td></tr><tr><td>

Integration with Scaled Agile Framework \(SAFe\)

</td><td>

no

</td><td>

yes

</td></tr><tr><td>

Test version

</td><td>

You cannot create and maintain multiple versions of a test.

</td><td>

You can create and maintain multiple versions of a test.

</td></tr><tr><td>

Test relation

</td><td>

You can associate a test to one test suite only.

</td><td>

You can associate a test to multiple test sets, test plans, and test cycles.

</td></tr><tr><td>

Time duration

</td><td>

You can create a test plan describing how a product or a feature is to be tested.

</td><td>

-   You can create a test plan describing how a product or a feature is to be tested and the time frame in which the test plan must be run.
-   You can further decompose a test plan into test cycles, test cycles into test execution sets, and specify a time range for their execution.

</td></tr><tr><td>

Traceability of test runs and test results

</td><td>

You can: -   run a single test at a time.
-   view the test result.

</td><td>

You can:-   run a single test at a time.
-   view which version of test has been run.
-   view the test result.

</td></tr></tbody>
</table>**Note:**

-   If you are an existing Test Management user on a release prior to London, you are using Test Management 1.0 activated through the Test Management \(com.snc.test\_mgmt\) plugin. See the [Test Management 1.0](../../test-management/concept/c_TestManagement.md) documentation for more information.
-   If you are a new user, you can activate the Test Management 2.0 \(com.snc.test\_management.2.0\) plugin as it provides enhanced testing capabilities. See the [Test Management 2.0](test-management-overview.md#)documentation for more information.

-   **[Domain separation and Test Management](../../test-management/concept/domain-separation-test-management.md)**  
Domain separation is supported in Test Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Test Management 1.0](../../test-management/concept/c_TestManagement.md)**  
The ServiceNow® Test Management 1.0 application provides a tool for manual software testing.
-   **[Test Management 2.0](../reference/test-management2-landing-page.md)**  
The ServiceNow® Test Management 2.0 application streamlines the management of testing processes to help you deliver software products more efficiently and with fewer errors. You can create multiple versions of a test and integrate with Agile Development 2.0.
-   **[Migration from Test Management 1.0 to Test Management 2.0](../task/migrate-test.md)**  
Migrate your test data from Test Management 1.0 to Test Management 2.0, and start using Test Management 2.0 for its enhanced testing capabilities and features.

**Parent Topic:**[Strategic Portfolio Management](../../it-business-management/reference/r_ITBusinessManagement.md)

