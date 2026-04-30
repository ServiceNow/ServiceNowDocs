---
title: Set the default validation option for service locations
description: Set the default validation option that will be used when adding locations to a work order or work order task.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service with Service Locations, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Set the default validation option for service locations

Set the default validation option that will be used when adding locations to a work order or work order task.

## Before you begin

Set the **sn\_fsm\_service\_loc.max\_new\_location\_per\_day** property to limit the addition of service locations per day. For more information, see [Set the limit of maximum service locations added per day](set-max-locations-limit.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Configuration**.

2.  On the Field Service Configuration page, navigate to **Add-ons** &gt; **Service Locations**.

3.  In the **Validation** field, choose the default validation option.

    -   **Using map**: Add locations using a Google map interface. For information about selecting the default location when the map is opened, see [Set the default location on a map](set-default-location-while-using-map.md).
    -   **Without map**: Provide location details to add locations without map. The location details will be validated using the global.ServiceLocationAddressValidationExtPoint API.
    -   **No validation**: The provided location details will not be validated.
4.  Click **Save**.


