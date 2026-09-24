---
title: Understand scan results and findings
description: After a scan runs, you can monitor its progress in real-time, review the completed results, and then work with the findings to resolve issues in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/understand-scan-engine-results-findings.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [scan results, scan findings, platform health]
breadcrumb: [Prevent and resolve technical debt with AI, Platform Health, Using Impact, Impact]
---

# Understand scan results and findings

After a scan runs, you can monitor its progress in real-time, review the completed results, and then work with the findings to resolve issues in your instance.

Reviewing scan results and acting on findings is a two-phase process.

1.  View scan results: Monitor an active scan or open a completed scan record to see its status, duration, and batch progress. See [View scan results for Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/viewing-scan-results-scan-engine.md).
2.  Work with findings: Open individual findings from the scan record to understand their enforcement level and impact, then apply fixes or submit exceptions for review. See [Use Real-time prevention monitoring while coding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/real-time-prevention-monitoring.md).

## How findings are evaluated

Every finding in your instance is evaluated along two critical dimensions to help your team prioritize remediation efforts and maintain compliance standards.

-   **Level of finding \(enforcement level\)**

    The enforcement behavior is determined whether the system blocks an action, issues a warning, or provides informational guidance. Enforcement levels are ACT, RECOMMEND, SUGGEST, and REVIEW. The enforcement level determines the action the system will take and whether exceptions are available.

-   **Impact to instance \(risk rating\)**

    The business and technical risk of leaving the finding unresolved, rated from 1 \(minimal\) to 10 \(critical\) within each enforcement level. Higher values indicate findings that should be addressed first within that level.

    Impact ratings operate independently within each enforcement level and don't create a global 1–10 scale across all levels.


These two dimensions work together, enforcement level determines what action is required, while impact rating determines the order in which findings should be addressed within that enforcement level.

## Enforcement levels and risk impact

Depending on the level of the definition, users may be required to fix a finding before saving a record.

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

-   The record can't be saved until the code is fixed to meet the requirements in the definition.
-   No exception reason option is available.
-   An override requires admin-level rights or the disabling of the definition.

</td></tr><tr><td>

RECOMMEND

</td><td>

1-10

</td><td>

High severity issues that may degrade performance, stability, or security. Exceptions are allowed with approval.

</td><td>

-   The record can't be saved until the issue is resolved or and exception reason is provided formal approval.
-   For more information, refer to [Submit exceptions for Scan Engine findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/submitting-exception-reasons-scan-engine.md).

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
-   Select whether to Exclude suggestion finding, which hides Suggestion level findings messages from displaying.

</td></tr><tr><td>

REVIEW

</td><td>

1-10

</td><td>

Low impact, informational findings with minimal impact \(i.e., unused fields or minor UI inconsistencies\).

</td><td>

-   Monitor and optionally fix during future development cycles.
-   Displays an informational message without blocking saves or creating finding records.

</td></tr></tbody>
</table>**Important:** Impact rating applies independently to each enforcement level. An ACT 1 finding is always higher priority than a recommend 10 level finding, even though the numbers appear reversed.

Enforcement level takes precedence over impact rating in prioritization. The 1–10 scale within each level allows granular severity differentiation while maintaining the enforcement hierarchy.

## Examples

These two metrics work together to help teams balance enforcement and risk prioritization, ensuring critical issues are addressed first while maintaining development velocity.

-   ACT level finding with impact to instance of 9: Critical and must be fixed immediately before proceeding. No exceptions.
-   SUGGEST level with impact to instance of 8: High-risk but does not block development. Should still be prioritized for remediation.

## Finding record fields

When you open a finding record from a scan result, the record displays several key fields that provide context and tracking information about the finding.

**Note:** To view the actual findings, navigate to **ALL &gt; Impact &gt; Platform Health &gt; Open Findings**.

\[Omitted image "remediation-dev-open-findings.png"\] Alt text: Findings table.

|Column|Description|
|------|-----------|
|Application|The application scope containing the scanned record where the finding was detected.|
|Description|The scan definition violation that was detected.|
|Category|The category of the finding, such as Performance or Security. See [Customize Scan Engine definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/view-modify-scan-engine-properties.md) for details.|
|Finding counts|The number of times this finding was detected across scanned records in the application.|
|Impact to instance|A color-coded severity indicator showing the potential impact level. Higher numbers indicate greater severity.|
|Total technical debt \(time\)|The estimated time required to resolve the finding.|
|Fix status|The current remediation state of the finding. Values include Not requested, Not applicable, Ready for review, Reviewed, Revised, Processing, and Error.|

<table id="table_finding_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scanned Record URL/Application

</td><td>

-   A direct link to the record in your instance that triggered this finding during the scan.
-   Select to navigate directly to the record and review the code, configuration, or content that generated the finding.
-   Essential for explaing the context of the issue.

</td></tr><tr><td>

Description

</td><td>

The description of the definition that triggered the finding

</td></tr><tr><td>

Introduced by

</td><td>

-   The user, system process, or update set that created or last modified the record being scanned.
-   Use to track ownership and identify patterns in findings across your team. Helps with root-cause analysis and accountability.

</td></tr><tr><td>

Exception Reason

</td><td>

-   When an exception is submitted for a RECOMMEND level finding, this field captures the business justification or context for the exception request.
-   Visible only when an exception is in progress or has been approved. Provides transparency to approvers and team members reviewing the exception.

</td></tr><tr><td>

Assigned group

</td><td>

-   The team group to which the finding was automatically assigned when detected. Use to identify which team is responsible for remediating this finding.
-   The assigned group is set automatically at detection time by the assignment rule engine and cannot be changed by editing this field directly.

</td></tr><tr><td>

Assignment source

</td><td>

-   Records which rule or fallback tier resolved the assignment for this finding, including the rule name and a timestamp.
-   Use to audit why a finding was routed to a specific group. The value identifies the Decision Table rule that fired, or the fallback tier that resolved the assignment when no rule matched.

</td></tr></tbody>
</table>**Related topics**  


[View scan results for Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/viewing-scan-results-scan-engine.md)

