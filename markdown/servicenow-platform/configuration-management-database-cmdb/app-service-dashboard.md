---
title: Use Service instance \(Application Services\) dashboard to monitor health
description: Use insights from the Service instance dashboard to reduce the number of incomplete Service instances by populating them and adding missing data. To use service instances effectively, ensure that service instances are fully configured and are populated.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Service instances \(Application services\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Use Service instance \(Application Services\) dashboard to monitor health

Use insights from the Service instance dashboard to reduce the number of incomplete Service instances by populating them and adding missing data. To use service instances effectively, ensure that service instances are fully configured and are populated.

## Before you begin

Role required: sn\_cmdb\_admin, itil\_admin or app\_service\_admin

## About this task

The dashboard queries for service instances by checking for those records in the \[cmdb\_ci\_service\_auto\] class in which the value of **Service classification** is **Application Service**. Reduce the number of incomplete service instances by [editing application services](../../service-mapping/task/create-it-services.md) and populating any empty attributes. For example, if an application service isn't configured with a service population method, then configure a service population method for it.

The Service instance dashboard is fully integrated into the [Insights view in CMDB Workspace](../concept/cmdb-workspace-insights-view.md)and the [Service instances insights dashboard in Service Graph Workspace](../concept/sg-workspace-insights-serviceinstances.md), and refreshes on a 24-hour cycle during night hours.

## Procedure

1.  Follow either navigation step to access the Service instance dashboard:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **Insights** on the CMDB Workspace menu bar. On the Insights view, select the Application services tile.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**. Then, on the navigation panel select the Insights icon, and in the Insights navigation panel select **Service instances**.
    -   Navigate to **All** &gt; **CSDM** &gt; **Service instance dashboard**.
2.  View the tiles on the Overview tab, which show application services in which basic configurations are incomplete.

    -   Total Service instances: Count of all Service instances, complete and incomplete.
    -   Population method defined: Count of Service instances for which a service population method is specified.
    -   Population method not defined: Count of Service instances missing a service population method. Data for the tags and top down discovery methods appear only if Service Mapping is installed.

        **Note:** Some population methods for Service instances are available only with Service Mapping and therefore won't appear in the tile if Service Mapping isn't installed.

    -   Service instances types: Chart of Service instances by population methods such as Dynamic CI Group and Manual, including Service instances without a population method \(Empty\). The chart includes business services that were converted to Service instances.
    -   Service instances missing data: Chart of Service instances by key data that is missing, such as service offering and owner. For example, the bar 'No Service Offering' shows Service instances without any relationship with a business service or a technical service.
3.  View counts on the Service instance coverage tab, which shows Service instances in which other configurations are potentially incomplete.

    -   Application Servers: Total number of application servers. The number of those which aren't in any Service instances and a breakdown of those application servers by class.
    -   Databases: Total number of databases. The number of those which aren't in any Service instances and a breakdown of those databases by class.
    -   Hardware Servers: Total number of hardware servers. The number of those which aren't in any Service instances and a breakdown of those hardware servers by class.
    **Note:** Application servers, hardware servers, and databases, not included in Service instances, are counted only up to about 100,000, even if the actual count is greater than this limit. This number limit is determined by the value of the [glide.cmdb.csdm.app\_service.max\_results](../reference/components-installed-app-services.md) property.

4.  Select **Owned by**, **Support group**, or **Change Group** to filter the list of Service instances that are included in the dashboard, by a key attribute.

    A filter doesn't impact counts of Service instances in which the respective filter attribute is missing. For example, filtering by **Owner**, doesn't change the count of the Missing Owner card.

5.  Select a tile in either tab on the dashboard to drill down to the associated CIs list view.

    For example, select the Population method not defined tile to see the CIs list view of Service instances without a population method.


## What to do next

Update Service instances with any missing important details:

1.  Navigate to **CSDM** &gt; **Manage Technology Management Services** &gt; **Service instance**.
2.  In the Service instances list view, select a Service instances to edit.
3.  Add the missing details.

    For details about configuring a Service instances, see [Create Service instance \(application service\)](../../service-mapping/task/create-it-services.md).


