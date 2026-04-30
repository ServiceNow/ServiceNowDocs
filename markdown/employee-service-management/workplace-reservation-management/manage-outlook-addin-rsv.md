---
title: Manage Workplace Reservations for Microsoft Outlook Add-in
description: Employees can create reservations using the Microsoft Outlook Add-in. They can calendar events or meetings to the Workplace Reservation Management 3.0.2 manifest add-in file.
locale: en-US
release: zurich
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: concept
last_updated: "2025-12-07"
reading_time_minutes: 2
breadcrumb: [Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Manage Workplace Reservations for Microsoft Outlook Add-in

Employees can create reservations using the Microsoft Outlook Add-in. They can calendar events or meetings to the Workplace Reservation Management 3.0.2 manifest add-in file.

As of Workplace Reservation Management version 3.0.2, you’re no longer required to install the Microsoft Outlook Add-in plugin. The advanced search widget in the Workplace Reservation Management 3.0.2 version is used for Outlook Add-in reservations. The advanced search widget in the Workplace Reservation Management 3.0.2 version is used for Microsoft Outlook Add-in reservations. To use Microsoft Outlook Add-in, install and configure Workplace Calendar Synchronization. Administrators can configure the manifest add-in file to complement integration with Workplace Calendar Synchronization.

Employees can enable advanced search to filter spaces, work with a reservable module, and make multi-building space selection. Employees can search for a space using the **Map** or **Card** options while making reservations. Employees can update current or existing reservations quickly by updating date, time, location, or workplace services.

When a meeting is created in Microsoft Outlook, the meeting event on the resource is synchronized with Workplace Reservation Management to create a reservation.

Workplace Reservation Management administrators can enable the Reservable module configuration for Microsoft Outlook Add-in. They can migrate or update existing Microsoft Outlook add-in version 1.12.2 or earlier versions to the latest Workplace Reservation Management 3.0.2 For more information, see [Configure Reservable Module for Microsoft Outlook](../task/config-rsv-module-outlook.md).

Employees can perform the following using Workplace Reservation Management 3.0.2.

**Note:** Shift-based, Reservable Modules aren’t supported for Microsoft Outlook add-in reservations. Group and recurring reservations are also not supported.

-   Create reservations using a Reservable Module \(for example Meeting rooms\).
-   Create reservations for multi-building and recurring reservations.
-   Select reservable paths based on the neighborhood or Browse near a person.
-   Invite colleagues or guests to a meeting or event.
-   Edit and update existing reservations.
-   Add workplace services and edit or remove them as required.

    Extra services \(catering, IT support, furniture arrangements, and so on\) can be configured and requested alongside workplace reservations.


Workplace calendar synchronization allows employees to use Calendar Providers \(MS Outlook or Google\) to create reservation records in Workplace Reservation Management. For more information, see [Microsoft Exchange Online - Calendar synchronization](../../workplace-calendar-synchronization/reference/ms-exchange-reservation-synchronization.md).

1.  [Configure Reservable Module for Microsoft Outlook](../task/config-rsv-module-outlook.md)  
Configure Reservable Module settings for Microsoft Outlook in Workplace Reservation Management version 3.0.2. Employees can create a meeting or an event in the Microsoft Outlook calendar, and reserve a space using the Workplace Reservation Management manifest add-in file.
2.  [Redirect WSD RSV MOA OAuth registry](../task/route-outlook-add-in.md)  
Redirect MOA Outh access \(moa\_login\) for Microsoft Outlook Add-in version 1.12.2 or earlier to WSD RSV MOA OAuth registry \(rsv\_moa\_login\) registry.
3.  [Activate the add-in for Microsoft Outlook](../task/add-outlook-addin.md)  
Workplace Reservation Management administrators can activate the manifest add-in for Microsoft Outlook. Add a manifest add-in file and customize it as per your requirements.

**Parent Topic:**[Workplace Reservation Management](workplace-rsv-mgmt-feat.md)

