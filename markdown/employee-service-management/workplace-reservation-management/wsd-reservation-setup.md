---
title: Configure Workplace Reservation Management portal
description: As a Workplace Reservation Management admin, you can decide what can be made reservable in the organization. You can add different types of reservable items in the application for employees to reserve.
locale: en-US
release: yokohama
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Configure Workplace Reservation Management portal

As a Workplace Reservation Management admin, you can decide what can be made reservable in the organization. You can add different types of reservable items in the application for employees to reserve.

You can configure what must be available in the application for reservation. You can configure the reservable modules displayed on the application.

The Reservation portal enables you to make a reservation and perform reservation-related actions. You can access the Reservation portal from the Workplace Reservation Management application and the Workplace Service Portal. For more information about the reservation portal, refer to [Make a reservation](reservation-portal.md).

As a Workplace Service Delivery admin, you can perform any action on the Workplace Reservation Management application. You can add reservable workplace items and perform other actions.

As a Workplace Reservation Management admin, the application enables you to perform the following actions:

-   Enable manager approvals on reservable modules for reservation.
-   Make reservations on behalf of others.
-   View all the reservations made.
-   Modify existing reservable modules.
-   Activate or de-activate reservable items and control its availability on the application.
-   Configure standard services.
-   Add reservable purpose on reservable items for employees to make easy selection.
-   Configure check-in and check-out requirement on a reservable module.
-   View the current state, synchronization state and the check-in state of a reservation.
-   View the source, sub-source, last updated source and last updated sub-source of the reservation.
-   If you have the Workplace Space Management application installed, you can specify if a cost center/department check is required to reserve the workplace item.
-   Create archiving rules. Select from archive rules provided by ServiceNow®.
-   Create and assign time slots to reservable modules that are configured for the Quick Reservation widget on the Workplace Service Portal
-   Configure the views of the reservable module such as Map view or Schedule view.
-   Enable group reservation on workplace items of a module.
-   Enable employees to download an iCalendar of a reservation.
-   Specify the search limit on a module.
-   Assign workplace locations that are allowed to be reserved in a reservable module.

-   **[Install Workplace Reservation Management](../task/install-wsd-reservation-mgmt.md)**  
Install the Workplace Reservation Management application from ServiceNow Store applications. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).
-   **[Add a workplace space for reservation](../task/add-reservable-items.md)**  
Add different types of workplace spaces like a workspace, desk, or similar spaces for employees to reserve.
-   **[Add a workplace room for reservation](../task/add-workplace-rooms.md)**  
Add a workplace room for employees to reserve.
-   **[Configure a reservable module](../task/config-reservable-module.md)**  
Create a Reservable Module to add a group of similar reservable workplace items. These workplace items are displayed in a single category on the Reservation portal.
-   **[Assign spaces to an area](../task/add-neighbourhood-spaces-to-an-area.md)**  
Add spaces to an area to make them available for reservation. On the Reservation portal, when an employee searches for an area, all the available spaces that are assigned to that area are displayed.
-   **[Create a standard service](../task/add-standard-services.md)**  
Create a Standard service to make it available to employees by default when they make a reservation.
-   **[Create a flexible service](../task/add-flexible-service.md)**  
Create a flexible service and provide it as an extra service to employees. Employees can use the flexible service and other basic standard services when they make a reservation.
-   **[Create a workplace service to provide an extra service for a reservation](../task/create-workplace-service-to-provide-extra-service.md)**  
Create a workplace service and provide it as an extra service to employees while making a reservation. Use the Workplace Case Management application to create the workplace service.
-   **[Create a reservable view](../task/create-a-reservable-view.md)**  
Configure a view that employees can view while making a reservation on the Reservation portal.
-   **[Create a user criteria record](../task/create-user-criteria.md)**  
Add a user criteria record to decide which users, roles, and groups can access a reservable module.
-   **[Configure a reservable purpose](../task/configure-reservable-purpose.md)**  
Create a purpose that describes the use of a workplace item. Add this purpose to a relevant workplace space or room so that the purpose is displayed on the reservation portal.
-   **[Create a quick reservation time slot](../task/add-reservable-time-slots.md)**  
Create a time slot for the reservable module that is available in the Quick Reservation widget on the reservation portal. When an employee wants to reserve a workplace item of that reservable module, the employee can select a suitable time slot instead of specifying a start and end times for the reservation.
-   **[Configure virtual meeting providers](../task/configure-virtual-meeting-providers.md)**  
Enable employees to provide a virtual meeting link with their reservation. Configure the virtual meeting providers so that the virtual meeting link of that provider is automatically generated when the employee makes a reservation.
-   **[Configure Microsoft Teams as virtual meeting provider](../task/configure-msteams-as-virtual-meeting-provider.md)**  
Set Microsoft Teams as your virtual meeting provider.
-   **[Connect Workplace Reservation Management with Microsoft Teams](../task/connect-rsv-mgmt-with-teams.md)**  
Establish connection between Microsoft Teams Communications and Workplace Reservation Management.
-   **[Connect Workplace Reservation Management with Zoom](../task/connect-rsv-mtm-with-zoom.md)**  
Establish connection between Zoom and Workplace Reservation Management.
-   **[Display permanent seat assignments on floor maps](../task/display-permanent-seats-on-maps.md)**  
Display permanent space assignments along with employee names on maps.
-   **[Display name of the person reserving a space](../task/displayname-person-booking-rsv.md)**  
Display the name of a person who booked a space on the floor map.
-   **[Manage check-in and check-out reservations](check-in-check-out-process.md)**  
Reservation check in and check- out reminders are managed through the Check-in and check out reminder scheduled jobs
-   **[Configure automatic check-in for reserved spaces](configure-rsv-check-in.md)**  
Configure automatic reservation check-in using the Occupancy state of a location or space. If a location is using occupancy data sensors, it checks for Occupancy state of each space in the Space Occupancy data table
-   **[Configure reservation multi-day settings in Reservable Module](rsv-config-rsv-mod-value.md)**  
Set the Max days in future value for configuring reservation.

**Parent Topic:**[Workplace Reservation Management](workplace-rsv-mgmt-feat.md)

