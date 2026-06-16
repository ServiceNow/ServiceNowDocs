---
title: Workplace Indoor Mapping release notes
description: Version history for the Workplace Indoor Mapping application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-workplace-indoor-mapping.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Indoor Mapping release notes

Version history for the Workplace Indoor Mapping application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.18.5 - June 2026**
    -   Fixed:
        -   Fixed an issue where the Directions button was missing from the map in the Kiosk experience.
        -   Fixed an issue where filters remained visible in the Location Directory card view when filter persistence was disabled.
-   **Version 1.18.2 - May 2026**

    Fixed: Applied security fixes.

-   **Version 1.18.1 - March 2026**
    -   New:
        -   Introduced vector-based PDF export for floor plans
        -   Added a PDF configuration interface with Map Content and Page Layout panels
        -   Enabled configurable data layers in exports, including departments, occupancy, space types, neighborhoods, user assignments, and cost centers
        -   Introduced configurable data layers from the Space and Space Details tables, with an advanced mode for additional tables
        -   Added page layout controls, including paper size, orientation, scale, offsets, font size, text color, and legend placement
        -   Included live preview with a regenerate option prior to download
    -   Fixed:
        -   Improved manual WSD sync performance for large campuses
        -   Resolved an issue in Enhanced WSD Sync where properties were not syncing across multiple columns
-   **Version 1.17.4 - December 2025**
    -   New:
        -   Added the ability to configure which data is displayed by default on the kiosk map.
        -   Added a button to reset the kiosk map camera to its default configuration.
        -   Added the ability to reserve spaces directly from the kiosk map.
    -   Changed: Updated location directory behavior so loading the map based on user assignment now works for campus, building, and floor assignments \(not only space-level assignments\).
-   **Version 1.16.5 - September 2025**
    -   Changed:
        -   Users can no longer zoom out beyond the campus boundary on Kiosk maps.
        -   The map maintains its default orientation and no longer rotates to north during wayfinding.
    -   Fixed: Issue where some buildings were not appearing in the Location Directory.
-   **Version 1.16.3 - August 2025**
    -   New:
        -   Location directory improvements:
            -   Enabled Neighborhood search.
            -   Enabled search for users assigned to specific neighborhoods.
            -   Added ability for users to change wayfinding units.
            -   Introduced step-by-step wayfinding directions.
            -   Added support for displaying neighborhoods via URL parameters.
        -   Automated Data Synchronization from Indoor Mapping to WSD
            -   Automated creation of new buildings, floors and spaces \(following initial manual sync\).
            -   Automated updates to campuses, buildings, floors, spaces and CAD attribute values.
            -   Automated retirement of buildings, floors and spaces.
            -   Introduced approval step to confirm retirements.
        -   Bidirectional Data Synchronization now available from WSD to Indoor Mapping
            -   Enabled updates to campus, building, floor and space names.
            -   Enabled updates to campus, building, floor and space titles.
            -   Enabled space type updates.
            -   Enabled deactivation of campuses, buildings, floors and spaces.
            -   Introduced approval step to confirm deactivations.
    -   Changed: Updated filters to show values only from the currently displayed floor.
    -   Fixed: Space filter no longer displays inactive space types.
-   **Version 1.14.1 - May 2025**
    -   Changed: In the location directory, the Reserve button has been removed from the space details card when space is unavailable.
    -   Fixed:
        -   Floor display order had been corrected in the floor controller for floors 10 and above.
        -   Resolved an issue where the location directory failed to load after the February upgrade due to user preferences.
        -   Resolved an issue with the display of occupancy data on certain spaces.
