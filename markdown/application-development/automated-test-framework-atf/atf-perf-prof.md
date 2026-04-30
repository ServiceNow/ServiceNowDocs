---
title: Performance profiling
description: Performance profiling allows you to do performance testing on your instances.Execute performance profiling on a test or a suite for performance testing on your instance. You can also detect performance degradation when you upgrade your instance and then investigate and fix the issues.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Test types and techniques, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Performance profiling

Performance profiling allows you to do performance testing on your instances.

Apart from being a functional testing medium that ensures nothing breaks when any changes are made to an instance, ATF can also detect performance degradation during upgrades. You can know the cause, investigate, and fix the performance issue.

You can execute performance profiling on any of your ATF tests or suites. For each test or suite, the default test run is 10. In a suite, each test runs 10 times sequentially. The first run is a warmup that helps in warming up the cache values and is not counted to the 10 test runs of a test or suite.

**Note:** Performance profiling can’t be done on more than 1 test simultaneously. It doesn’t support parallel performance assessment.

![Running a performance test](../image/atf-10-runs.png)

**Note:** When you execute a performance test run, the system pauses and waits for any ongoing jobs to finish before starting the test run. This helps in avoiding any slowdown of your instance.

**Parent Topic:**[Automated Test Framework \(ATF\) test types and techniques](atf-test-type-testing.md)

**Related topics**  


[Reusable tests](atf-reuse-tests.md)

[Mutually exclusive tests](mutual-exclusion-rule.md)

[Quick start tests](quick-start-tests.md)

[Parallel testing](parallel-testing.md)

[Accelerate ATF tests failure resolution](../task/atf-test-triage.md)

## Execute performance profiling

Execute performance profiling on a test or a suite for performance testing on your instance. You can also detect performance degradation when you upgrade your instance and then investigate and fix the issues.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Test**.

    **Note:** You can also select the Suites module if you want to execute performance profiling on a suite.

    A list of tests or suites shows up.

2.  Select the test you want to execute performance profiling on.

3.  Select **Run Performance Test** on the Test form.

    A **Run Test** modal shows up. The modal shows the warmup run and all the 10 test runs of the selected test or suite. You can track all the test runs as they start executing.

    **Note:** You can select **Run Performance Suite** if you have selected a suite for performance profiling.

4.  Scroll down and select the **Performance Test Results** related list.

5.  Select the required performance number to view the results of all the test runs within the selected performance test.

    The Performance Run form shows up. You can also directly navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Test** &gt; **Performance Profiling** &gt; **Performance Runs** to see the Performance Run form. Add a screenshot

    **Note:** You can view the test name, status of the test runs, and the duration of the test run. If the **Is warmup** value is true, its the first test run that is done to warmup the cache values. The rest of the test runs will have **Is warmup** value set to false. The warmup test is not counted as one of the 10 test runs for each test or suite.

6.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Test** &gt; **Performance Profiling** &gt; **Performance Comparisons**.

    The Performance Comparisons form shows up. &lt;add a screenshot of the form&gt;

7.  Select the first and second run to view a comparison result.

    Add the complete screenshot. You can view information like performance means and the delta mean values.

    **Note:** You can compare only 2 test runs at one point of time. In the next comparison, you can consider one of the previous test run as the baseline to compare with the next test run.


