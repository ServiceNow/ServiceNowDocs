---
title: Grouping by breakdown and filtering by breakdown
description: In breakdown widgets, breakdowns either group or filter indicator scores. When you create a widget, this dual purpose of breakdowns affects the function of the breakdown fields.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Breakdown widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Grouping by breakdown and filtering by breakdown

In breakdown widgets, breakdowns either group or filter indicator scores. When you create a widget, this dual purpose of breakdowns affects the function of the breakdown fields.

The **Breakdown** and **2nd Breakdown** fields in the widget form have a different function for breakdown widgets than for other widget types. In most other widget types, these fields specify filters. Only the indicator scores that correspond to the specified breakdown elements are shown. However, when you create a breakdown widget, you group the scores by a breakdown instead of filtering it. The elements of the breakdown are shown as the different wedges of a pie visualization, or separate columns in a column visualization, for example.

By default, a breakdown widget shows all the elements of the breakdown. However, you can restrict which elements are shown by applying an element filter. For more information, see [Element filters](c_BreakdownElementFilters.md#).

You can filter the scores by a first-level breakdown and element and show the elements of a second-level breakdown. To do this, specify a breakdown and an element in the **Breakdown** and **Element** fields. Then specify the breakdown that is used to group the data in the **2nd Breakdown** field. If you do not specify a **2nd Breakdown**, the **Element** field is ignored and the first **Breakdown** is used to group indicator scores instead of filtering them.

