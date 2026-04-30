---
title: Configuring dashboards
description: Configure your dashboard and perform admin tasks. Most tasks are performed in either the dashboard details or the dashboard settings UI.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Dashboards, Platform Analytics experience, Platform Analytics]
---

# Configuring dashboards

Configure your dashboard and perform admin tasks. Most tasks are performed in either the dashboard details or the dashboard settings UI.

## Common configuration tasks

The following tasks do not require a special role, though they may be limited to the dashboard owner or a user with editing rights.

-   [Change dashboard name or description](../task/config-db-in-ac.md)

    Provide an informative description of your dashboard for other users.

-   [Specify dashboard requester](../task/config-db-in-ac.md)

    Specify the user who requested that this dashboard be created. Specifying the user automatically gives them editing rights to the dashboard.

-   [Transfer ownership of a dashboard](../task/config-db-in-ac.md)

    By default, the creator of the dashboard is the dashboard owner. If you are the owner of a dashboard, you can transfer this ownership to another user or to a user group.

-   [Set background colors](../task/configure-ac-db-settings.md)

    Select the background colors for one or more tabs on the dashboard.

-   [See who created a dashboard](../task/config-db-in-ac.md)
-   [See who the dashboard is shared with](../task/config-db-in-ac.md)

## Admin configuration tasks

The following tasks require at least the dashboard\_admin if not the admin role.

-   [Set data refresh options](../task/configure-ac-db-settings.md)

    Set whether the dashboard is refreshed on a schedule and whether data caching is used. Requires the dashboard\_admin or admin role. For more information, see [Data caching in Platform Analytics](../../par-for-workspace/concept/data-caching-pa.md).

-   [Certify a dashboard](../task/certify-db-ac.md)

    Certify that a dashboard has been officially approved for use by your organization. Requires the admin role.

-   [Configure Platform Analytics dashboard tab cache timeout](../task/configure-ac-db-timeout.md)

    Set the number of minutes that dashboard tab content is retained before being refreshed. Applies to all dashboard tabs on the instance. Requires the admin role.

-   [Manage which workspaces are allowed to contain the dashboard](../task/config-db-in-ac.md)

    Specify the workspaces on the instance other than the Platform Analytics experience that this dashboard can be added to. Requires the admin or dashboard admin role. For more information about dashboards in workspaces, see [Add a dashboard to a Dashboards page](../../performance-analytics/task/add-dashboard-to-workspace.md).

-   [Move a Platform Analytics dashboard with an update set](../task/move-pae-db-with-update-set.md)

    Moves the dashboard structure to an update set, so it can be put on another instance. Does not include dashboard contents. Requires the admin role.


## Process Mining integration tasks

-   [Configure a Process Mining map on a dashboard](../../par-for-workspace/task/configure-po-map.md)

    Map the different states that are part of your process and the transitions between those states. See which states the objects of the process are in and the speed with which they change state. Requires the sn\_process\_optimization\_analyst role.

-   [Creating Process Mining projects from Proactive Analytics suggestions](../../par-for-workspace/concept/pm-projects-insights-suggestions.md#)

    The Insights panel can include suggestions for Process Mining projects to create. Creating the projects requires the sn\_process\_optimization\_analyst role.


