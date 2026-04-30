---
title: Interacting with breakdown widgets on dashboards
description: Performance Analytics users can interact with individual breakdown widgets on dashboards to change the visualization or breakdown.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Breakdown widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Interacting with breakdown widgets on dashboards

Performance Analytics users can interact with individual breakdown widgets on dashboards to change the visualization or breakdown.

Widgets with the **Type** of **Breakdown** enable users to select the visualization when viewing the widget on a dashboard. Users can select any visualization for the widget type from the **Visualization** choice list when viewing the widget on a dashboard.

**Note:** You cannot select the **Pivot Scorecard** visualization from a dashboard. To use this visualization, configure the widget record.

Breakdown widgets also enable users to select the breakdown when multiple breakdowns are available. All available breakdowns for the widget **Indicator** appear in the **Breakdown** choice list when viewing the widget on a dashboard. If the indicator has only one associated breakdown, the **Breakdown** choice list does not appear on the widget.

**Note:** If the widget is added to a breakdown dashboard and the user selects the same breakdown on the widget and on the dashboard, the dashboard breakdown is ignored. However, when the user selects any other combination of widget and dashboard breakdowns, both breakdowns apply.

By default, the interactive breakdown applies as the 1st-level breakdown. However, if the widget is on a breakdown dashboard and **Follow element** is selected on the Widget form, the interactive breakdown applies as the 2nd-level breakdown. \(**Collect breakdown matrix** must be set on the indicator for 2nd-level breakdowns to apply.\) Any breakdown that is set on a dashboard that contains the widget applies as the 1st-level breakdown.

You can disable this functionality for a specific widget by clearing the **Show visualization selector** or **Show breakdown selector** check boxes on the Widgets form.

The visualization or breakdown selected in the widget record is used as the default.

**Related topics**  


[Indicator breakdowns](c_CreatingBreakdowns.md)

[Using breakdowns on dashboards](c_SpecialDashboards.md)

