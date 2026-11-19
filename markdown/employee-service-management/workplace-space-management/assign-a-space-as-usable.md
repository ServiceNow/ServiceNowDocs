---
title: Configure a space type as usable with Workplace Space Management
description: Specify if a space type is usable or not by using the Space type configuration functionality. Specify if the space can or cannot be used for reservations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-space-management/assign-a-space-as-usable.html
release: brazil
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Manage, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Configure a space type as usable with Workplace Space Management

Specify if a space type is usable or not by using the Space type configuration functionality. Specify if the space can or cannot be used for reservations.

## Before you begin

Ensure that you have the following:

-   The space type is configured in the application. Otherwise, refer to [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/workplace-core/add-space-type-configuration-wsd.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/workplace-core/add-space-type-configuration-wsd.md).
-   Workplace Space Management is installed.

Role required: sn\_wsd\_spcmgmt.manager

## About this task

Configure a space type as usable. Specify if the space type can be used for reservations or for any space-related planning. The space type is not usable if it is a storage space or a standalone space that cannot be reserved nor included in space-related activities.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Administration** &gt; **Space type configuration**.

2.  Select the space type that you want to configure as usable.

3.  Open the form in the Space Management view.

    1.  Right-click the form header.

    2.  Select **View** &gt; **Space Management**.

        The form view changes.

4.  Select the **Usable** check box to enable the feature.

5.  Select **Update**.


## Result

The space type is configured as usable.

The size of all the spaces that are assigned to this space type is calculated in the **Usable size** fields of their areas, floors, and buildings.

**Parent Topic:**[Managing workplace locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/workplace-space-management/Creating-workplace-location-records-using-spce-mgmt.md)

**Related topics**  


[Add a campus]()

[Add a building using Workplace Space Management]()

[Add a floor using Workplace Space Management]()

[Add an area using Workplace Space Management]()

[Add a room using Workplace Space Management]()

[Add a space using Workplace Space Management]()

[Allocate a cost center, department, or workplace entity]()

[Configure a workspace or desk as flexible or permanent]()

[Update the measurement details of a workplace location]()

[Change the status of a workplace location]()

[Configure a BOMA type]()

[Map a space type with BOMA type]()

[Create a Space Recommender rule]()

[Raise a space assistance request]()

[Create a view-by configuration]()

[]()

[Reviewing allocation changes]()

