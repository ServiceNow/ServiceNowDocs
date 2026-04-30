---
title: Text analytics and text widgets
description: Text analytics reveal any patterns that exist in user-entered text fields.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Text analytics and text widgets

Text analytics reveal any patterns that exist in user-entered text fields.

**Note:** This feature is part of the Core UI front end. It is not supported on Platform Analytics dashboards or UI Builder pages, except to a limited extent when migrated in compatibility mode. To build Platform Analytics components, see [Data visualizations in Platform Analytics](analytics-center-data-visualizations.md) or [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

This feature is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

Text analytics provides visual tools for analyzing the text that users enter in forms. The possible benefits of such analyses include early warning of customer pain points, disclosure of fraudulent activity, and the extraction of certain entities or concepts that are clustering in sales, incident reports, etc. The useful information in this unstructured, qualitative data may be hidden from other tools.

**Note:**

-   Text analytics is available only with licensed Performance Analytics.
-   Platform Analytics data visualizations do not support text analytics.

Text analysis begins with indexing the text. Text indexing is defined on indicator sources, to allow for the reuse of a single index configuration by many indicators.

When you set up text analytics, you decide on:

-   Which fields in an indicator source to index.
-   Which indicators to apply a text index configuration to.
-   Which stop words to exclude from analysis.
-   What phrases to search for, besides single words.
-   Keywords for default filtering.

When you have set up text analytics, create a widget to visualize the text and include the widget in a dashboard.

The following video walks you through the process of setting up and viewing text analytics:

How to create a Performance Analytics text analytics word cloud widget, which analyzes unstructured or qualitative data. Also how to set up and collect data for text analytics widgets.

