---
title: Related dashboards page
description: The Related Dashboards page in Assistant analytics dashboard provides a centralized location to view and manage dashboards created in the Platform Analytics experience and shared across your organization.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-02-17"
reading_time_minutes: 2
breadcrumb: [Analyzing assistants, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Related dashboards page

The Related Dashboards page in Assistant analytics dashboard provides a centralized location to view and manage dashboards created in the Platform Analytics experience and shared across your organization.

## Overview of Related Dashboards page

The dashboard library in the Related Dashboards page includes dashboards that have been added by default or custom dashboards contributed by admins, making them available to users with appropriate permissions. You can pin favorite dashboards for quick access, search and filter the library, view, add, edit, and remove dashboards from the dashboard library.

To access the dashboard library, navigate to **All** &gt; **Assistant Analytics** and select Related Dashboards in the left navigation. The dashboard is accessible to the virtual\_agent\_admin and sn\_na\_analytics.ai\_engmt\_viewer roles.

![Dashboard Library in Related Dashboards screen.](../image/NAinVA-assistant-designer-analytics-related-dashboards.png "Dashboard Library in Related Dashboards page") ![]( "Dashboard Library in Related Dashboards page")

## Dashboard cards

Each dashboard in the library displays as a card with the following information:

-   Name: Display name of the dashboard as it appears on the card.
-   Description: A brief summary of the dashboard purpose.
-   Category: Tags indicating the dashboard type. For example, Default or Custom.
-   Last Updated: The user who last updated the dashboard and the date it was updated.

Use the grid and list icons to switch between grid layout and list layout based on your preference.

## Search and filter dashboards

Use the following options to find dashboards in the library:

-   **Search**: Enter keywords in the search bar to filter dashboards by name or description.
-   **Pinned dashboards**: View only dashboards you have pinned as favorites.
-   **All Dashboards**: View all dashboards that are added to the library.

The dashboard library supports pagination to help you navigate through large number of dashboards.

## Add or edit dashboards in the library

Role required: virtual\_agent\_admin

See [Add a dashboard to dashboard library](add-a-dashboard-to-dashboard-library.md) and [Edit a dashboard in the dashboard library](edit-a-dashboard-in-the-dashboard-library.md) for information on adding and editing a dashboard respectively.

## View a dashboard

Role required: virtual\_agent\_admin or sn\_na\_analytics.ai\_engmt\_viewer

To open a dashboard in full view, locate the dashboard card in the library and select anywhere on the card or select **View** from the Actions menu.

## Pin a dashboard as a favorite

Role required: virtual\_agent\_admin or sn\_na\_analytics.ai\_engmt\_viewer

Pin dashboards you frequently use to quickly access them from the Pinned dashboards section.

To pin a dashboard, locate the dashboard card in the library and select **Pin** from the Actions menu. To unpin a dashboard, select **Unpin** from the Actions menu.

You can pin a maximum of 8 dashboards to the pinned dashboard section.

## Remove a dashboard from the library

Role required: virtual\_agent\_admin

You can remove dashboards that are no longer needed, provided you have admin privileges.

To remove a dashboard, locate the dashboard card in the library and select **Remove** from the Actions menu. The dashboard is removed from the Related Dashboards page. This action does not delete the underlying Platform Analytics dashboard.