-   **Version 1.13.0 - February 2025**
    -   New:
        -   Location directory improvements:
            -   Option to display the names of employees who booked a space on the map.
            -   Ability to display both permanent seat assignments and the names of employees who booked a space on the map simultaneously.
            -   Ability to open a campus map based on an employee's workplace profile location.
        -   Indoor mapping for kiosk:
            -   Admin experience: Configure floor plans for kiosks with options to define map zoom levels, orientation, location pins and enable features such as wayfinding, filters, employee name display, and raising a case.
            -   End-user Experience: Introduction of a new UI dedicated to kiosk interactions.
    -   Changed:
        -   The page loader no longer appears when staying on the same floor in the Location Directory.
        -   Filters are now consolidated in a side panel, including neighborhood filtering, which has been removed from the legend.
    -   Fixed: Improved loading time when searching for a space in the Location Directory.
    -   Removed: Filter pills previously displayed at the top of the screen.
-   **Version 1.11.1 - November 2024**
    -   New:
        -   Improvements to Location Directory maps
            -   Larger maps make viewing and interacting with spaces on the map easier.
            -   View all neighborhoods on the map and filter out ones you are not interested in.
    -   Fixed: Accessibility improvements have been made. Improved support for keyboard, added IDs, alt text, contrast ratio, support for screen readers, and more.
-   **Version 1.8.0 - August 2024**
    -   New:
        -   Improvements to Location Directory maps
            -   Refresh button to fetch latest reservation and occupancy details on the map
            -   Auto refresh functionality to automatically fetch latest reservation and occupancy details at pre defined intervals
            -   New filters to filter spaces based on reservation \(booked, available\) and occupancy \(occupied, not occupied\) status
    -   Changed:
        -   Improvements to Location Directory maps
            -   Colors and icons on the map to indicate reservation and occupancy status
-   **Version 1.7.0 - May 2024**
    -   New: The synchronization between Indoor Mapping and Workplace Service Delivery now also populates the coordinate fields for campuses, buildings, floors, and space tables of the Workplace core.
    -   Fixed: Fixed location directory space type filter that returned no results.
-   **Version 1.6.0 - February 2024**

    New: Display employee names for permanent seat assignments on employee portal maps.

-   **Version 1.5.3 - November 2023**
    -   Fixed:
        -   Reservation search map view was showing incorrect color coding after space was unlinked. This has been fixed.
        -   The space details card was not showing on the map when searching for a user with an active reservation. This has been fixed
        -   The 'unselect all' link of the reservation page map did not respond when several elements were selected. This is no longer the case.
-   **Version 1.5.0 - August 2023**

    New: Ability to compute room surface from AutoCAD file and retrieve the value to populate the relevant space table column.

-   **Version 1.4.0 - May 2023**

    New:

    -   Indoor Mapping to WSD Synchronization script now supports delete operations
    -   A new step has been added to the Synchronization Script to visualize place type to space type mappings.
    -   Introducing the ability to configure notifications to remind users when the script needs to be launched.
-   **Version 1.3.0 - February 2023**
    -   New
        -   Ability to extract CAD values and configure which WSD Space column they should populate
        -   Migration of Indoor Mapping and Workplace Locations data from one instance to another
        -   Ability to share URLs to a specific space on the map from the Location Directory
        -   Support of Patterns on the map for color blind users in the Reservation Module only
    -   Fixed: The Synchronization Script of the Space Data from Indoor Mapping to Workplace Service Delivery has been fixed and improved
-   **Version 1.1.2 - August 2022**
    -   New: Wayfinding between two workplace locations as defined in workplace profiles of employees
    -   Fixed: Performance Improvements in Location Directory UI
-   **Version 1.0.2 - May 2022**
    -   ServiceNow Workplace Indoor Mapping provides indoor navigation for workplace teams as part of ServiceNow Workplace Service Delivery. Employees and end users can visualize in real-time workplace interiors, room reservation states, along with other indoor and outdoor details for a selected campus, building, and floor.
    -   Workplace administrators can design, edit, and manage inbuilt indoor maps for interactive locations and wayfinding. Install all the Workplace Service Delivery applications at once by downloading the ServiceNow Workplace Service Delivery Suite.

**Parent Topic:**[ServiceNow Store - Workplace Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-wsd-highlight.md)

