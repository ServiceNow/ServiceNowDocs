---
title: Configure the location search bar visibility on the map
description: Configure the visibility of the location search bar on the map widget when reporting a Health and Safety incident or observation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/health-and-safety-incident-management/hs-configure-property-hide-map-location.html
release: australia
product: Health and Safety Incident Management
classification: health-and-safety-incident-management
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 1
breadcrumb: [Configure, Health and Safety Incident Management, Health and Safety, Employee Service Management]
---

# Configure the location search bar visibility on the map

Configure the visibility of the location search bar on the map widget when reporting a Health and Safety incident or observation.

## Before you begin

Role required: sn\_ohs\_im.admin

## About this task

The location search bar on the map is used to find the exact location of the incident or observation. For more information on using location search while submitting an incident, see [Submit a safety incident as an employee](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-incident-management/submit-hs-incident-observation.md).

Use this configuration to hide the search bar for users who prefer to set a location by selecting directly on the map.

To enable the map component in the Health and Safety Workspace install the geomap component \[sn\_geo\_map\] plugin. For more information, see [Additional features in Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-incident-management/install-hs-incident-mgmt.md).

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety administration** &gt; **Properties**.

2.  In the **Show location search on map** property, select **Yes** to display the search bar, or **No** to hide it.

    The property is set to **Yes** by default.

3.  Select **Save**.


## Result

-   The property is applied to the map widget on the **Add event details** playbook step of the Health and Safety incident and observation form. For more information on working on a safety incident, see [Work on a safety incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-incident-management/work-hs-incident-observation.md).
-   When set to **No** the search bar is hidden and users can still set a location by selecting the map directly.

**Parent Topic:**[Setting up Health and Safety Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-incident-management/setting-up-hs-incident-mgmt.md)

