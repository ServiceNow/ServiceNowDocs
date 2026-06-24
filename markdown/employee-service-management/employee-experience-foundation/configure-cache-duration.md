---
title: Configure cache duration for the user presence status
description: You can modify the system property to configure the cache duration to retain the user presence status of the Microsoft Teams user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/configure-cache-duration.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [User Presence Indicator, Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Configure cache duration for the user presence status

You can modify the system property to configure the cache duration to retain the user presence status of the Microsoft Teams user.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list` and press **Enter**.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

    \[Omitted image "sys-properties-0012.png"\] Alt text: System properties

2.  In the Name column, search for the system property `sn_tcm_collab_hook.teams.presence_status_cache_invalidate_duration` and click the property to view the property details.

    \[Omitted image "edit\_sys\_property\_0013.png"\] Alt text: Edit system property

3.  Click here to edit the property details.

4.  Define the cache duration in seconds to retain the user presence status in the **Value** field.

5.  Click **Update**.


**Parent Topic:**[User Presence Indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/user-presence-indicator.md)

