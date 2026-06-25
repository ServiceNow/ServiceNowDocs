---
title: Block a workplace location
description: Block a workplace location for a specific period. The blocked workplace location is unavailable during the specified period for any type of reservation on the Workplace Reservation Management Reservation portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-core/block-workplace-location.html
release: australia
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Block a workplace location

Block a workplace location for a specific period. The blocked workplace location is unavailable during the specified period for any type of reservation on the Workplace Reservation Management Reservation portal.

## Before you begin

**Note:** The blocked location is unavailable only on the Workplace Reservation Management Reservation portal for reservation.

Role required: sn\_wsd\_core.admin

## About this task

You can block a workplace location, such as a region, a site, a campus, a building, a floor, an area, a room, or a space. When you block a location, the location is unavailable for any type of reservation on the Workplace Reservation Management Reservation portal. Because of the block action, any existing reservations made on the workplace location are automatically canceled.

You can also block a location directly. Open the location and select the **Block location** option on the form.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Administration** &gt; **Block location**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|Number of the location. This field is automatically set.|
    |Location|Location that you want to block.|
    |Opened by|User who is blocking the location.|
    |Reason|Reason for blocking the location. Select from a list of available options.|
    |Comment|Comment that explains the reason for blocking the location or any important information.|
    |Active|Option to activate the block action.|
    |Progress state|Current progress state of the block action.|
    |Start time|Start time of the block.|
    |End time|End time of the block.|

4.  Select **Submit**.


## Result

The workplace location is blocked for the specified period. You can’t make any reservations for the location on the Workplace Reservation Management Reservation portal during this period. All existing reservations that are made on the workplace location are canceled.

**Parent Topic:**[Manage workplace safety activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/manage-wsd-activites.md)

**Related topics**  


[Import your workspaces data from an Excel spreadsheet]()

[Add a space type configuration]()

[Configure a workplace card]()

[Configure Workplace entity and entity types]()

[Managing Neighborhoods]()

[Enable favorites option for Workplace Service Portal]()

[Create a workplace performer criteria]()

[Mapping employees to their designated workspaces]()

[Assign the workplace user role to employees]()

[Configuring shifts for your workplace]()

[Managing workplace shifts that you own]()

[Managing workplace reservations for employees]()

[Setting and tracking arrivals at the workplace]()

[Approve employee workplace reservation requests]()

[Managing workplace tasks]()

[Workplace knowledge management]()

[QR code management]()

[Location migration]()

[View workplace service usage analytics with Usage Insights]()

