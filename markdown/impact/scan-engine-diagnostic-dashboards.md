---
title: Track Platform Health trends
description: Analytics Dashboards provide a graphical way to view detailed information relating to findings, both pending and resolved, with the Scan Engine. The dashboards are role-based, allowing for persona-based views of information. They display  key metrics,  charts, and  trend analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/scan-engine-diagnostic-dashboards.html
release: australia
product: Impact
classification: impact
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Platform Health, Using Impact, Impact]
---

# Track Platform Health trends

Analytics Dashboards provide a graphical way to view detailed information relating to findings, both pending and resolved, with the Scan Engine. The dashboards are role-based, allowing for persona-based views of information. They display  key metrics,  charts, and  trend analysis.

Analytics Dashboards vary depending on your ServiceNow role. As each role has specific needs and responsibilities, the dashboard is tailored to provide relevant insights and metrics per role.

Each dashboard role has a correlative relationship with its corresponding dashboard view. Users will only be able to access dashboard views associated to the roles their account has been granted.

<table id="table_z2w_4vz_chc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Executive`sn_impact_common.Impact Executive`

</td><td>

-   Provides executives a high-level view of platform health and AI remediation impact.
-   Focuses on strategic indicators such as technical debt, compliance risk, and overall cost and time savings from Platform Health fixes.
-   Helps leadership understand business value and make informed decisions about investments and priorities without diving into technical details.

</td></tr><tr><td>

Platform Owner`sn_impact_common.Impact Platform Owner`

</td><td>

-   Provides visibility into scan results, remediation progress, and technical debt across instances.
-   Designed for operational oversight to help owners manage risk, enforce governance, and verify workflows are running efficiently.

</td></tr><tr><td>

Team Lead`sn_impact_common.Impact Development Team Lead`

</td><td>

-   Highlights assigned findings and team performance metrics.
-   Centered on delivery and resource management.
-   Helps team leads balance workloads, track progress, and keep remediation aligned with project timelines, ensuring smooth execution without disrupting other deliverables.

</td></tr><tr><td>

Developer`sn_impact_common.Impact Developer`

</td><td>

-   Provides hands-on, task-focused information such as developer assignments, detailed findings, and outstanding exception reasons.
-   Developers can quickly act on issues, provide feedback, and streamline remediation work, reducing manual effort while maintaining code quality. 

</td></tr></tbody>
</table>## Dashboard data freshness

Performance Analytics \(PA\) jobs run automatically at the correct time and frequency following each scan, so dashboard data updates in near-real-time without manual intervention. The dashboard displays a status indicator so that all user personas can monitor the current state of data processing.

|Status|Description|
|------|-----------|
|Up to date|PA jobs have completed and the dashboard reflects the latest scan results.|
|Updating|PA jobs are currently running. Data will refresh automatically when processing completes.|
|Delayed|PA jobs have not completed within the expected window. Data may not reflect the most recent scan. Contact your administrator if this persists.|

## Interacting with dashboard charts

Donut chart segments are interactive. Select any segment to open a filtered backend list view showing only the findings that correspond to that segment. For example, findings by a specific level, category, or status.

The heatmap uses an accessible color scheme designed for readability across a range of color vision differences.

