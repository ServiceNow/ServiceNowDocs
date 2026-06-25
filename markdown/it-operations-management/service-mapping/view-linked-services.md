---
title: View dependent application services in classic Service Mapping
description: Check which application services depend on an application service and open maps for dependent application services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/view-linked-services.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application service analysis and maintenance using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# View dependent application services in classic Service Mapping

Check which application services depend on an application service and open maps for dependent application services.

## Before you begin

Roles required: service\_mapping\_user

## About this task

The service that contains a reference to another service instance, becomes a dependent service. The service that you include as a reference is a contained service.

\[Omitted image "linked-services-dependent-contained.png"\] Alt text: The map showing a contained service.

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Right-click the entry point and select **Show dependent services**.

    The pop-up window displays the links to all dependent services for this application service.

3.  Select the link for the dependent service whose map you want to view.

    \[Omitted image "linked-services-show-dependent.png"\] Alt text: View dependent application services

    The map window shows the map for the dependent service you selected.


**Parent Topic:**[Application service analysis and maintenance using classic Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/c_SvcPlanningAndAnalysisUsingMaps.md)

**Related topics**  


[Link application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/link-services-to-services.md)

