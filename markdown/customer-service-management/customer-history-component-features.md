---
title: Customer History component features
description: Customer service agents can use several features in the Customer History component to view customer, consumer, or account history information.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer Central, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Customer History component features

Customer service agents can use several features in the Customer History component to view customer, consumer, or account history information.

## Search

The Search icon introduces keyword-based search functionality enabling agents to retrieve activities such as interactions, cases, and work orders by entering keywords or partial matches.

-   By default, the search bar is hidden. Select the search icon to show or hide it.
-   Admins can configure a toggle option to have the search bar open by default when the page loads.
-   Agents can enter a keyword or partial match to find relevant results. For example, entering `connect` displays cases with terms like connect, connected, or connection.

![Customer History search bar](../image/cust-central-search-feature.png)

## Filter

Agents can use the filter icon next to the search bar to quickly filter and view relevant case data. Selecting the filter icon displays the results in the Customer History component.

![Customer History filter feature](../image/cust-central-history-filter-feature.png)

Facets have been replaced by a filter icon. If the **Enable facets** check box is selected in UI builder, the system displays facets on the left of the CSM voice interaction record page. If this check box is not selected, the system displays a filter icon. Selecting the filter icon displays the selectable facets.

When an agent selects a facet:

-   The selected facet name appears below the search bar and the system displays the current results.
-   Selecting a new facet replaces the current results with the new facet's results.
-   Only one facet can be selected at a time.

**Note:**

-   For new customers: Filter icons are displayed by default.
-   For existing customers: Facets or filters appear based on screen size.

## Customer History access 

Starting with the Yokohama release, the [Front-line case page](csm-front-line-case-page.md) includes the Customer History component. This component ensures that agents can easily view customer details without navigating away from the case page.

Select the **Customer History** tab in the contextual side panel to access customer history.

![Customer History component](../image/cust-central-cust-history-comp.png)

## Cases facet

The Cases facet has been updated to improve case categorization for agents. This helps agents quickly filter the cases based on their status directly within the Customer History component.

![Cases Facet screen showing cases, open cases, and resolved cases](../image/cust-central-facets-feature.png)

The facet is divided into two subcategories: 

-   Open Cases 
-   Resolved Cases 

## Resizable layout blocks

The **Resizable Layout Blocks ** feature enables agents to adjust the size of page panel for better visibility. Agents can resize any block \(left, center, or right\) by following these steps:

1.  Click the edges of the block. 
2.  Drag to adjust the size as needed.

This feature is available across record pages in CSM Configurable Workspace and enables agents to optimize their workspace based on their needs.

## Real-Time updates in Customer History

The Customer History view updates in real time. When an agent adds a new case or interaction, a new activity is created. If another agent has the same customer record open, the view automatically refreshes to show the new activity. You don’t need to refresh the page manually.

**Note:**

-   The view refreshes only for new activities created in the \[sn\_actsub\_activity\] table that are linked to the currently open customer record.
-   Changes to existing records or knowledge articles do not trigger a refresh.
-   The view updates only for the specific record that you're viewing. For example, if you’re viewing a contact, updates to the associated account won’t appear unless you open the account record directly.
-   Real-time updates are supported only on the Front-line case page and CSM default record page.

## Filter activities by time

Agents can use the date range icon to filter customer activities by day, month, quarter, or year-based on the configuration set by the admin. The date range icon appears next to the search bar:

-   If Day is configured, select a specific date to view activities for that day.
-   If Month, Quarter or Year is configured, activities appear grouped by the selected time. The activity list updates based on the selected filter.

