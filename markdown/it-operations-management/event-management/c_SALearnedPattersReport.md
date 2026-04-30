---
title: Learned Patterns report
description: The Learned Patterns report helps you assess the efficiency and depth of analysis of alert aggregation and helps you to identify higher-frequency occurring alert patterns.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Automated alert grouping, Alert grouping types, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Learned Patterns report

The Learned Patterns report helps you assess the efficiency and depth of analysis of alert aggregation and helps you to identify higher-frequency occurring alert patterns.

The report displays metrics associated with learned patterns such as the frequency of occurrence and the number of occurrences of the pattern identifier attributes in learned patterns \(CI/MetricName by default\). For each alert, Event Management alert aggregation combines the associated pattern identifier attributes that represent the alert. It then groups all the pattern identifier attributes for alerts that occur together, to create a learned pattern. The same combination of pattern identifier attributes can exist in multiple learned patterns. Typically, a learned pattern indicates a single problem. The report displays metrics in table format, grouped by learned patterns.

To display the report, navigate to **Event Management** &gt; **Reporting** &gt; **Learned Patterns**.

You can sort the learned patterns by pattern score, pattern frequency, and pattern size. You can use this report to:

-   Allocate resources to the higher frequency occurring alerts to reduce the time for closing a large number of alerts.
-   Allocate resources to larger learned patterns of lower frequency.

Actions:

-   Expand a pattern group to display details about all the identifier attributes that are associated with the pattern.

    |Column|Description|
    |------|-----------|
    |Configuration Item|The configuration item used for the combined pattern identifier attributes.|
    |Feature Identifier|The feature identifier used for the combined pattern identifier attributes.|
    |Frequency|The number of times that the combined pattern identifier attributes occur in the data set.|

-   Sort within each pattern by Configuration Item and Feature Identifier.
-   View the following information for each pattern:
    -   **Size**: The number of combined pattern identifier attributes occurrences in a learned pattern.
    -   **Frequency**: The number of times that a learned pattern occurs in the data set.
    -   **Score**: Combined calculation of frequency and size, using the formula:

        `Frequency * (Size + 1)`

-   Click a CI link in the **Configuration Item** column to display the CI form.

