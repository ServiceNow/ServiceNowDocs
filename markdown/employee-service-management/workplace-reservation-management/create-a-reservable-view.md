---
title: Create a reservable view
description: Configure a view that employees can view while making a reservation on the Reservation portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/create-a-reservable-view.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create a reservable view

Configure a view that employees can view while making a reservation on the Reservation portal.

## Before you begin

The following reservable views are available with the Workplace Reservation Management application:

-   card
-   map
-   schedule

To view workplace items in the above views while making a reservation, configure the reservable module to use the reservable views. For more information, refer to [Configure a reservable view on a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/configure-rsv-view-of-cnfig-module.md).

**Note:** The Workplace Reservation Management application does not support DXF maps.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Reservable Views**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the view.|
    |Label|Label with which this reservable view is displayed on the Reservation portal.|
    |Application|Application of the reservable view. This field is automatically set. Ensure that **Workplace Reservation Management** is selected.|
    |Icon class name|Icon class name of the reservable view.|
    |Active|Option to activate the reservable view.|

4.  Click **Submit**.


## Result

The reservable view is added.

## What to do next

Add the view to a reservable module. The workplace items of the reservable module to which the view is added will be displayed in that view. For more information, refer to.

-   **[Configure a reservable view on a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/configure-rsv-view-of-cnfig-module.md)**  
Assign different views on a reservable mobile. The workplace items of the module can be viewed in the configured views while making a reservation on the Reservation portal.

**Parent Topic:**[Configure Workplace Reservation Management portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management]()

[Add a workplace space for reservation]()

[Add a workplace room for reservation]()

[Configure a reservable module]()

[Assign spaces to an area]()

[Create a standard service]()

[Create a flexible service]()

[Create a workplace service to provide an extra service for a reservation]()

[Create a user criteria record]()

[Configure a reservable purpose]()

[Create a quick reservation time slot]()

[Configure virtual meeting providers]()

[Configure Microsoft Teams as virtual meeting provider]()

[Connect Workplace Reservation Management with Microsoft Teams]()

[Connect Workplace Reservation Management with Zoom]()

[Display permanent seat assignments on floor maps]()

[Display name of the person reserving a space]()

[Manage check-in and check-out reservations]()

[Configure automatic check-in for reserved spaces]()

[Configure reservation multi-day settings in Reservable Module]()

