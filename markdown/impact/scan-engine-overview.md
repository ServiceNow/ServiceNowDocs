---
title: Monitor and manage instance health
description: The Scan Engine is the diagnostic engine behind Impact Platform Health. It continuously evaluates your ServiceNow instance against leading practice definitions so you can find, prioritize, and resolve issues before they affect your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/scan-engine-overview.html
release: brazil
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 4
keywords: [Scan Engine, Platform Health, instance health, health score, scan findings]
breadcrumb: [Exploring Impact, Impact]
---

# Monitor and manage instance health

The Scan Engine is the diagnostic engine behind Impact Platform Health. It continuously evaluates your ServiceNow instance against leading practice definitions so you can find, prioritize, and resolve issues before they affect your users.

With thousands of configuration points across an instance, it is difficult to know where risk is hiding. The Scan Engine solves this by scanning your instance against a library of leading practice definitions, then surfacing the results as actionable findings, trends, and consolidated Instance Health scoring.

Using the Scan Engine, you can:

-   Understand instance health through hundreds of leading practice checks across five categories.
-   Reduce technical debt and optimize performance before issues reach production.
-   Prevent common implementation missteps with real-time, in-context guidance.
-   Track trends over time with role-based dashboards and a comparable, repeatable health score.

## Why scan your instance

Every scan protects your instance against risk that would otherwise go unnoticed until it causes an outage, a failed upgrade, or a security incident. The Scan Engine supports two overall scan types so you can choose the right depth for the moment.

|Scan type|When it runs|
|---------|------------|
|Full scan|Evaluates every record in scope against every active definition. Only one full scan can run on an instance at a time, protecting instance performance.|
|Delta scan|Evaluates only what has changed since the last scan. The Scan Engine determines automatically whether a full or delta scan is needed, reducing the decisions you have to make.|

For details on initiating, monitoring, and canceling scans, see [Full and delta scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-parallel-processing.md).

## Health scores and definitions

Every finding traces back to a definition, and every definition belongs to one of five categories.

|Category|What it covers|
|--------|--------------|
|Security|Breach risk, compliance violations, and access-control vulnerabilities.|
|Performance|Issues that affect responsiveness and compound if left unaddressed.|
|Manageability|Administration and supportability of the instance.|
|Upgradeability|Configurations that can block or delay ServiceNow release upgrades.|
|User experience|Adoption and satisfaction factors with lower overall urgency.|

These five categories roll up into a single Instance Health Score, a 0–100 metric weighted by how much risk each category represents. For the full calculation model, see [Platform Health score calculation model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/instance-health-score-calculation.md).

## Working with findings

After a scan completes, every violation of a definition becomes a finding. Reviewing and resolving findings is a two-phase process.

1.  Review results, monitor an active scan or open a completed scan record to see its status, duration, and batch progress.
2.  Work findings, open individual findings to understand their enforcement level and impact, then apply fixes or submit exceptions for review.

Each finding is evaluated along two dimensions, its enforcement level, which determines whether the system blocks, warns, or informs. Also its risk rating, which determines the order findings should be addressed within that level. For the full breakdown of enforcement levels and finding record fields, see [View scan results for Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/viewing-scan-results-scan-engine.md).

For most findings, resolution does not have to be manual. With ServiceNow Otto, you can generate an AI-suggested fix as you code or in bulk from completed scan results. For details on both workflows, see [Prevent and resolve technical debt with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/prevent-resolve-technical-debt-ai.md).

## Tracking trends over time

Role-based dashboards give every persona, from executives to developers, a view of platform health suited to their responsibilities, refreshed automatically after each scan. For details on dashboard roles and interactivity, see [Track Platform Health trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-diagnostic-dashboards.md).

**Related topics**  


[Full and delta scans to monitor instance health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-parallel-processing.md)

[Instance Health Score calculation model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/instance-health-score-calculation.md)

[View scan results for Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/viewing-scan-results-scan-engine.md)

[Prevent and resolve technical debt with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/prevent-resolve-technical-debt-ai.md)

[Track Platform Health trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-diagnostic-dashboards.md)

