---
title: Configuring additional columns for Prioritization page in Portfolio Planning
description: Configure what columns must be displayed on the Prioritization page of portfolio plans so that your planning managers can select the appropriate data points they need.
locale: en-US
release: yokohama
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Configuring additional columns for Prioritization page in Portfolio Planning

Configure what columns must be displayed on the Prioritization page of portfolio plans so that your planning managers can select the appropriate data points they need.

Portfolio managers or product owners can show or hide the data for their planning items by using the Personalize side panel in the Prioritization page of their workspace. By default, this side panel of List and Hierarchy views provides all the default fields available for that planning item. If your planning managers want to see additional columns, for example, there could be a requirement of information from a dot-walked field. In such cases or to remove any existing choices, you can configure them using the admin role.

|Personalize settings for List view|Personalize settings for Hierarchy view|
|----------------------------------|---------------------------------------|
|![Personalize side panel of Strategic Planning List view in the Prioritization page showing the column choices.](../../spw-prioritization/images/personalize-list-config.png)|![Personalize side panel of Strategic Planning List view in the Prioritization page showing the column choices.](../../alignment-planner-workspace/images/personalize-hierarchy-config.png)|

Add extra columns as choices to this side panel or remove any of the default column choices by updating the list layout configuration for the planning item types associated to the portfolio plan.

-   If the portfolio plan has multiple item types associated to it, update the view configuration of the Planning Item \[sn\_align\_core\_planning\_item\] table.
-   If the portfolio plan has a single item type associated to it, update the view configuration of the relevant table.

From the form view of the identified table, change the view to **APW Prioritization**, and update the list layout. For the detailed procedure of updating the layout configuration for a list, see [Configure the list layout](https://www.servicenow.com/docs/access?context=t_ConfigureTheListLayout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

**Note:** List v3 is no longer available for new deployments. If you are already using list v3, you may continue to do so, but in this case some of the functionalities might not be available.

