---
title: View application service health information in Service Operations Workspace
description: Monitor the health of services and filter the information that you want to view, allowing you to focus on the most relevant data and make informed decisions quickly.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Operations Workspace, Configuring SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View application service health information in Service Operations Workspace

Monitor the health of services and filter the information that you want to view, allowing you to focus on the most relevant data and make informed decisions quickly.

## Before you begin

Role required: evt\_mgmt\_user or evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left navigation bar, select the Service Dashboard icon: ![Service Dashboard icon](../image/icon-service-dashboard.png).

    The Service Dashboard page appears.

    **Note:** The application services that appear in the Service Dashboard are those added to the Impact Filter Services list. For more information, see [Add application services for impact calculation](../../event-management/task/add-impact-cal-services.md).

3.  Perform the following actions as required.

<table id="table_qrg_kld_zbc"><thead><tr><th>

Features

</th><th>

Actions

</th></tr></thead><tbody><tr><td>

Make the tile size larger or smaller.

</td><td>

1.  Select the Display settings icon \(![Display settings icon](../image/settings-display-icon.png)\).
2.  From the **Display settings** pop-up window, select the size.
 ![Display size list.](../image/sow-display-size.png)

</td></tr><tr><td>

Group services by selected criteria

</td><td>

Select the arrow next to **Group By** and then select the criteria by which you want to group services.

 ![List of options by which you can group by services.](../image/sow-group-by-list.png)

</td></tr><tr><td>

Group order

</td><td>

Select the arrow next to **Group order** and then select the criteria by which you want to group services.

 ![Group order list](../image/sow-group-order.png)

</td></tr><tr><td>

Segment each group by

</td><td>

Segment each group by severity, business criticality, and cost to categorize and organize them into distinct groups based on these attributes.

 ![Segment each group by list](../image/sow-segment-grp-by-list.png)

</td></tr><tr><td>

Filter information

</td><td>

Filter the information displayed on the dashboard ensuring you focus on relevant data for effective monitoring.

 -   To set a global filter, select the Filter icon \(![Filter icon](../../event-management/image/filter-icon-button.png)\) and set the global filter condition, add filter conditions, and then select **Apply**.

![Global filter option](../image/sow-global-filter.png)

-   To exclude a severity from the display, select it in the **Severity Breakdown** ribbon. Filtered-out severities will appear dimmed. To restore a dimmed severity to the display, simply select it again.
![Severity Breakdown filter](../image/sow-severity-breakdown.png)

</td></tr></tbody>
</table>
**Parent Topic:**[Service Operations Workspace](../concept/workspace-dashboard-use.md)

