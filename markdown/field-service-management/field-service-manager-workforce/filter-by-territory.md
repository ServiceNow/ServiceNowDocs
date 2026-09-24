---
title: Filter the team calendar by territory
description: Filter which agents appear on the team calendar by territory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-manager-workforce/filter-by-territory.html
release: brazil
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [territory filter, team calendar, Manager Workforce]
breadcrumb: [Change views in Workforce, Managing agents and tasks from Workforce, Managing workforce, Use, Field Service Management]
---

# Filter the team calendar by territory

Filter which agents appear on the team calendar by territory.

## Before you begin

Role required: wm\_agent, wm\_basic, or wm\_manager

## About this task

Whenever you open the team calendar, agents in the territories saved as your default are displayed. Territories are listed as parent territories, with any child territories nested underneath. Select **Restore default** to return the filter to the territories saved in Settings. Select **Clear all** to remove the current selection. To limit the filter to one territory at a time, in Settings, turn on **Single select territory**. With this setting on, selecting a different territory replaces your previous selection, and selecting a parent territory still applies only that parent. If no default territory is saved in Settings, the calendar displays all territories.

## Procedure

1.  Navigate to **Workforce**.

    -   Managers, navigate to **All** &gt; **Field Service** &gt; **Manager** &gt; **Workforce**.
    -   Agents, navigate to **All** &gt; **Field Service** &gt; **Agent** &gt; **Workforce**.
    -   If Workforce Optimization is installed and activated, managers can navigate to **Workspaces** &gt; **Manager Workspace** &gt; **Workforce**.
2.  Select the territory filter above the calendar.

3.  Select one or more territories from the list.

    **Note:** Selecting a parent territory applies only that parent. Its child territories aren't included.

4.  Select **Apply**.

    The calendar updates to show agents in the selected territories.


**Related topics**  


[Set a default territory on the Team calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-manager-workforce/configure-a-default-territory-on-the-team-calendar.md)

[Filter the team calendar by assignment group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-manager-workforce/filter-by-group.md)

