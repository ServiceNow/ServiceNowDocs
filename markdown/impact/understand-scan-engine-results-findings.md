---
title: Understand scan results and findings
description: After a scan runs, you can monitor its progress in real-time, review the completed results, and then work with the findings it identifies to resolve issues in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/understand-scan-engine-results-findings.html
release: australia
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 3
keywords: [scan results, scan findings, platform health]
breadcrumb: [Diagnose technical debt, Platform Health, Using Impact, Impact]
---

# Understand scan results and findings

After a scan runs, you can monitor its progress in real-time, review the completed results, and then work with the findings it identifies to resolve issues in your instance.

Reviewing scan results and acting on findings is a two-phase process.

1.  View scan results: Monitor an active scan or open a completed scan record to see its status, duration, and batch progress. See [View scan results for Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/viewing-scan-results-scan-engine.md).
2.  Work with findings: Open individual findings from the scan record to understand their enforcement level and impact, then apply fixes or submit exceptions for review. See [Work with Scan Engine findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/work-with-scan-engine-findings.md).

## How findings are evaluated

Every finding in your instance is evaluated along two critical dimensions to help your team prioritize remediation efforts and maintain compliance standards.

-   **Level of finding \(enforcement level\)**

    The enforcement behavior is determined whether the system blocks an action, issues a warning, or provides informational guidance. Enforcement levels are ACT, RECOMMEND, SUGGEST, and REVIEW. The enforcement level determines the action the system will take and whether exceptions are available.

-   **Impact to instance \(risk rating\)**

    The business and technical risk of leaving the finding unresolved, rated from 1 \(minimal\) to 10 \(critical\) within each enforcement level. Higher values indicate findings that should be addressed first within that level.

    Impact ratings operate independently within each enforcement level and do not create a global 1–10 scale across all levels.


These two dimensions work together, enforcement level determines what action is required, while impact rating determines the order in which findings should be addressed within that enforcement level. For full details, see [Work with Scan Engine findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/work-with-scan-engine-findings.md).

## Enforcement levels and risk impact

<table id="table_scan_findings"><thead><tr><th>

Level of finding

</th><th>

Impact to instance \(typical\)

</th><th>

Severity description

</th><th>

Enforcement behavior / recommended action

</th></tr></thead><tbody><tr><td>

ACT

</td><td>

1–10

</td><td>

Critical issues that can break functionality, cause security vulnerabilities, or block upgrades.

</td><td>

-   The record can not be saved until the code is fixed to meet the requirements in the definition.
-   No exception reason option is available.
-   An override requires admin-level rights or the disabling of the definition.

</td></tr><tr><td>

RECOMMEND

</td><td>

1-10

</td><td>

High severity issues that may degrade performance, stability, or security. Exceptions are allowed with approval.

</td><td>

-   The record can not be saved until the issue is resolved or and exception reason is provided formal approval.
-   For more information, refer to [Submit exceptions for Scan Engine findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/submitting-exception-reasons-scan-engine.md).

</td></tr><tr><td>

SUGGEST

</td><td>

1-10

</td><td>

Moderate issues, often related to optimization, maintainability, or best practices.

</td><td>

-   Address during future development cycle
-   Does not block progress
-   Prompts to check for a better solution, if one is available.

</td></tr><tr><td>

REVIEW

</td><td>

1-10

</td><td>

Low impact, informational findings with minimal impact \(e.g., unused fields or minor UI inconsistencies\).

</td><td>

Monitor and optionally fix during future development cycles.

</td></tr></tbody>
</table>**Important:** Impact rating applies independently to each enforcement level. An ACT 1 finding is always higher priority than a recommend 10 level finding, even though the numbers appear reversed.

Enforcement level takes precedence over impact rating in prioritization. The 1–10 scale within each level allows granular severity differentiation while maintaining the enforcement hierarchy.

## Examples

These two metrics work together to help teams balance enforcement and risk prioritization, ensuring critical issues are addressed first while maintaining development velocity.

-   ACT level finding with impact to instance of 9: Critical and must be fixed immediately before proceeding. No exceptions.
-   SUGGEST level with impact to instance of 8: High-risk but does not block development. Should still be prioritized for remediation.

**Related topics**  


[View scan results for Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/viewing-scan-results-scan-engine.md)

[Work with Scan Engine findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/work-with-scan-engine-findings.md)

