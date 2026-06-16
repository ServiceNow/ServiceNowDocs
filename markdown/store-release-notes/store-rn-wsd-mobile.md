---
title: Workplace Service Delivery for Mobile release notes
description: Version history for the Workplace Service Delivery for Mobile application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-mobile.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Service Delivery for Mobile release notes

Version history for the Workplace Service Delivery for Mobile application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.17.5 - June 2026**

    Fixed: Checking the all-day toggle did not always show results

-   **Version 1.17.0 - March 2026**

    Fixed: Duplicate reservations were displayed after selecting a colleague when selecting a space while browsing near a person.

-   **Version 1.16.2 - December 2025**
    -   Fixed:
        -   A building was pre-selected even when it was not part of the selected reservable module.
        -   Sometimes, it is not possible to remove the building using the responsive reservation experience.
        -   It was not possible to select more than three spaces using the responsive reservation experience.
        -   The floor was not cleared after changing or clearing the building in the different paths, resulting in empty search queries.
        -   Floor options were based on the path and not on the selected neighborhood.
        -   iCalendar files could not be downloaded.
        -   Enhancements to how restricted neighborhoods were handled.
        -   Enhanced the alignment of the X-icon in the building field.
-   **Version 1.16.0 - August 2025**
    -   New:
        -   Reserve multiple days using suggested spaces in the mobile Workplace experience.
        -   Edit reservations using suggested spaces in the mobile Workplace experience.
        -   View planned reservations in the mobile Workplace experience.
    -   Changed: Use the new neighborhood tables, which are part of Workplace Core.
    -   Fixed: There was an empty record in the quick action button in the Now Mobile App configuration.
-   **Version 1.15.0 - May 2025**
    -   Fixed:
        -   When making a reservation, a location input field was displayed instead of the available spaces after selecting a space and pressing next.
        -   The status for the requested extra services was truncated on the reservation summary page when viewed on a mobile browser.
        -   Employees could select multiple locations when editing an occurrence in a recurring series.
        -   Employees could not select any available areas when editing an existing reservation created through "browse by area".
        -   In some cases, the employee could not see any available spaces after selecting the building, start and end times, and proceed with next.
        -   Certain mobile push notifications were not linked to the correct page in Workplace Reservation Management.
-   **Version 1.14.0 - February 2025**
    -   Fixed:
        -   No result was displayed while searching for an available space on future date when the all-day configuration was set to default.
        -   In some cases, both desks and meeting rooms were displayed when selecting a reservable module created to reserve desks.
        -   When using the space details page, employees could not search for availability when the number of occurrences was set to one.
        -   Employees could see "Make subject private" using the quick reservation page, even when "display sensitivity" was disabled.
-   **Version 1.13.0 - November 2024**
    -   New: Allow employees to browse the locations, select spaces, see neighborhoods, and get directions on the go. Employees can now use the location directory on their mobile devices.
    -   Fixed:
        -   The floor field was empty when browsing within favorites
        -   Reserving desks from mobile was using UTC regardless of the specified timezone when All Day reservation was selected.
-   **Version 1.12.4 - August 2024**
    -   Changed: Updated the text labels for the push messages when an employee is to expected to check-in while using occupancy sensors.
    -   Fixed:
        -   My reservations screen was not sorted start \(a-z\) by default. This has been fixed.
        -   Searching for a space near a colleague returned an error while using the indoor map. This has been fixed.
-   **Version 1.12.0 - June 2024**
    -   New: Search for spaces based on the standard services, or their location purpose.
    -   Changed: Viewing related items will now also show the reserved space when only one space is part of the reservation.
    -   Fixed:
        -   Floor criteria were still considered in the search results of available spaces when the criteria were removed while managing an existing reservation. This has been fixed.
        -   Employees could try to reserve a space for longer than the maximum allowed duration after scanning a QR code. This has been fixed now.
        -   The Building field does not default when using the "Browse favorites" option.
-   **Version 1.11.3 - May 2024**

    No new features. The new version is released to manage dependencies with other applications.

-   **Version 1.11.0 - February 2024**
    -   New:
        -   Reserve a space after scanning QR code
        -   Make all-day reservations directly from mobile.
        -   Automatically pre-fill the employee's name who creates the reservation in the "Requested for" field.
    -   Changed: Control per reservable module if employees can reserve a space using the map or a list or if the map is always used.
    -   Fixed: "Requested for" is not updated to the selected employee when editing a multi-location reservation.
