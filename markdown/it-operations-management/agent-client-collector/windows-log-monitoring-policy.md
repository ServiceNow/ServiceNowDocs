---
title: Windows log monitoring default checks and policies
description: Agent Client Collector provides the following policy for Windows log monitoring.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC-M default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector, IT Operations Management]
---

# Windows log monitoring default checks and policies

Agent Client Collector provides the following policy for Windows log monitoring.

<table id="table_rdf_3r1_ktb"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage and Usage Example

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Event

</td><td>

os.windows.check-log

</td><td>

Enables monitoring log files on a Windows server.

</td><td>

Usage:-   -c crit N: Critical level if pattern has a group.
-   -f -log-file FILE: Path to log file.
-   -o --warn-only: Warn instead of critical on match.
-   -q pattern PAT: Pattern to search for. To search for multiple patterns, separate each pattern with a pipe \(\|\) and put inside quotes. For example: "SEVERE\|404"
-   -w warn N: Warning level if pattern has a group.

</td><td>

Windows Log CRITICAL: Found 4 criticals, 0 warnings for pattern SEVERE\|Exception\|404\|Errorin file C:\\ProgramData\\ServiceNow\\agent-client-collector\\log\\acc.log

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

