---
title: Enable favorites option for Workplace Service Portal
description: Enable employees to set a workplace location as their favorite while using the Workplace Service Portal. Integrate with Employee Service Center to configure the favorites option.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-core/confgure-favourites-option-for-ws-portal-wsd.html
release: australia
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Enable favorites option for Workplace Service Portal

Enable employees to set a workplace location as their favorite while using the Workplace Service Portal. Integrate with Employee Service Center to configure the favorites option.

## Before you begin

To enable the favorites option for Workplace Service Portal, verify that you have the latest versions of the following applications and plugins installed:

-   Employee Center Core \(sn\_ex\_sp\)
-   Employee Experience Taxonomy plugin \(sn\_ect\)
-   Employee Experience Foundation \(sn\_ex\_emp\_fd\)

Role required: esc\_admin or sn\_wsd\_core.admin

## About this task

Configure the favorites option so that employees can set any workplace location as their favorite. The employees can view their favorite locations anytime by selecting the **Favorites** tab on the Employee Center home page. The locations that they set as their favorite are given as the first priority when they search for available locations to make a reservation.

## Procedure

1.  Navigate to **All** &gt; **Favorites** &gt; **Favorite Content Configuration**.

2.  Verify that the following Content types are listed in the favorite Content Configuration form:

    -   Desks \(sn\_wsd\_core\_space\)
    -   Rooms \(sn\_wsd\_core\_rooms\)
3.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

4.  In the Service portals list, perform the following actions:

    1.  Go to **Workplace Services**.

    2.  In the **Enable favorites** column, set the option to **true**.


## Result

The favorites option is enabled for employees to set any workplace location as their favorite.

**Parent Topic:**[Manage workplace safety activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-core/manage-wsd-activites.md)

**Related topics**  


[Import your workspaces data from an Excel spreadsheet]()

[Add a space type configuration]()

[Configure a workplace card]()

[Block a workplace location]()

[Configure Workplace entity and entity types]()

[Managing Neighborhoods]()

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

