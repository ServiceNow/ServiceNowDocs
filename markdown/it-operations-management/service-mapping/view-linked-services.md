---
title: View dependent application services in classic Service Mapping
description: Check which application services depend on an application service and open maps for dependent application services.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Application service analysis and maintenance using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# View dependent application services in classic Service Mapping

Check which application services depend on an application service and open maps for dependent application services.

## Before you begin

Roles required: service\_mapping\_user

## About this task

The service that contains a reference to another application service, becomes a dependent service. The service that you include as a reference is a contained service.

![The map showing a contained service.](../image/linked-services-dependent-contained.png "Dependent service map with a reference to a contained application service")

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technical Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Right-click the entry point and select **Show dependent services**.

    The pop-up window displays the links to all dependent services for this application service.

3.  Select the link for the dependent service whose map you want to view.

    ![View dependent application services](../image/linked-services-show-dependent.png)

    The map window shows the map for the dependent service you selected.


**Parent Topic:**[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

**Related topics**  


[Link application services](link-services-to-services.md)

