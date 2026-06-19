---
title: View unified service map and the impact paths in Service Operations Workspace
description: Visualize relationships between Configuration Items \(CIs\) and alerts with real-time updates and detailed impact paths. Enhance troubleshooting and proactive management by quickly identifying root causes and dependencies for both discovered services and application services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-operations-workspace-for-itom-apps/view-impact-tree.html
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Unified service map in SOW ITOM, Impact path in SOW ITOM, Impact tree in SOW ITOM, Relation between CIs and alerts]
breadcrumb: [Service Operations Workspace, Configuring SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View unified service map and the impact paths in Service Operations Workspace

Visualize relationships between Configuration Items \(CIs\) and alerts with real-time updates and detailed impact paths. Enhance troubleshooting and proactive management by quickly identifying root causes and dependencies for both discovered services and application services.

## Before you begin

Role required: evt\_mgmt\_user, evt\_mgmt\_operator, or evt\_mgmt\_admin

## About this task

The enhanced service map in Service Operations Workspace displays the impacted path of an alert to enable you to quickly assess its impact on a service. You can access the enhanced service map directly from the Service Dashboard, or from the preview panel or from an impacted service in the Express List.The service map has several modes of display:

-   For a service with up to 60 CIs, regardless of alert status, the map shows all CIs.
-   For a service with more than 60 CIs without alerts, the map shows up to 60 CIs.
-   For a service with more than 60 CIs with alerts, the map shows the impacted path of the most recent alert with the highest severity.

You can also investigate a wider view of the service topology on the service map for up to 250 CIs regardless of alerts. For a broader view, select **Clear** and choose a mode of either up to 60 or up to 250 nodes.

**Note:** Admins can continue using the legacy service map to manage the propagation of severity. Access the map by navigating to **Services** &gt; **Application Services**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left navigation bar, select the Service Dashboard icon: \[Omitted image "icon-service-dashboard.png"\] Alt text: Service Dashboard icon.

    The Service Dashboard page appears.

    **Note:** The application services that appear in the Service Dashboard are those added to the Impact Filter Services list. For more information, see [Add application services for impact calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/add-impact-cal-services.md).

3.  Select a service tile.

    A pop-up window displays the business criticality and severity of a service.

    \[Omitted image "sow-itom-service-app-tile-options.png"\] Alt text: Application service tile with options to see service details and service map.

4.  Select **Service Map**.

    The application map along with the CI relationships appears.

    \[Omitted image "sow-service-map-page.png"\] Alt text: The application map along with the CI relationships appears.

    **Note:**

    Depending on the size of the service, the unified map either shows the full map \(if it contains up to 60 CIs\) or an Impact Path leading to the most critical alert \(for maps with over 60 CIs\). For large maps, you can reveal more CIs by clearing the existing selecting and navigating to the **Showing more nodes** optimization option.

    **Impact Path** shows alerts on the selected CI and all CIs within its impact subtree.

    \[Omitted image "sow-service-map-nodes.png"\] Alt text: Option to change how many CIs you want to view in the map.

    If the **Impact path** panel is closed, you can open it by selecting the Impact path icon \(\[Omitted image "icon-sow-impact-path.png"\] Alt text: Impact path icon\).

    To view active alerts directly associated with the selected CI, select the Related items icon \(\[Omitted image "icon-service-map-related-items.png"\] Alt text: Related items icon\) in the right pane, then select **Active Alerts**.

    \[Omitted image "sow-service-map-related-items.png"\] Alt text: View active alerts directly associated with the selected CI.

5.  Navigate between alerts by selecting an alert card.

    Alternatively, use the search function to find an alert by description, CI, or alert number and focus on its impact path.

    Selecting any alert tile displays the unified map for that alert. To return to the full map for the service, select **Clear**.

    \[Omitted image "sow-clear-option.png"\] Alt text: Clear option to return to the full service map.

6.  To view alert details, select the Open Record Form icon \(\[Omitted image "icon-sow-open-record-form.png"\] Alt text: Open record form icon to view details of the alert.\) on the alert card.

    The alert details page opens.

    \[Omitted image "sow-servicemap-alert-details-page.png"\] Alt text: Alert details page.


