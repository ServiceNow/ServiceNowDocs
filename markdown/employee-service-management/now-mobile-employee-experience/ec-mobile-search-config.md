---
title: Update search configurations
description: Search configurations are not automatically updated when you install the Now Mobile application. Manually run the fix script that is provided to update the search configuration to experience unified browsing on your mobile device.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/now-mobile-employee-experience/ec-mobile-search-config.html
release: yokohama
product: Now Mobile - Employee Experience
classification: now-mobile-employee-experience
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure EC for Now Mobile, Now Mobile app, Unified Employee Experience, Employee Service Management]
---

# Update search configurations

Search configurations are not automatically updated when you install the Now Mobile application. Manually run the fix script that is provided to update the search configuration to experience unified browsing on your mobile device.

## Before you begin

Role required: admin

## Procedure

1.  In the Navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Create a property of type **true/false** in the Now Mobile application scope.

    For example, create a property `enable_taxonomy`. For more information on creating system properties, see Add a system property.

3.  Set the property value to **true**.

4.  Navigate to **System Definition** &gt; **Fix Scripts**.

5.  Search for `Enable Taxonomy For Mobile`script and click to open.

6.  Click **Run Fix Script** to update the search configuration.

    **Note:** If the default Employee Taxonomy is attached to the Mobile Service Portal, then run the **Set primary topics for Employee taxonomy** fix script to update the mappings.


**Parent Topic:**[Configuring Employee Center for Now Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-mobile-employee-experience/ec-mobile-configrations.md)

