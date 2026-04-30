---
title: View unified service map and the impact paths in Service Operations Workspace
description: Visualize relationships between Configuration Items \(CIs\) and alerts with real-time updates and detailed impact paths. Enhance troubleshooting and proactive management by quickly identifying root causes and dependencies for both discovered services and application services.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [Unified service map in SOW ITOM, Impact path in SOW ITOM, Impact tree in SOW ITOM, Relation between CIs and alerts]
breadcrumb: [Service Operations Workspace, Configuring Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
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

2.  From the left navigation bar, select the Service Dashboard icon \(![Service Dashboard icon](../image/icon-service-dashboard.png)\).

    The Service Dashboard page appears.

3.  Select a service tile.

    A pop-up window displays the business criticality and severity of a service.

    ![Application service tile with options to see service details and service map.](../image/sow-itom-service-app-tile-options.png)

4.  Select **Service Map**.

    The application map along with the CI relationships appears.

    ![The application map along with the CI relationships appears.](../image/sow-service-map-page.png)

    **Note:** Depending on the size of the service, the unified map either shows the full map \(if it contains up to 60 CIs\) or an Impact Path leading to the most critical alert \(for maps with over 60 CIs\). For large maps, you can reveal more CIs by clearing the existing selecting and navigating to the **Showing more nodes** optimization option.

    ![Option to change how many CIs you want to view in the map.](../image/sow-service-map-nodes.png)

    If the impact path panel is closed, you can open it by selecting the Impact path icon \(![Impact path icon](../image/icon-sow-impact-path.png)\).

5.  Navigate between alerts by selecting an alert card.

    Alternatively, use the search function to find an alert by description, CI, or alert number and focus on its impact path.

    Selecting any alert tile displays the unified map for that alert. To return to the full map for the service, select **Clear**.

    ![Clear option to return to the full service map.](../image/sow-clear-option.png)

6.  To view alert details, select the Open Record Form icon \(![Open record form icon to view details of the alert.](../image/icon-sow-open-record-form.png)\) on the alert card.

    The alert details page opens.

    ![Alert details page.](../image/sow-servicemap-alert-details-page.png)


