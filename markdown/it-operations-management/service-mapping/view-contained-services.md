---
title: View contained application services in classic Service Mapping
description: A contained application service is a reference included into another, dependent application service. You can open the contained service map directly from within the dependent service map.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application service analysis and maintenance using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# View contained application services in classic Service Mapping

A contained application service is a reference included into another, dependent application service. You can open the contained service map directly from within the dependent service map.

## Before you begin

Roles required: service\_mapping\_user

## About this task

The service that contains a reference to another service instance, becomes a dependent service. The service that you include as a reference is a contained service.

![Map showing a contained service.](../image/linked-services-dependent-contained.png "Dependent service map with a reference to a contained application service")

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  Right-click the CI that is the contained service, and select **Show contained service**.

    The map shows an automatic redirection to the web address for the contained service. No additional tabs need to open.


**Parent Topic:**[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

