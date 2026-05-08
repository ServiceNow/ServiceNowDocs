---
title: Analyze safety incident patterns
description: The Incident patterns tab of the Health and Safety dashboard provides safety managers with an automated, real-time overview of the recurring patterns across their safety incident data.
locale: en-US
release: australia
product: Now Assist for Health and Safety
classification: now-assist-for-health-and-safety
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Incident pattern analysis, Use generative AI skills, Now Assist for Health and Safety, Health and Safety, Employee Service Management]
---

# Analyze safety incident patterns

The **Incident patterns** tab of the Health and Safety dashboard provides safety managers with an automated, real-time overview of the recurring patterns across their safety incident data.

The tab is designed to help the safety teams quickly understand where risks are clustering and how serious they are.

## Prerequisites

-   Verify that the Health and Safety Incident Management application is installed. For more information, see [Health and Safety Incident Management](../../ohs-incident-management/concept/hs-incident-mgmt-landing-page.md).
-   Verify that the generative AI \[com.snc.sn\_hs\_gen\_ai\] plugin is installed.
-   Configure the inclusion of incident records that contain sensitive data. For more information, see [Configure the inclusion of sensitive data in incident patterns](../task/hs-configure-sensitive-data-incident-pattern.md).
-   Verify that all the jobs are running. For more information on configuring the interval at which these jobs run, see [Configure the generation of incident patterns](../task/hs-configure-generation-incident-pattern.md).

## Role required

-   sn\_ohs\_im.manager and sn\_ohs\_im.agent roles are needed to view the dashboard.
-   sn\_ohs\_im.admin to edit the dashboard.
-   ui\_builder\_admin, to edit the dashboard visualizations that are built using the UI Builder.

## Access the Health and Safety incident pattern dashboard

Navigate to **Workspaces** &gt; **Health and safety Workspaces** and select the **Incident pattern** tab on the Health and Safety dashboard.

![](../image/na-hs-incident-pattern-dashboard.png "Incident pattern dashboard")

## Metrics on the incident pattern tab

Users can view the metrics on the dashboard if they have the Health and Safety Incident Management and the generative AI plugin installed.

<table id="table_krl_b23_l3c"><thead><tr><th>

Cards

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and safety pattern impact summary \(banner\)

</td><td>

AI-generated summary that analyzes all current pattern records and produces a consolidated overview of the most significant risk drivers across the organization.

</td></tr><tr><td>

Patterns identified

</td><td>

Total number of incident patterns detected in the most recent analysis run.

</td></tr><tr><td>

Pattern urgency

</td><td>

Breakdown of all identified patterns by their urgency classification.Each segment represents an urgency level, showing both the count and the percentage share.

</td></tr><tr><td>

Actions created

</td><td>

Count of corrective actions generated from identified patterns.

</td></tr><tr><td>

Patterns by urgency

</td><td>

Detailed table listing all identified patterns that are sorted by urgency.Select individual pattern record from the list to triage.

</td></tr><tr><td>

Pattern urgency trend

</td><td>

Month-by-month view of how patterns at each level have changed over time.

</td></tr><tr><td>

Pattern volume trend

</td><td>

Monthly snapshot of the total number of patterns identified and stacked by urgency level.

</td></tr></tbody>
</table>## Customizing widgets

You can customize the widgets in the dashboard to display relevant metrics by using the UI Builder. For more information, see UI Builder tutorial.

**Parent Topic:**[Incident pattern analysis](hs-incident-pattern-analysis.md)

