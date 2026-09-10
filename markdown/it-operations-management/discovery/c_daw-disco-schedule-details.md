---
title: Discovery Admin Workspace schedule details
description: Discovery Admin Workspace enables you to conveniently view, edit, and run Discovery schedules conveniently within a single interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/c\_daw-disco-schedule-details.html
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace Schedules, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace schedule details

Discovery Admin Workspace enables you to conveniently view, edit, and run Discovery schedules conveniently within a single interface.

To access Discovery schedule details in Discovery Admin Workspace, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules** &gt; **Discovery schedules**.

**Note:** The capabilities described here are available starting with Discovery Admin Workspace v1.8.0. Specific version requirements are noted for individual features where applicable.

After selecting a schedule name from the table, the schedule header displays key information such as Discovery details, MID Server details, and anomaly severity when anomaly detection is enabled. For more information, see [Discovery Admin Workspace Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/discovery-admin-workspace-setup.md).

The actions available in the schedule header depend on the discovery type:

-   For an IP-based Discovery schedule, select **Save** to save your changes, or select **Quick ranges** to create a range of IP addresses to discover.
-   For a cloud or certificate Discovery schedule, select **Edit** to update the schedule. To run any Discovery schedule on demand, select **Discover now**.

**Note:** Certificate discovery is available in Discovery Admin Workspace starting with v1.20.0 and requires the Brazil, Australia, or Zurich release starting with Patch 8.

## Key features

-   **Overview**

    The **Overview** tab includes visualizations that provide detailed information about the Discovery schedule. These visualizations offer a comprehensive view of the schedule's performance and status, showing key metrics like the number of discoveries completed, success rate, and any errors encountered. Additionally, the visualizations highlight trends over time, enabling you to quickly identify patterns and potential issues. For a full list of the visualizations available on this tab, see [Schedule details data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/r_dawScheduleDetailsOverview.md).

    **Note:** The time scale reflected on this page can be configured on the Settings page. For more information, see [Discovery Admin Workspace Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/discovery-admin-workspace-setup.md).

    Select the **More Options** icon \(\[Omitted image "icon-menu-sow.png"\]\), then select **Refresh** to refresh the data for each visualization in this section.

-   **Schedule Details**

    The **Schedule Details** tab provides in-depth information about the Discovery schedule and enables you to update the information directly within the interface.

    Select the **More Options** icon \(\[Omitted image "icon-menu-sow.png"\]\), to access additional actions for customizing and managing the form interface.

-   **Run History**

    The **Run History** tab displays the status of the last 10 scheduled discoveries, including icons for anomaly detection, when enabled. Select a Discovery status number to view detailed information. For more details, see [Discovery Admin Workspace status details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/daw-disco-status-details.md).


