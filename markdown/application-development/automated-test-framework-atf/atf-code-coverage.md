---
title: ATF Code Coverage
description: Metadata code coverage tracks which lines of code in your custom scripts are executed during ATF test runs. It helps identify untested code, validate test quality, and assess deployment risk in ReleaseOps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/atf-code-coverage.html
release: brazil
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-09-14"
reading_time_minutes: 4
breadcrumb: [Administering the Automated Test Framework \(ATF\), Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# ATF Code Coverage

Metadata code coverage tracks which lines of code in your custom scripts are executed during ATF test runs. It helps identify untested code, validate test quality, and assess deployment risk in ReleaseOps.

Metadata code coverage is a testing and quality assurance feature that automatically collects and analyzes code coverage data when running ATF tests. It provides visibility into:

-   Which lines of code in your scripts execute during test runs
-   Code coverage percentages at the script level and deployment level
-   Gaps in test coverage across your custom code
-   Integration with test triage and test result analysis

## Supported Code Scopes

Metadata code coverage can track code execution in the following scopes:

-   Server-side scripts: Business rules, script includes, workflow activities, and other server-side code written in Rhino JavaScript
-   Client-side scripts: Client scripts, UI policies, and other client-side code executed in the browser
-   Global scope code: Custom global scope scripts and libraries
-   Application-scoped code: Code within specific application scopes can be filtered and analyzed separately

## Key Concepts

Line coverage tracks whether individual lines of code in a script were executed during a test run. Line-level granularity helps identify which specific code paths are exercised by your tests.

Coverage aggregation combines coverage data from multiple test runs to show cumulative coverage at the test, test suite, script, and deployment levels.

Traced records are captured during test execution with code coverage enabled. The system records which table records and metadata attributes are accessed by your scripts. This tracing data is linked to coverage records for detailed analysis.

Test result integration captures code coverage metrics at the test, test suite, and test result levels, allowing you to correlate test outcomes with the code paths they exercise.

## Use Cases

Test quality assessment uses code coverage data to identify critical code paths that lack test coverage and prioritize writing additional tests for those areas.

Deployment risk analysis reviews code coverage data before deploying custom code changes to verify the modified code is adequately tested. Low coverage on recently changed code indicates higher deployment risk.

Test triage and troubleshooting uses code coverage data to support the Test Triage feature. This feature helps identify why tests fail by showing which code paths were exercised and which metadata was modified.

Deployment request assessment in ReleaseOps automatically evaluates code coverage as part of the deployment request assessment process. By default, if custom code coverage is below 70%, the deployment request transitions to the Reconciling state and a test failure task is created.

## Deployment Coverage Threshold

Metadata code coverage integrates with ReleaseOps deployment assessment. By default, if custom code in a deployment request has less than 70% ATF test coverage, the following occurs:

-   The deployment request transitions to the `Reconciling` state
-   A test failure task is automatically created
-   Deployment is blocked pending review and potential remediation

You can adjust the coverage threshold in the deployment request assessment playbook. See [Set Automated Test Framework \(ATF\) code coverage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/releaseops/set-atf-code-coverage-threshold.md) for configuration details.

## Limitations and Considerations

When working with metadata code coverage, be aware of the following:

-   Code coverage collection may impact test performance. The system includes thresholds to prevent excessive data accumulation.
-   Code coverage can be disabled globally or at the script level if performance becomes a concern.
-   Data truncation: Large API request payloads may be truncated when persisted. By default, fields are limited to 4,000 characters. When truncation occurs, a `was_truncated` flag is set to `true` in the API response, with details provided in the `truncation_message` field. You can adjust the default limit using the `glide.db.truncate_utf8` system property.
-   Coverage data is subject to database field length constraints. Fields affected include test\_suite\_results, test\_results, and metadata\_info JSON arrays.
-   Code coverage only includes code executed by the server-side Rhino engine or browser; static metadata, configurations, and non-executable records are not covered.
-   When tracing is interrupted due to threshold constraints, an indicator is recorded on the test result to show that coverage data is incomplete.

## Availability

Metadata code coverage is available starting with the Australia release.

## Programmatic Access

You can retrieve and analyze code coverage data programmatically using the ATF Code Coverage REST API. The API provides three main endpoints for computing code coverage:

-   `POST /api/now/atf/code_coverage/all` — Aggregates coverage across all scripts covered by specified test suite or test runs
-   `POST /api/now/atf/code_coverage/by_script_id` — Computes coverage for specific script records
-   `POST /api/now/atf/code_coverage/by_line_number` — Computes coverage using filtered line numbers per metadata record

Each endpoint returns coverage percentages at the script and deployment levels, along with metadata about the request and any data truncation warnings. For detailed API specifications, parameter documentation, and code examples, see [ATF Code Coverage API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/atf-code-coverage-api.md).

## Related Features

-   Automated Test Framework \(ATF\): The testing framework that generates code coverage data during test execution
-   Test Triage: Analyzes test failures using code coverage and metadata tracing to identify root causes
-   ReleaseOps: Integrates code coverage assessment into deployment request workflows
-   Deployment Analyzer: Uses code coverage data to assess deployment readiness and risk

**Parent Topic:**[Administering the Automated Test Framework \(ATF\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/automated-test-framework-atf/atf-admin-overview.md)

