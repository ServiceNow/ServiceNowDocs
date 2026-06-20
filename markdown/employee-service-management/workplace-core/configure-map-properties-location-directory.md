---
title: Configure map properties for Location Directory
description: Configure map properties to enable reservation states, occupancy states, display permanent seat assignments, or auto-refresh time interval for showing the latest reservation and occupancy information on the map. Show or hide neighborhoods on the Location directory by using a map property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/workplace-core/configure-map-properties-location-directory.html
release: xanadu
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-04-22"
reading_time_minutes: 1
breadcrumb: [Manage workplace activities and services with Location directory, Request employee-related services, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Configure map properties for Location Directory

Configure map properties to enable reservation states, occupancy states, display permanent seat assignments, or auto-refresh time interval for showing the latest reservation and occupancy information on the map. Show or hide neighborhoods on the Location directory by using a map property.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Space mapping** &gt; **Map properties**.

2.  Configure the map properties for the Location directory.

    For more information about the map properties, see [Properties installed with Workplace Space Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/wsd-space-mapping-properties.md).

3.  Select **Save**.

    The updated map configuration properties are available on the Location directory.

4.  Display the name of a person reserving a space on the map by following these steps.

    1.  In the filter navigator, enter `sys_properties.list`.

    2.  Select the **sn\_wsd\_core.floor\_plan.portal.show\_reservation\_details** property.

    3.  Set the value of the property to **true** and save the record.


**Parent Topic:**[Manage workplace activities and services with Location directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown)

**Previous topic:**[Manage workplace activities and services with Location directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown)

**Next topic:**[Work with the Map view on the Location Directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/workplace-core/wsd-map-view-loc-directiory.md)

