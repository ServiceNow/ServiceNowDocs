---
title: Mutually exclusive tests
description: Prevent conflicting tests from running in parallel by marking them as mutually exclusive. For example, when the system identifies tests that modify the same record, the system makes these tests mutually exclusive. You can also manually mark tests as mutually exclusive.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Test types and techniques, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Mutually exclusive tests

Prevent conflicting tests from running in parallel by marking them as mutually exclusive. For example, when the system identifies tests that modify the same record, the system makes these tests mutually exclusive. You can also manually mark tests as mutually exclusive.

The system marks tests as mutually exclusive when there is a potential resource conflict. When the system can't detect resource conflicts automatically, you can create your own mutual exclusion rules that can prevent conflicting tests from running in parallel. For example, if a test changes a sys\_properties record, the record shows up under **Records Modified** of that test. If the validation path of another test depends on the same sys\_properties record without any change, that test fails. This can occur if the previous test runs at the same time.

You can view mutually exclusive tests on the Mutually Exclusive Tests related list in the test form. This related list shows all tests that don't run in parallel with the current test and the reason. The same test might appear more than once in the list if there are multiple reasons.

## Mutually exclusive tests reasons

Tests are marked mutually exclusive for the following reasons.

-   Two or more tests modify the same record.
-   A test that runs in parallel with itself.
-   You can create your own mutual exclusion rules when the system can’t detect resource conflicts automatically.

## Mark tests as mutually exclusive

You can mark tests as mutually exclusive using any of the following methods.

-   **Mutually Exclusive Tests tab**

    Select a test from the Tests list and navigate to **Mutually Exclusive Tests** &gt; **Add Mutual Exclusion** to make the selected test mutually exclusive with another test.

-   **Tests list**

    Select one or more tests from the Tests list and choose **Add mutually exclusive test** from the Action on selected rows context menu. Enter one test in the Add mutually exclusive test dialog box to make the selected tests mutually exclusive with the current test.

-   **Parallel Test Runs tab**

    When two or more tests run in parallel, navigate to **Test Results** &gt; **Parallel Test Runs**. Select one or more tests and choose **Add mutually exclusive test** from the Action on selected rows context menu to mark the selected tests as mutually exclusive.

    **Note:** The **Parallel Test Runs** tab is visible only if the test runs in parallel with one or more tests.


**Parent Topic:**[Automated Test Framework \(ATF\) test types and techniques](atf-test-type-testing.md)

**Related topics**  


[Reusable tests](atf-reuse-tests.md)

[Quick start tests](quick-start-tests.md)

[Parallel testing](parallel-testing.md)

[Accelerate ATF tests failure resolution](../task/atf-test-triage.md)

[Performance profiling](atf-perf-prof.md#)

