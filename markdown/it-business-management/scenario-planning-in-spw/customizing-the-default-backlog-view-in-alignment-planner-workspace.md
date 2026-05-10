---
title: Configuring additional columns for Prioritization in Strategic Planning
description: Customize the default column configuration for the Prioritization page of your portfolio plan so that your planning managers can select the appropriate data points they need.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Prioritization display settings in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Configuring additional columns for Prioritization in Strategic Planning

Customize the default column configuration for the Prioritization page of your portfolio plan so that your planning managers can select the appropriate data points they need.

Portfolio managers or product owners can show or hide the data for their planning items by using the Personalize side panel in the Prioritization tab of their workspace. By default, this side panel of Prioritization tab provides all the default fields available for that planning item. If your planning managers want to see additional columns, for example, there could be a requirement of information from a dot-walked field. In such cases or to remove any existing choices, you can configure them using the admin role.

|Personalize settings for Prioritization tab|Personalize settings for Kanban tab|Personalize settings for Hierarchy tab|
|-------------------------------------------|-----------------------------------|--------------------------------------|
|![Personalize side panel of Strategic Planning in the Prioritization tab showing the column choices.](../images/personalize-list-config.png)|![Personalize side panel of Strategic Planning Kanban tab showing the column choices.](../images/kanban-personalize.png)|![Personalize side panel of Strategic Planning Hierarchy tab showing the column choices.](../../alignment-planner-workspace/images/personalize-hierarchy-config.png)|

Add extra columns as choices to this side panel or remove any of the default column choices by updating the list layout configuration for the planning item types associated to the portfolio plan.

-   If the portfolio plan has multiple item types associated to it, update the view configuration of the Planning Item \[sn\_align\_core\_planning\_item\] table.
-   If the portfolio plan has a single item type associated to it, update the view configuration of the relevant table.

From the form view of the identified table, change the view to **APW Prioritization**, and update the list layout. For the detailed procedure of updating the layout configuration for a list, see [Configure the list layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-administration/t_ConfigureTheListLayout.md).

**Note:** List v3 is no longer available for new deployments. If you are already using list v3, you may continue to do so, but in this case some of the functionalities might not be available.

**Parent Topic:**[Prioritization display settings in Strategic Planning](configuring-prioritization-and-roadmap-settings-strategic-planning.md)

