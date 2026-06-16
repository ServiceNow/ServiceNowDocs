---
title: Workplace Reservations for Microsoft Outlook Add-in release notes
description: Version history for the Workplace Reservations for Microsoft Outlook Add-in application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-workplace-reservation-ms-outlook.html
release: store
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Reservations for Microsoft Outlook Add-in release notes

Version history for the Workplace Reservations for Microsoft Outlook Add-in application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.12.2 - August 2025**

    Increasing version number to align with the releases.

-   **Version 1.12.0 - May 2025**

    Fixed: Removed hardcoded colors to have better support for theming.

-   **Version 1.11.0 - February 2025**

    New: Support for Personal Authentication: Synchronize reservations made in Workplace Service Delivery to Microsoft Outlook using personal credentials of a workplace user.

-   **Version 1.10.0 - November 2024**
    -   Fixed:
        -   The message informing employees of when they can reserve a space was incorrect.
        -   The text box on extra services was not highlighted.
-   **Version 1.9.3 - August 2024**
    -   Changed: When opening the Outlook add-in, certain information is retrieved from Exchange Online, requiring the employee to wait. The data is now retrieved when saving the reservation, allowing the employee to use the add-in directly.
    -   Fixed: Item description was not loaded when opening an existing reservation with service in the add-in. This has been fixed.
-   **Version 1.9.0 - May 2024**
    -   New: You can now use the diagnostics tools to validate the Outlook add-in configuration.
    -   Fixed: Selecting more than 35 spaces for a single reservation created an error. This has been fixed now.
-   **Version 1.8.5 - February 2024**
    -   Fixed:
        -   Unable to see and add services to an existing reservation when created using the Outlook add-in.
        -   Employees cannot log in to the Outlook add-in using some clients and web browsers. After logging in, the login page is displayed again.
-   **Version 1.8.3 - November 2023**
    -   Fixed:
        -   Earlier, in a few cases, the performance of the Outlook client app was slow. This has been fixed now.
        -   Earlier, the label "Make space details private" was not translated. This has been fixed now.
-   **Version 1.8.0 - August 2023**
    -   New: Show descriptions added to services and service items while making or viewing a reservation.
    -   Fixed:
        -   Earlier, some messages informing the employee about the max days in the future were not translated after changing the language. This has been fixed.
        -   Accessibility improvements to ensure attribute IDs are unique, added names, updated labels, support for screen readers, and more.
-   **Version 1.7.0 - May 2023**
    -   New:
        -   Inform employees about existing and overlapping reservations while creating or editing an existing reservation of the same type.
        -   Inform employees when they are creating a reservation that is too far in the future.
    -   Fixed: Earlier, the privacy settings were not set accordingly when reserving a space. This has been fixed.
-   **Version 1.6.0 - February 2023**
    -   New: You can now allow employees to set their location privacy preferences while making a reservation.
    -   Changed: You can control the visibility when someone is searching for a space near a colleague or while using the location directory.
    -   Fixed:
        -   In a few cases, the add-in would not load while using the Microsoft Outlook web.
        -   Locations with services got canceled in the Microsoft Outlook add-in if the location was excluded from being visible
-   **Version 1.5.0 - December 2022**
    -   New:
        -   You can now exclude spaces and other locations \(e.g., virtual meeting link URLs\) from the Outlook add-in display.
    -   Fixed:
        -   Earlier, adding a virtual meeting link before opening the Outlook add-in resulted in the add-in remaining in the "Preparing the add-in" state. This has been fixed now.
        -   Earlier, the virtual meeting link would get removed while opening the Outlook add-in. This has been fixed now.
-   **Version 1.4.0 - November 2022**
    -   Changed: To retrieve the required information in order to search for available spaces and to add services to a reservation while using the Microsoft Outlook add-in, the system will now use GraphAPI instead of the soon-to-be deprecated Mircosoft Outlook REST APIs.
    -   Fixed: Earlier, the save option in the Microsoft Outlook add-in was not always enabled while removing a selected space from the reservation if it was created using Workplace Reservation Management. This has been fixed now.
-   **Version 1.3.0 - August 2022**
    -   Changed: Employees can select any type of space in the Outlook add-in when the spaces are synchronized with the calendar provider.
    -   Fixed:
        -   Earlier, the entire width of the service comment field was not always used for long texts.
        -   Earlier, while loading the add-in, an error was returned that retrieves mandatory information.
-   **Version 1.2.3 - May 2022**

    Changed: The version numbers of Workplace Reservations for Microsoft Outlook Add-in dependency applications have been updated.

-   **Version 1.2.1 - February 2022**
    -   New: You can request different types of space arrangements while scheduling a new reservation.
    -   Changed: The labels are updated to improve space searching.
    -   Fixed: All elements now support accessibility accordingly.
-   **Version 1.1.8 - December 2021**
    -   Fixed
        -   In some cases, an error was displayed while editing existing reservations.
        -   In some cases, the add-in needed to be reloaded to save the reservation after removing the recurring series.
        -   While making a reservation too far in the future \(according to the reservable module\), the reservation would get blocked without indicating any reason.
-   **Version 1.1.5 - October 2021**
    -   New: Additional support has been added to support all the 22 languages that are currently available across the ServiceNow AI Platform.
-   **Version 1.1.1 - September 2021**
    -   Fixed
        -   When saving the reservation, the add-in lost focus where it should have remained.
        -   Adding services to a reservation was not possible when the iCalId was not yet available.
-   **Version 1.0.2 - July 2021**
    -   New:
        -   Find available spaces by applying multiple search criteria.
        -   You can add spaces directly to the event, or let the add-in do this. If the selected spaces are no longer available or if the date or time has changed, the add-in will indicate the same.
        -   You can request extra services along with your reservation based on the available extra services menu card defined by workplace teams for each space. The extra services displayed in the add-in are the same as the ones available directly in the Workplace Service Delivery Suite.
        -   You can update existing reservations, add or change services, and select a different location. You can manage spaces and use the existing reporting tools to understand the demand directly from the Workplace Reservation Management application.

**Parent Topic:**[ServiceNow Store - Workplace Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-wsd-highlight.md)

