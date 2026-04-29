---
title: Learned patterns report
description: The Learned Patterns report helps assess the efficiency of alert aggregation and identify recurring alert patterns. It enables proactive issue resolution, enhancing overall system performance by providing insights into frequent alerts.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Learned patterns report

The Learned Patterns report helps assess the efficiency of alert aggregation and identify recurring alert patterns. It enables proactive issue resolution, enhancing overall system performance by providing insights into frequent alerts.

## Navigating and sorting the report

To access the Learned Patterns report, navigate to **Event Management** &gt; **Reporting** &gt; **Learned Patterns**.

Sorting Options: You can sort patterns by Pattern Score, Frequency, and Size to prioritize which alerts to address first.

## Metrics and data in the report

The report displays key metrics associated with learned patterns, including:

-   Frequency: The occurrence count of pattern identifier attributes \(CI/MetricName\).
-   Pattern Identifier Attributes: Describes how alert grouping combines relevant pattern attributes to create a learned pattern. These patterns can reappear across multiple alerts, often indicating the same underlying issue.
-   Presentation Format: Metrics are shown in a table format, organized by learned patterns.

This report allows you to:

-   Focus on Higher Frequency Alerts: Allocate resources to higher-frequency alerts to expedite the resolution of numerous alerts.
-   Target Larger Patterns with Lower Frequency: Allocate resources to larger learned patterns with lower frequency for targeted analysis.

## Pattern group details and identifier attributes

-   Expand a pattern group to display details about all the identifier attributes that are associated with the pattern.
-   Sort the entries within each pattern by Configuration Item and Feature Identifier.

<table id="table_mzp_gbf_gv"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration Item

</td><td>

CI associated with the combined pattern identifier attributes.

</td></tr><tr><td>

Feature Identifier

</td><td>

Feature identifier used for the combined pattern identifier attributes.

</td></tr><tr><td>

Frequency

</td><td>

Number of times the combined pattern identifier attributes appear in the data set.

</td></tr><tr><td>

Size

</td><td>

Number of occurrences of the combined pattern identifier attributes \(like Configuration Item and Feature Identifier\) within a learned pattern.

</td></tr><tr><td>

Score

</td><td>

Calculated score that combines the frequency and size of the learned pattern. The formula for this score is: `Score = Frequency × (Size + 1)`.This score helps prioritize patterns based on their recurrence and size, making it easier to focus on high-priority patterns.

</td></tr><tr><td>

CI Link

</td><td>

Link in the **Configuration Item** column to view details of the CI information.

</td></tr></tbody>
</table>