-   **Version 1.9.0 - November 2023**
    -   New: Reserve spaces covering multiple days. Employees are informed of the maximum duration of the reservation while selecting the type of space.
    -   Changed: Updated the default text to inform employees of the maximum number of days a reservation can be created in the future.
    -   Fixed: Improved support for theming.
-   **Version 1.8.5 - August 2023**
    -   Changed: Improve support for dark theme on mobile
    -   Fixed:
        -   Earlier, the text and icons to add another building or show filters on the mobile responsive experience had the incorrect color. This has been fixed.
        -   Earlier, viewing a case on mobile could result in the "Error applying UI rules". This has been fixed.
-   **Version 1.8.0 - May 2023**
    -   New:
        -   Enable employees to reserve a space in neighborhoods assigned to them.
        -   Inform employees of how many days in the future they can make a reservation.
        -   Inform employees about existing and overlapping reservations while creating or editing an existing reservation of the same type.
        -   Employees can view the optional message added to the reservation when opening an existing reservation.
-   **Version 1.7.0 - February 2023**
    -   New: Allow employees to provide their location privacy preference on reservations.
    -   Changed: Update experience to support next experience for native mobile and responsive-web.
    -   Fixed: Earlier, when adding a favorite space could result in an error. This has been fixed now.
-   **Version 1.6.1 - November 2022**
    -   New: Search for a space\(Campus, Building, Space\) using AI Search technology. See space details, raise a case and find directions to the space using Indoor Mapping.
    -   Changed: Favorite spaces will not be shown in the Map View of the "Browse All" reservations flow. To reserve favorite spaces, use "Browse By Favourites" which shows the favorite spaces in Card View and Map View.
    -   Fixed: Earlier, the option to add a virtual meeting to a reservation was always visible when completing the reservation. This has been fixed now.
-   **Version 1.5.1 - August 2022**
    -   New:
        -   Create a reservation using the Indoor Mapping solution.
        -   Use the location directory to find and navigate to a colleague or a space.
        -   Reserve your favorite spaces using the new reservation path.
        -   Send Push Notifications to mobile devices to alert employees about their upcoming workplace reservation-related events; ready to check-in, reservation is about to start, and more.
            -   Several notifications are actionable. For example, when the reservation is ready for check-in.
        -   Mandatory information will be prefilled while searching for available space and can be updated by the employee if required.
            -   Information is prefilled based on the workplace profile or the last created reservation.
    -   Changed: General usability improvements while making a reservation
    -   Fixed: When making a reservation, the last used building and floor were not saved for the next use.
-   **Version 1.3.4 - July 2022**
    -   Fixed:
        -   The toggle to show the floor map when editing an existing reservation was always active.
        -   The spaces were not visible on the floor map while creating a new reservation.
-   **Version 1.3.2 - May 2022**
    -   New:
        -   Employees can find the availability of spaces when reserving near a colleague or within an area. They can reserve the space using a floor map.
        -   Employees can now edit reservations using a floor map.
        -   Employees can now add a virtual meeting link to their reservation to plan a hybrid reservation.
-   **Version 1.2.1 - February 2022**
    -   New:
        -   Employees can find the availability of spaces and reserve a space using a floor map.
            -   They can search for available spaces by scrolling over the map.
            -   They can select a suitable space and make a reservation.
        -   Employees can reserve spaces in their area by using the new reservation path.
-   **Version 1.1.2 - December 2021**
    -   New:
        -   Find the quickest route to your location by using the indoor wayfinding in Now Mobile.
        -   Find and reserve an available space near a colleague.
        -   Reserve multiple spaces in one go using Workplace Reservation Management in Now Mobile.
        -   As an employee, you can now scan a QR code to create a case or check-in / check-out a reservation without hassle.
        -   Share your reservation details with your team members.
        -   After selecting the type of space that you want to reserve, the system automatically displays a suitable space that you can reserve with just a click.
-   **Version 1.0.3 - September 2021**

    ServiceNow® Workplace Service Delivery for Mobile brings the capabilities of Workplace Reservation Management within the ServiceNow AI Platform natively to mobile. An employee can search, reserve, modify, and check-in a reservation directly using their mobile device and sync it back to Workplace Service Delivery.


**Parent Topic:**[ServiceNow Store - Workplace Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-wsd-highlight.md)

