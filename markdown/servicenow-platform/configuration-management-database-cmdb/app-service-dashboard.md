---
title: Monitor the health of application services on the Application Services dashboard
description: Use insights from the Application Services dashboard to reduce the number of incomplete application services by populating them and adding missing data. To use application services effectively, ensure that application services are fully configured and are populated.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Monitor the health of application services on the Application Services dashboard

Use insights from the Application Services dashboard to reduce the number of incomplete application services by populating them and adding missing data. To use application services effectively, ensure that application services are fully configured and are populated.

## Before you begin

Role required: itil\_admin or app\_service\_admin

## About this task

The dashboard queries for Application Services by checking for those records in the Application Service \[cmdb\_ci\_service\_auto\] class in which the value of **Service classification** is **Application Service**. Reduce the number of incomplete application services by [editing application services](../../service-mapping/task/create-it-services.md) and populating any empty attributes. For example, if an application service isn't configured with a service population method, configure a service population method for the application service.

The Application Services dashboard is fully integrated into the [Insights view in CMDB Workspace](../concept/cmdb-workspace-insights-view.md) and refreshes on a 24-hour cycle during night hours.

## Procedure

1.  Follow either navigation step to access the Application Services dashboard:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **Insights** on the CMDB Workspace menu bar. On the Insights view, select the Application services tile.
    -   Navigate to **All** &gt; **CSDM** &gt; **Application Service Dashboard**.
2.  View the tiles on the Overview tab, which show application services in which basic configurations are incomplete.

    -   Total Application Services: Count of all application services, complete and incomplete.
    -   Population method defined: Count of application services for which a service population method is specified.
    -   Population method not defined: Count of application services missing a service population method. Data for the tags and top down discovery methods appear only if Service Mapping is installed.

        **Note:** Some population methods for application services are available only with [Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) and therefore won't appear in the tile if Service Mapping isn't installed.

    -   Application services types: Chart of application services by population methods such as Dynamic CI Group and Manual, including application services without a population method \(Empty\). The chart includes business services that were converted to application services.
    -   Application services missing data: Chart of application services by key data that is missing, such as service offering and owner. For example, the bar 'No Service Offering' shows application services without any relationship with a business service or a technical service.
3.  View counts on the Application service coverage tab, which shows application services in which other configurations are potentially incomplete.

    -   Application Servers: Total number of application servers. The number of those which aren't in any application service and a breakdown of those application servers by class.
    -   Databases: Total number of databases. The number of those which aren't in any application service and a breakdown of those databases by class.
    -   Hardware Servers: Total number of hardware servers. The number of those which aren't in any application service and a breakdown of those hardware servers by class.
    **Note:** Application servers, hardware servers, and databases, not included in application services, are counted only up to about 100,000, even if the actual count is greater than this limit. This number limit is determined by the value of the [glide.cmdb.csdm.app\_service.max\_results](../reference/components-installed-app-services.md) property.

4.  Select **Owned by**, **Support group**, or **Change Group** to filter the list of application services that are included in the dashboard, by a key attribute.

    A filter doesn't impact counts of application services in which the respective filter attribute is missing. For example, filtering by **Owner**, doesn't change the count of the Missing Owner card.

5.  Select a tile in either tab on the dashboard to drill down to the associated CIs list view.

    For example, select the Population method not defined tile to see the CIs list view of application services without a population method.


## What to do next

Update application services with any missing important details:

1.  Navigate to **CSDM** &gt; **Manage Technical Services** &gt; **Application Services**.
2.  In the Application Services list view, select an application service to edit.
3.  Add the missing details.

    For details about configuring an application service, see [Create application service](../../service-mapping/task/create-it-services.md).


