---
title: Differences between Core UI and Platform Analytics dashboards
description: When the unified analytics property is enabled, Core UI dashboards and dashboards in Platform Analytics can coexist in your instance. Use this reference to distinguish between them.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [What's the difference between old and new dashboards]
breadcrumb: [Explore, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Differences between Core UI and Platform Analytics dashboards

When the unified analytics property is enabled, Core UI dashboards and dashboards in Platform Analytics can coexist in your instance. Use this reference to distinguish between them.

Both Core UI and Platform Analytics dashboards enable you to show visual components in a shareable canvas. When the **com.glide.par.unified\_analytics.enabled** property is enabled, all dashboards are available. This property is set to true on net new Australia instances and on upgrade to Australia.

On migrated instances, your Core UI data, existing dashboards, reports, interactive filters, and Performance Analytics widgets are moved to Platform Analytics. The result is a single set of visualizations and unified filters for all data sources. For more information, see [Platform Analytics Migration Center](../../par-for-workspace/concept/data-migration.md).

## Core UI dashboards

Core UI dashboards are those created in the classic UI featuring visualizations created in Report Designer and Performance Analytics content created using PA widget forms.

-   **Dashboard example**

    ![Core UI dashboard example with four single score visualizations and part of the configuration panel](../image/db-edit-mode-core-ui.png)

-   **Menu path**

    Both Core UI and Platform Analytics dashboards are found in the Library. Navigate to **Platform Analytics** &gt; **Library** &gt; **Dashboards**.


When you edit Core UI dashboards and their content, you do so in the Core UI tools including Report Designer. For more information, see [Reporting, dashboards, and Performance Analytics in the Core UI](../../reporting/concept/classic-vis-overview.md).

## Platform Analytics dashboards

Platform Analytics dashboards are created using either UI Builder or the inline dashboard editor. These dashboards support all objects in the element library, such as data visualizations, filters, and rich text. In a tabbed dashboard, these contents can be placed in a tab or above the tabs. Filters placed above the tabs apply to content on all the tabs.

When you create Platform Analytics dashboards, you can add any existing element that you have rights to, or create a new element from within the dashboard. These elements include data-agnostic visualizations based on indicators, table data, MetricBase data, and Usage Insights.

Platform Analytics dashboards also provide Proactive Insights that support more informed decision making. Insights explore correlations and highlight potential changes and issues before they turn into problems.​ For more information, see [Proactive analytics insights on dashboards](../../par-for-workspace/concept/proactive-analytics.md).

-   **Dashboard example**

    ![Platform Analytics experience dashboard with three single score visualizations and part of the Details panel](../image/db-edit-mode-ne-ac.png)

-   **Menu path**

    **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**


**Parent Topic:**[Exploring Platform Analytics dashboards](ac-elements.md)

