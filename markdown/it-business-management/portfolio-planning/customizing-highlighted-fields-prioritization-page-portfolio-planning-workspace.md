---
title: Customizing highlighted fields on prioritization tab of Portfolio Planning workspace
description: Customize the fields to be highlighted on the Prioritization tab of a portfolio plan according to your planning manager's needs.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Configuring Prioritization and Roadmap settings in Portfolio Planning, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Customizing highlighted fields on prioritization tab of Portfolio Planning workspace

Customize the fields to be highlighted on the Prioritization tab of a portfolio plan according to your planning manager's needs.

By default, the Prioritization and Hierarchy tabs of a portfolio plan highlight the **Planning state** and **Status** fields of a planning item with colors. Based on your planning manager's requirements, you can configure fields that are of Choice type, such as Owner or Priority to also be the highlighted columns on the page. This customization requires:

-   Modifying the Prioritization view Script Includes \(APWBacklogConfigImpl for List view and APWGanttConfigImpl for Hierarchy view\).
-   Configuring a new record for the required field in the sys\_highlighted\_value table.

-   **[Modify Script Includes for Prioritization page in Portfolio Planning](../task/modify-script-includes-prioritization-page-portfolio-planning.md)**  
Modify the Script Includes for List and Hierarchy views of the Prioritization page to change the columns to be highlighted in these views in the workspace.
-   **[Create new highlighted values for Prioritization columns in Portfolio Planning](../task/create-highlighted-values-prioritization-portfolio-planning.md)**  
Customize the fields to be highlighted on the Prioritization page of a portfolio plan according to your planning manager's needs.

**Parent Topic:**[Configuring Prioritization and Roadmap settings in Portfolio Planning](configuring-prioritization-and-roadmap-settings-in-portfolio-planning.md)

