---
title: Using Service Owner Workspace
description: Use Service Owner Workspace to monitor the health of your services and your customer satisfaction. View outages, critical incidents, and change requests associated with services and offerings.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Service Owner Workspace, IT Service Management]
---

# Using Service Owner Workspace

Use Service Owner Workspace to monitor the health of your services and your customer satisfaction. View outages, critical incidents, and change requests associated with services and offerings.

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. For information on the product replacement and the deprecation process, see [Service Owner Workspace](SPM2-premium.md).

<table id="table_e2x_rbr_nkb"><tbody><tr><td>

![Use Service Owner Workspace](../image/SOWUseBanner2.png "Navigate")

</td></tr></tbody>
</table>With Service Owner Workspace you can monitor metrics and analyze the health of your services from a single user interface. Get to know how metric models are created and configured for service offerings and how they are used in Service Owner Workspace.

## Service Owner Workspace features

Service Owner Workspace features include:

-   A view-only, multi-tab interface for monitoring and managing multiple portfolios and related services.
-   Dashboards offer immediate access to portfolio and service health and performance metrics, as well as who owns and manages the service.

    **Note:** In most cases, data is collected up to the previous day. If there is a current outage or incident, then data does not appear in trend charts or displays.

-   Comprehensive layout of all information related to a portfolio and its component services.

Service owners can access the workspace to perform their most common tasks, including:

-   View and manage owned IT services, as well as view all IT services the business manages.
-   Expand service lists to expose child services and service offerings.
-   Select a service to access pertinent information, including service trends, related services and information, improvement initiatives, and associated service offerings.
-   View and monitor service performance score reports, customers' scores, and total subscribers.
-   Monitor recent and upcoming changes.
-   Drill down into service offerings to view availability, SLA compliance, customer satisfaction, offering stability, performance scores, and more.
-   View associated unique or critical information about the service offering in the impact stream panel on the right side of the workspace. For example, you can view outages records with a unique **Outage Number** identifier. You can also see the outage number on the list view for outages via the **Outage** tab in the report viewer.

    **Note:** The Outage Numbering plugin \(com.snc.outage\_numbering\) must be activated to introduce number data. The plugin is automatically activated for all instances and upgrades except those that already have a number prefix column on the Outage table. Refer to the [Activate Outage Numbering plugin \[KB0823685\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0823685) article in the HI Knowledge Base or contact Customer Service and Support if the plugin is not active and you want to move to the base system field.


System administrators can configure the workspace according to the specific needs within the organization:

-   Disable particular metrics from displaying in the workspace.
-   Configure the metric weights that contribute to performance scores within the workspace.
-   Configure the metric thresholds for each metric that displays in the workspace.

Start here: [Access Service Owner Workspace](../task/access-service-owner-workspace.md).

