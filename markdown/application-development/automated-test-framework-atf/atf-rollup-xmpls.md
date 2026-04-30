---
title: Test suite results examples
description: Examples of relationship terms and how aggregated results roll up for test suites.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Suite results, Automated Test Framework reference, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Test suite results examples

Examples of relationship terms and how aggregated results roll up for test suites.

## Example: Base test suite result

The base test suite is the top-level test suite in the hierarchy. For example, if you are viewing the test suite results record for \(A\) Test Suite 1.3.1, the **base test suite result** field links to the test suite results record for \(B\) Test Suite 1.

![Example: Base test suite result](../image/test-suite-hierarchy_base.png)

## Example: Parent test suite results

The parent test suite is the test suite immediately above the one you are currently viewing. For example, ff you are viewing the test suite results record for \(A\) Test Suite 1.3.1, the **parent** field links to the test suite results record for \(B\) Test Suite 1.3.

![Example: Parent test suite results](../image/test-suite-hierarchy-parent.png)

## Rolled up counts for test suites results

You can view rolled up counts for a test suite for four metrics: test successes, failures, errors, and skips. Each of these sum data from all tests in the test suite plus all tests in the test suite's descendents.

For example, if you are viewing the test suite results record for \(A\) Test Suite 1.3.1, the **Rolled up test success count** field shows the total number of successes counting results from all the tests represented by boxes labeled A.

If you are viewing the test suite results record for \(B\) Test Suite 1.3.1, the **Rolled up test success count** field shows the total number of successes counting results from all the tests represented by boxes labeled B.

![Rolled up counts for test suites results](../image/test-suite-rollup-success.png)

## Child Test Suites Results

If you are viewing the test suite results record for \(A\) Test Suite 1, the **Child Test Suites Results** related list shows result records for Test Suite 1.3 \(B\).

![Rolled up counts for test suites results](../image/test-suite-hierarchy-child.png)

## All Test Suites Results

If you are viewing the test suite results record for \(A\) Test Suite 1, the **All Suites Results** related list shows result records for all Test Suites represented by boxes labeled A

If you are viewing the test suite results record for \(B\) Test Suite 1.3, the **All Suites Results** related list shows result records for all Test Suite 1.3.1 only \(represented by the box labeled B\)

![Child Test Suites Results](../image/test-suite-hierarchy-all-suites.png)

**Parent Topic:**[Suite results](../concept/suite-results-module.md)

