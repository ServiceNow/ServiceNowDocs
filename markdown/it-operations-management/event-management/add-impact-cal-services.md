---
title: Add application services for impact calculation
description: Specify the application services that must be considered during impact calculation to ensure accurate service impact assessment.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Alert impact calculation, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Add application services for impact calculation

Specify the application services that must be considered during impact calculation to ensure accurate service impact assessment.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

Organizations may have thousands—or even hundreds of thousands—of application services. If a CMDB class is added to the em\_impact\_inclusion\_class.list table, then all application services related to that class are included in impact calculation. However, there are two possible scenarios:

-   Scenario 1: CMDB class is added to em\_impact\_inclusion\_class.list but you want only specific services to be considered for impact calculation. You can either:

    -   Remove the unwanted services from the em\_impact\_filter\_service.list, or
    -   Set their status to false in the em\_impact\_filter\_service.list.
    For information on how to remove the application service from the list, see [Remove application services from impact calculation](remove-impact-cal-services.md).

-   Scenario 2: CMDB class is not added to em\_impact\_inclusion\_class.list. So, none of the application services related to this class are considered for impact calculation. However, you want only specific application services from this class to be included, you can directly add those services to the em\_impact\_filter\_service.list table and set their status to true without adding the CMDB class to the em\_impact\_inclusion\_class.list table.

The following procedure shows how to add an application service directly to the em\_impact\_filter\_service.list table so that it is considered for impact calculation.

## Procedure

1.  Navigate to **All** and search for `em_impact_filter_service.list`.

    The Impact Filter Services page opens.

    ![A list of application services that are included in impact calculation.](../image/em-impact-cal-app-services-list.png)

2.  Select **New**.

    ![Impact Filter Service details page.](../image/em-impact-cal-app-services-new.png)

3.  In the **Service** field, select the search icon \(![search icon](../../../common/image/List_SearchIcon.png)\).

    **Note:** By default, the **Calculate impact** check box is selected.

4.  In the Service Instances page, select the service that you want to add for the impact calculation.

    ![Service Instances page to select a service.](../image/em-impact-cal-app-service-selection.png)

5.  Select **Submit**.

    The application service adds to the list of impact filter services.

    ![The selected application service is added.](../image/em-impact-cal-app-services-added.png)

    **Note:** Only the application services added to the Impact Filter Services list appear in the [Service Dashboard](worksplace-view-service-details.md).


