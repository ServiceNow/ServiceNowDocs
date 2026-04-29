---
title: Parallel testing
description: Reduce test design time by running multiple tests and test suites in parallel. Design tests to run in parallel by avoiding resource conflicts and data dependencies.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Automated Test Framework \(ATF\) test types and techniques, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Parallel testing

Reduce test design time by running multiple tests and test suites in parallel. Design tests to run in parallel by avoiding resource conflicts and data dependencies.

**Note:** If two or more users are developing tests simultaneously, parallel testing reduces test design time. After test design completes, it is recommended to organize tests into a single hierarchical suite structure, and run the tests as a single base suite.

## Parallel testing limit

Parallel testing enables users to run multiple automated tests simultaneously. This process continues until the number of parallel running tests is as per the following formula.

```
Number of parallel tests = max(1, number of worker threads - 2)
```

**Note:** If your instance has 2 or less worker threads, configuration improvements review is recommended.

The actual number of parallel tests that a non-production instance can support depends on the system resources that the instance has when it is provisioned. The parallel testing limit ensures that an instance always has system resources available for other non-testing tasks.

## Test waiting queue

When the system reaches the parallel testing limit, it reschedules tests to run later. It automatically places the tests back in sys\_trigger until a worker thread is available to pick them up. Each test in the waiting queue has a schedule the next time the test runs.

## Design considerations

Run multiple tests and test suites in parallel to reduce test design time. Avoid resource conflicts and data dependencies by designing parallel running tests. Avoid resource conflicts and data dependencies by designing tests that rely only on newly generated or self-created data, or have mutual exclusion rules defined between tests that share resources.

**Prevent resource conflicts between parallel tests**

Prevent resource conflicts by running tests that create their own data. Tests that run with existing data prevent other tests that need the same data from running in parallel.

**Note:** If you have two or more tests with resource conflicts, see [Mark tests as mutually exclusive](mutual-exclusion-rule.md#section_egk_ztm_thb) to create a mutual exclusion rule that prevents the tests from running in parallel.

**Parent Topic:**[Automated Test Framework \(ATF\) test types and techniques](atf-test-type-testing.md)

**Related topics**  


[Reusable tests](atf-reuse-tests.md)

[Mutually exclusive tests](mutual-exclusion-rule.md)

[Quick start tests](quick-start-tests.md)

[Accelerate ATF tests failure resolution](../task/atf-test-triage.md)

[Performance profiling](atf-perf-prof.md#)

