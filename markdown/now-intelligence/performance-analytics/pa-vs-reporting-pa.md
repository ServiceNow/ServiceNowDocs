---
title: Performance Analytics indicators compared to table data
description: Indicator data sources address a different set of use cases than table data sources.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics indicators compared to table data

Indicator data sources address a different set of use cases than table data sources.

Generally speaking, table data shows current state and indicators show trends. Visualizations of table data are more suitable for managing records. Performance Analytics indicators focus on managing processes. You need both.

Performance Analytics is able to generate accurate historical trends by capturing continuous snapshots on a regular schedule. As illustrated by the following diagram, table data answers the question of "Where are we today," while indicators answer questions of what is happening over time.

![Reporting answers questions about what is happening now. Performance Analytics answers questions about where we were and where we are going.](../image/pa-vs-reporting.png "Common process insight questions for table data and for Performance Analytics indicators")

In addition to calculating trends from snapshots, Performance Analytics is able to:

-   Track performance against Targets.
-   Alert when Thresholds are met.
-   Forecast future performance.
-   Compare performance at different points in time.
-   Accelerate time to value with best practice metrics.

Finally, while you can develop table data visualizations through trial and error, Performance Analytics requires background knowledge in how the feature works. You should carefully plan your Performance Analytics solutions and test them before implementing in a production environment.

**Important:** Do not try to configure Performance Analytics without training. A poorly-designed Performance Analytics solution can severely impact performance and even destabilize your instance. The initial training, [Performance Analytics Essentials](https://learning.servicenow.com/lxp/en/now-intelligence/performance-analytics-pa-essentials?id=learning_course_prev&course_id=289a949bdb2b009015531cbd139619d1), is available free of charge.

**Parent Topic:**[Exploring Performance Analytics](c_GetStartedwithPA.md)

**Related topics**  


[Planning your indicators](planning-indicators.md)

[Workflow for creating indicators](../task/workflow-automated-indicators.md)

[Design your Performance Analytics solution with KPI Composer](designing-pa-solution.md)

