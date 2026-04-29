---
title: Test suite results record
description: The Test Suite Results record displays information about the results of one execution of one test suite.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Suite results, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Test suite results record

The Test Suite Results record displays information about the results of one execution of one test suite.

<table><thead><tr><th>

Field / Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start Time

</td><td>

\(Appears in list of records, but not on default record form\). The time this test suite started.

</td></tr><tr><td>

Test Suite

</td><td>

The test suite that was run.

</td></tr><tr><td>

Number

</td><td>

Unique ID for this test suite results record.

</td></tr><tr><td>

Base Test Suite Result

</td><td>

If this test suite is a child in a hierarchy of test suites, the base test suite result is the unique ID of the result record for the suite at the top-most level of the hierarchy. For more information, see [Example: Base test suite result](atf-rollup-xmpls.md#pfg_d1f_5w).

</td></tr><tr><td>

Parent

</td><td>

If this test suite has a parent, this is the test result record for the parent suite. For more information, see [Example: Parent test suite results](atf-rollup-xmpls.md#ulw_p1f_5w).

</td></tr><tr><td>

Status

</td><td>

Result of the test or test suite execution:-   Canceled – user canceled the test or test suite run.
-   Error – an error occurred in the test framework. For example, the test runner halted or the server encountered an unintended scenario. The error message appears in the summary field of the Step Results form for the test step that contains the error.
-   Failure – test, test suite run, or test step failed due to an error.
-   Ignored – test step passed but contains client-side JavaScript errors entered into the Allowed Browser Error table with report level of Ignored.
-   Running – test or test suite is running.
-   Skipped – occurs if an earlier test in the suite failed and **Abort on failure** is set to **true**.
-   Success – test, test suite, or test step run passed.
-   Success with warning\(s\) – test or test suite run passed but contains a test step with client-side JavaScript errors entered into the Allowed Browser Error table with report level of Warning.
-   Waiting – test or suite run is waited to start.
-   Warning – test or suite contains client-side JavaScript errors entered into the Allowed Browser Error table with report level of Warning.

</td></tr><tr><td>

Run time

</td><td>

The duration it took to execute this test suite.

</td></tr><tr><td>

Retain indefinitely

</td><td>

Check box to keep this record even after the specified data retention period has passed. For more information, see [Table Cleanup](../concept/table-cleanup.md).

</td></tr><tr><td>

Rolled up test success count

</td><td>

How many tests were successful. The tests counted as part of the roll up are all tests included in this suite, plus all others included in suites that are descendents of this one. For more information, see [Rolled up counts for test suites results](atf-rollup-xmpls.md#twp_tcf_5w).

</td></tr><tr><td>

Rolled up test failure count

</td><td>

How many tests failed. The tests counted as part of the roll up are all tests included in this suite, plus all others included in suites that are descendents of this one. For more information, see [Rolled up counts for test suites results](atf-rollup-xmpls.md#twp_tcf_5w).

</td></tr><tr><td>

Rolled up test error count

</td><td>

How many tests resulted in an error. The tests counted as part of the roll up are all tests included in this suite, plus all others included in suites that are descendents of this one. For more information, see [Rolled up counts for test suites results](atf-rollup-xmpls.md#twp_tcf_5w).

</td></tr><tr><td>

Rolled up test skip account

</td><td>

How many tests were skipped. The tests counted as part of the roll up are all tests included in this suite, plus all others included in suites that are descendents of this one. For more information, see [Rolled up counts for test suites results](atf-rollup-xmpls.md#twp_tcf_5w).

</td></tr><tr><td>

Test Results \(related list\)

</td><td>

Results of the individual tests included in this test suite.

</td></tr><tr><td>

Child Test Suites Results \(related list\)

</td><td>

The results of any test suites that are children of this test suite.

</td></tr><tr><td>

All Test Suite Results \(related list\)

</td><td>

Results from this test suite and all descendent test suites.

</td></tr><tr><td>

Failed Tests in Suite \(related list\)

</td><td>

Results from any failed tests included in this test suite.

</td></tr><tr><td>

Previous suite result

</td><td>

Only appears if this suite result is for a re-run of failed tests and you are logged on with the atf\_test\_admin, atf\_test\_designer, or admin role. Click the information icon to navigate to the "original" suite result record. ![Previous suite test result](../image/atf-prev-suite-results.png)

</td></tr></tbody>
</table>**Parent Topic:**[Suite results](../concept/suite-results-module.md)

**Related topics**  


[Test results](../concept/atf-test-results-module.md)

