---
title: Interactive Analysis filter deduplication
description: Upon launching Interactive Analysis, duplicate filters are removed automatically from the Filters panel. You do not have to clean up the filter panel.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Interactive Analysis, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Interactive Analysis filter deduplication

Upon launching Interactive Analysis, duplicate filters are removed automatically from the **Filters** panel. You do not have to clean up the filter panel.

Duplicate filters are removed according to the following criteria:

-   If the configuration is the same, the UI control determines which filter is shown on initial launch. Multiple input filters have first priority, then single input, check box, and radio buttons. For reference on available UI control type field options for displaying the filter, see .
-   If the configuration is the same, except that some filters have only one target and others have multiple targets, then only the last updated filter is retained.
-   If both the configuration and the UI control are the same, then the last updated filter is retained.
-   If the configuration is the same, but some filters have multiple target columns in the same target table, then all the filters are considered as separate filters and retained. An example of multiple target columns in the same target table is the **Date opened** and **Date escalated** columns in the incident table.
-   If the configuration and the UI control are the same, but the base condition is different for any two filters, then they are considered separate filters and retained.

**Parent Topic:**[Interactive Analysis](interactive-analysis.md)

