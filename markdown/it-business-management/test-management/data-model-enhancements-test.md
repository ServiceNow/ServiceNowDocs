---
title: Data model enhancements in Test Management 2.0
description: Test Management 2.0 offers a few data model enhancements over Test Management 1.0.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/test-management/data-model-enhancements-test.html
release: australia
product: Test Management
classification: test-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Appendix — Test Management 2.0, Migration from Test Management 1.0 to Test Management 2.0, Test Management applications, Strategic Portfolio Management]
---

# Data model enhancements in Test Management 2.0

Test Management 2.0 offers a few data model enhancements over Test Management 1.0.

## Enhanced traceability

Each test in Test Management 2.0 can have multiple versions. When a test version is in the state Ready, it can be run but cannot be edited. Every test result is associated with a specific run and a specific version of the test. Due to this logic, you can always be sure of the content of the test when a specific test result was received.\[Omitted image "test\_data\_model.png"\] Alt text: Illustration showing multiple versions of a test

## More flexible approach to organize tests

Unlike Test Management 1.0, where test cases can be placed in only one test suite, in Test Management 2.0 tests can be placed in multiple test sets. Test sets are free-form collections of tests. Tests can be grouped into test sets using any logic: by product, by component, or by release.

\[Omitted image "test\_sets.png"\] Alt text: Illustration showing that test set is a collection of tests

## Test plan defines the time frame

A test plan in Test Management 2.0 captures the time frame during which the tests are to be run. In addition, a test plan can be broken down into smaller planning windows, test cycles, for more precise planning, such as user acceptance testing, and integration testing. Further test cycles can be broken down into test execution suites, which are similar to sprints in testing. A test execution suite defines when a test must be run and by whom.\[Omitted image "test\_plan.png"\] Alt text: Illustration showing that a test plan is broken down into test cycles and test execution suites

