---
title: Prevent and resolve technical debt with AI
description: Use the Scan Engine and ServiceNow Otto AI agent to prevent technical debt as you code or remediate existing findings from completed scans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/prevent-resolve-technical-debt-ai.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Platform Health, Using Impact, Impact]
---

# Prevent and resolve technical debt with AI

Use the Scan Engine and ServiceNow Otto AI agent to prevent technical debt as you code or remediate existing findings from completed scans.

Impact Platform Health delivers AI-generated code fixes at two critical points in your development lifecycle. Whether you're actively writing code or cleaning up existing technical debt, the Scan Engine detects violations against your defined coding standards and ServiceNow Otto generates fixes automatically. This unified approach reduces manual remediation time and improves platform quality across your ServiceNow instances.

The Scan Engine examines your instances for findings related to active definitions stored in the Scan Findings table. You can view findings, apply manual fixes, generate AI-suggested fixes, or submit exceptions for findings you believe aren't valid.

## Prevention and remediation workflows

AI-powered code fixes are available through two distinct workflows. Understanding which workflow applies to your situation helps you take action quickly.

<table><thead><tr><th>

Workflow

</th><th>

When You Use It

</th><th>

Outcome

</th></tr></thead><tbody><tr><td>

Real-time Prevention

</td><td>

-   You're actively writing or modifying code in your development environment.
-   When you save a record, the Scan Engine detects violations inline and you generate an AI fix before committing or promoting the code.

</td><td>

-   Prevents technical debt from reaching production.
-   Reduces time spent in code review cycles.

</td></tr><tr><td>

Batch Remediation

</td><td>

-   A scan has completed and findings are displayed in the findings dashboard.
-   You review the list of violations and generate AI fixes in bulk or individually to clean existing technical debt.

</td><td>

-   Accelerates remediation of existing issues.
-   Reduces manual development effort and errors when fixing production code.

</td></tr></tbody>
</table>## Unified AI engine

Whether you're preventing technical debt during development or remediating findings from scans, you interact with the same AI fix generation engine.

-   ServiceNow Otto AI agent analyzes your code against scan definitions
-   Side-by-side code comparison interface shows original code versus suggested changes
-   You accept, reject, or revise suggested fixes using the same controls
-   Exception workflows for Recommend level findings follow the same process
-   All changes are tracked in your active update set with full audit trails

## AI-suggested fix capabilities

The AI fix engine handles common coding violations quickly and accurately. Common fix types include the following:

-   Replacing deprecated API calls with current equivalents, for example, gs.log to gs.error
-   Adding missing error handlers to prevent unhandled exceptions
-   Correcting scoped app API usage to match ServiceNow general guidelines
-   Removing unsafe or deprecated functions to improve security
-   Formatting code to match style guidelines and improve maintainability

## Key benefits

-   Faster development: Developers can apply AI-generated fixes instantly instead of manually reviewing and correcting code
-   Consistency: All fixes follow the same coding standards and patterns, reducing variability across your codebase
-   Learning: Side-by-side code comparisons help developers understand ServiceNow general guidelines and leading practices
-   Scale: Bulk generate fixes to remediate dozens of violations in one workflow instead of fixing them individually
-   Reduced risk: AI fixes are generated from validated patterns and include full audit trails for compliance

## Next steps

Choose the workflow that matches your current task.

-   You're writing code and want to catch violations before saving, See [Use Real-time prevention monitoring while coding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/real-time-prevention-monitoring.md)
-   A scan has completed and you want to fix existing findings, See [Remediate existing findings with AI-suggested fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/batch-remediation-with-ai.md).

