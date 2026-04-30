---
title: Explore Workplace Reservations for Microsoft Outlook Add-in
description: Reserve a workplace space in less than a minute without using the Reservation portal. The ServiceNow Workplace Reservations for Microsoft Outlook Add-in enables you to make a reservation using Microsoft Outlook directly.
locale: en-US
release: xanadu
product: Workplace Service Delivery
classification: workplace-service-delivery
topic_type: concept
last_updated: "2025-12-12"
reading_time_minutes: 4
breadcrumb: [Workplace Reservations for Microsoft Outlook Add-in, Workplace Service Delivery, Employee Service Management]
---

# Explore Workplace Reservations for Microsoft Outlook Add-in

Reserve a workplace space in less than a minute without using the Reservation portal. The ServiceNow® Workplace Reservations for Microsoft Outlook Add-in enables you to make a reservation using Microsoft Outlook directly.

**Note:** As of Workplace Reservation Management version 3.0.2, you are no longer required to install the Microsoft Outlook Add-in plugin. The advanced search widget in the Workplace Reservation Management 3.0.2 version is used for Outlook Add-in reservations. To use Microsoft Outlook Add-in, install and configure Workplace Calendar Synchronization. Administrators can configure the manifest add-in file to complement integration with Workplace Calendar Synchronization.

Workplace Reservation Management 3.0.2 manifest add-in file for Microsoft Outlook provides enhanced reservation experience and capabilities for employees. Employees can make reservations using multiple Reservable Modules. They can make multi-building, browse near a person, or neighborhood reservations. It provides advanced reservation web portal capabilities within the Microsoft Outlook Add-in manifest file.

Migrate or update to Workplace Reservation Management 3.0.2 version. For more information, see [Manage Workplace Reservations for Microsoft Outlook Add-in](../../wsd-reservation-management/concept/manage-outlook-addin-rsv.md).

The Workplace Reservations for Microsoft Outlook Add-in application is created on the Seismic workspace and uses Seismic components. The components are stored in the Workplace Service Delivery Components plugin to enhance the employee experience while using the add-in.

As an employee, you can easily reserve a space using Microsoft Outlook directly. The ServiceNow® Workplace Reservations for Microsoft Outlook Add-in provides you the capabilities of the Workplace Reservation Management application within the Microsoft Outlook application. The add-in enables an employee to create an appointment or edit an existing appointment. An employee can find the available spaces easily and request extra services without the need to open a separate application. Only the locations that exist in both the Microsoft Exchange Online and Workplace Reservation Management are displayed for reservation. Only rooms added in the Rooms \[sn\_wsd\_core\_room\] table are sychronized using the calendar provider. To synchronize spaces, that spaces must be added as rooms in the Rooms \[sn\_wsd\_core\_room\] table.

The add-in is displayed in the Microsoft Outlook ribbon. When you select the add-in icon, it displays a reservation form in a sidebar. You can configure a manifest file and upload it to the Microsoft Outlook application to view the add-in feature.

As a workplace admin, you can specify the reservable module that you want to use for reservations in the **sn\_wsd\_msaddin.default\_reservable\_module** system property. Only one reservable module can be used in the Workplace Reservations for Microsoft Outlook Add-in.

Only the workplace locations that are assigned to the reservable module are displayed to employees while making a reservation. All the reservations and the extra services requested by employees are managed within the Workplace Reservation Management application.

**Important:** The Workplace Reservations for Microsoft Outlook Add-in application does not support Microsoft Exchange On-Premises.

![Workplace reservations add-in window in the Microsoft Outlook application](../images/add-in-firstpage.png "Workplace Reservations add-in window in the Microsoft Outlook application")

## Workplace Reservation Management and the Microsoft Outlook Add-in

As an employee, the add-in enables you to make a reservation without using the Workplace Reservation Management Reservation portal, thus saving time. The add-in reduces the time to search for a location by directly displaying the available locations. The add-in enables you to perform the following actions:

-   Find available spaces by applying multiple search criteria.

    ![available spaces displayed by the add-in](../images/add-in-availablespaces.png "Available spaces displayed by the add-in")

-   Add spaces directly to an existing or a new event using the add-in directly.
-   Request a reservation for yourself or on behalf of others.
-   Make a reservation for any workplace location such as a conference room, parking lot, workspace, desk and more.
-   Make reservation on behalf of a visitor or to meet a visitor.
-   Specify the reservation duration.
-   Request extra services.

    ![extra services option in the add-in](../images/add-in-addextraservice.png "Extra services option in the add-in")

-   Update an existing reservation or modify the extra services. You can change the location and add/remove services.

If any selected space becomes unavailable for any reason or if the date or time has changed, the add-in indicates the same.

![unavailable space indicated by the add-in](../images/add-in-unavailablespace.png "Unavailable space indicated by the add-in")

You can use the existing reporting tools available with Workplace Reservation Management application to report any issue.

**Important:** Currently, it is not possible to use Microsoft Outlook on the web using the Apple Safari browser. Instead, you can use Mozilla Firefox or Google Chrome.

## Workplace Calendar Synchronization

You can also synchronize your reservations with your calendar provider by using the ServiceNow® Workplace Calendar Synchronization application. Enable your employees to make reservations with ServiceNow® Workplace Reservation Management or with your organization's calendar service providers, such as Microsoft Exchange Online.

For more information, refer the following:

-   [Explore Workplace Calendar Synchronization](../../workplace-calendar-synchronization/concept/workplace-calendar-synchronization-overview.md)
-   [Setup Workplace Calendar Synchronization](../../workplace-calendar-synchronization/concept/workplace-calendar-synchronization-setup.md)

