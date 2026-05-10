---
title: View service instances for a CI
description: For a selected CI, the Service instances panel in Unified Map lists details in the Service Mapping application for all associated service instances \(formerly application services\).
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View service instances for a CI

For a selected CI, the **Service instances** panel in Unified Map lists details in the Service Mapping application for all associated service instances \(formerly application services\).

## Before you begin

Service Mapping must be installed. For more information, see [Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/c_ServiceMappingOverview.md).

Role required:

-   To access maps: sn\_cmdb\_user, sn\_cmdb\_editor or sn\_cmdb\_admin
-   To access maps with operational service instances: app\_service\_user, and sm\_user or sm\_admin
-   To access maps with operational and non-operational service instances: app\_service\_admin, and sm\_user or sm\_admin
-   To access and view related items: itil

## About this task

The information that appears on a service instance card is described in [Service Mapping data](../reference/um-data-from-service-mapping.md).

## Procedure

1.  While working in a map, select a CI on the map and then select the Service Instances icon ![](../image/icon-um-app-services-panel.png).

    The panel displays a card with details for each related service instance.

    ![Service instances for the selected CI.](../image/um-app-services-panel.png)


## What to do next

-   Select another CI on the map to show its related service instances.
-   Select an empty space on the map to show all service instances for any of the CIs on the map.
-   In the **Service instances** \(formerly Application services\) panel:
    -   Use the Search box to search for a specific service instance.
    -   Select the Open filter icon ![](../image/icon-um-open-filter-panel.png) to open the filter panel, and then select a category and a sort order by which to sort the service instance cards. Close the filter panel to apply your settings.
-   On an individual service instance card, select the additional actions icon ![](../image/icon-um-additional-app-services.png) and then select one of the following options:

    -   Select **View CI details** to open the CI form for the service instance CI.
    -   Select **Open in new map** to open a new map in which the service instance is set as the home node.
    -   Select **Set CI as home** to set the service instance as the home node on the map and redraw the map accordingly.
    Some fields, such as **Business criticality**, are color-coded to denote specific values. For example, a status of Most Critical is highlighted with a red background.


**Related topics**  


[Service Mapping data that appears on maps](../reference/um-data-from-service-mapping.md)

