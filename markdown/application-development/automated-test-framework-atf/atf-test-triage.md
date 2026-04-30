---
title: Accelerate ATF tests failure resolution
description: Resolve ATF test failures faster using the actionable support provided by the new ATF failure insights feature. You can achieve it by accessing the Find changes since last successful run related link.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Test types and techniques, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Accelerate ATF tests failure resolution

Resolve ATF test failures faster using the actionable support provided by the new ATF failure insights feature. You can achieve it by accessing the Find changes since last successful run related link.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Tests**.

    A list of ATF tests shows up.

2.  Select the test you want to debug.

    The selected test form shows up.

3.  Select the Test Results related list.

    The list of last few execution results of the selected test shows up. If the test has never been executed, you don't see any test results. You can then execute the test to generate results.

4.  Select one of the failed results to see what has changed since the last successful run of the test.

    The Test Results form of the selected result shows up.

5.  Select the Find changes since last successful run related link.

    **Note:** This related link is visible only when you open a failed test result.

    The What changed related list shows up.

    **Note:** The What changed related list shows up only if you have metadata records that have changed in between the last successful run and the recent failure. It gives a better insight into what specific records could have caused the failure.

    You might experience a delayed update in the records in the What changed related list. If you still don't see the desired results, it is recommended to try selecting the Find changes since last successful run related link again.

6.  Implement one of the following ways to compare the results.

    -   Right-click on one of the changed files listed under the What changed related list. Select **Comparison** to see the changes since the last successful run.
    -   Select and open the changed file itself and select **Comparison** on the What changed form.

        **Note:** A screen showing the comparison between the 2 versions of the selected file shows up. It shows the exact changes made to the file. The left hand side is the most recent version of the record.

    -   Go to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Test Results**. Select any 2 tests and compare results by selecting the action.
7.  Select **Create a task** on the Test Results form if you want to create a task for a changed file.

    You will have to select at least 1 changed file to create a task for. Certain information about the changed record are auto-filled.

    **Note:** By default, the task created is an incident task type. This is determined by the sn\_atf.test.triage.task.type property. It creates the task type depending on the task table you have assigned the task to.

    If you select more than 1 changed file while creating a task, it still creates just 1 task for the multiple files.


-   **[Metadata exception list](../concept/atf-metadata-exception-triage.md)**  
The following list of tables are not supported by the ATF tests failure resolution feature.

**Parent Topic:**[Automated Test Framework \(ATF\) test types and techniques](../concept/atf-test-type-testing.md)

**Related topics**  


[Reusable tests](../concept/atf-reuse-tests.md)

[Mutually exclusive tests](../concept/mutual-exclusion-rule.md)

[Quick start tests](../concept/quick-start-tests.md)

[Parallel testing](../concept/parallel-testing.md)

[Performance profiling](../concept/atf-perf-prof.md#)

