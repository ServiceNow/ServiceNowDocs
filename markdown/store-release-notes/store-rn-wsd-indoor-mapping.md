---
title: Indoor Mapping release notes
description: Version history for the Indoor Mapping application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-indoor-mapping.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 9
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Indoor Mapping release notes

Version history for the Indoor Mapping application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.16.8 - June 2026**
    -   Fixed:
        -   Fixed an issue affecting map rendering in iOS.
        -   Fixed issues affecting CAD configuration.
        -   Fixed an issue affecting AI-assisted map updates when file prefixes are updated.
        -   Fixed an issue affecting AI-assisted map import status tracking.
-   **Version 1.16.6 - May 2026**

    Fixed: Applied security fixes.

-   **Version 1.16.5 - April 2026**
    -   Fixed:
        -   Fixed an issue where deleting a building could create duplicate empty campuses.
        -   Fixed an issue where the CAD editor configuration save could remain stuck in a loading state indefinitely.
-   **Version 1.16.0 - March 2026**
    -   Fixed:
        -   Resolved an issue where “Accessible” and “Default” labels in Map Studio were hardcoded and not translatable
        -   Fixed an issue where “Center on campus” failed when the target zoom level exceeded the building entry zoom level
        -   Resolved an issue causing an authentication popup to appear when opening a floor map from the Building Overview in Workplace Central for the first time
        -   Corrected incorrect scale and rotation applied to floor plans during bulk import
-   **Version 1.15.0 - December 2025**
    -   New:
        -   Introduced bulk location hierarchy creation.
        -   Added the ability to bulk-validate views.
        -   Enhanced CAD bulk import to support automatic georeferencing and file configuration.
        -   Added a property to remove the outdoor map background when entering a building for auto-georeferenced files.
    -   Fixed: Allowed the legend to span multiple pages when printing.
-   **Version 1.14.4 - September 2025**

    New: New AI Agent to identify sources automatically and suggest floors when bulk importing floor plans to reduce manual intervention.

-   **Version 1.14.1 - August 2025**
    -   New:
        -   Introduced ability to bulk upload and process AutoCAD and PNG files to automate file updates.
        -   Added new ACL for read-only access to Indoor Mapping tables.
    -   Fixed: Translation issues.
-   **Version 1.13.2 - May 2025**
    -   New
        -   New google places API support.
    -   Changed
        -   Removed former google places API key that was no longer active and replaced by new test one.
    -   Fixed
        -   none.
    -   Removed
        -   none.
-   **Version 1.12.0 - February 2025**
    -   New:
        -   CAD file configuration now supports retrieving titles and place types from separate layers.
        -   Improved handling and display of CAD file configuration errors.
    -   Changed:
        -   Warning pills on the file configuration page are now clickable.
        -   Indoor Mapping now references the country table.
    -   Fixed: The georeference step now correctly renders maps for rescaled floor plans.
-   **Version 1.12.12 - April 2025**
    -   New
        -   New google places API support.
    -   Changed
        -   Removed former google places API key that was no longer active and replaced by new test one.
    -   Fixed
        -   none.
    -   Removed
        -   none.
-   **Version 1.12.0 - February 2025**
    -   New:
        -   A new page is now available to configure map printing, accessible from both Map-Based Administration and Location Directory Maps. The configuration options include:
            -   Map preview
            -   Portrait and landscape mode
            -   Page size selection
            -   Customizable page title
            -   Map legend display
            -   Location pin display
            -   Adjustable font size and icon size
            -   Option to add timestamp
            -   Ability to remove the outdoor map
            -   Prioritization of specific spaces for display
            -   Conversion of spaces into numbered labels with corresponding legend for dense floor plans
    -   Fixed:
        -   Fixed an issue where the Export to AutoCAD button erased all CAD changes.
        -   Floors now display correctly for Raster sources in View Editor.
        -   Map Admins can now delete a source even if the setup job fails.
        -   Increased the maximum zoom level to 24 to address collision issues.
        -   Map Studio no longer uses inactive Place types during file configuration.
        -   Georeference errors causing file failures.
-   **Version 1.11.11 - January 2025**

    Fixed issue preventing Campus creation and Floorplan georeference.

-   **Version 1.11.0 - November 2024**
    -   Fixed:
        -   Walls now display properly on Now Mobile App
        -   Snapshot now handles spaces that change to rooms
-   **Version 1.10.0 - August 2024**
    -   Fixed:
        -   Multi-select for places is now functional when selecting points
        -   CAD file unit is retained when migrating to the new AutoCAD processing tool
        -   AutoCAD editor spinner no longer loads indefinitely without displaying an error message
        -   Issue causing the close shape feature of the CAD editor to fail is resolved
        -   Apply button now works correctly when displaying the person who booked a space
-   **Version 1.9.1 - May 2024**
    -   New: CAD file processing and display performance improvements during import
    -   Fixed:
        -   Remove rule that overwrote bearing setting when inferior to 7
        -   Fixed never ending loading pages when file import fails
        -   Fixed "text" migration when using new autocad tool
-   **Version 1.8.1 - March 2024**

    Fixed ACL issues with the new CAD management tool.

-   **Version 1.8.0 - February 2024**
    -   New:
        -   \[Map Studio\] New Floor plan configuration page
            -   Improved map preview with styling.
            -   Summary pills for configuration validation.
            -   Warning alerts for unclosed polylines.
            -   Retrieve place types from AutoCAD text labels and block attributes.
            -   Manually define place types.
        -   \[Map Studio\] New CAD File Editing Page
            -   Advanced floor plan preview with AutoCAD style.
            -   Display and manage layers with isolation and hide options.
            -   Editing options: draw/delete lines and shapes, add/edit/delete text, move elements between layers, and edit block attributes.
        -   \[Map Studio\] Export functionality from CAD editing page to AutoCAD.
        -   \[Map Studio\] Multiselect option in the place edition section.
    -   Changed: \[Map Studio\] Configuration and file preview tabs replaced with new configuration and CAD editing pages.
-   **Version 1.7.2 - January 2024**

    Security fixes.

-   **Version 1.7.0 - November 2023**
    -   Fixed: System failure present since 1.5.0 due to the auto-compute boundary feature.
    -   New: Compute floor surface from CAD files.
-   **Version 1.6.0 - August 2023**
    -   Fixed: Upgrade to Indoor Mapping 1.7.0 to fix system failure related to auto-compute boundary feature.
    -   New:
        -   Improved campus page on Map Studio
        -   Ability to configure names and titles separately on CAD configuration page
        -   Ability to configure what elements can be filtered by users on the map
        -   New Indoor Mapping to CMN location sync
-   **Version 1.5.0 - May 2023**
    -   Fixed: Upgrade to Indoor Mapping 1.7.0 to fix system failure related to auto-compute boundary feature.
    -   New:
        -   Automatic adjustment of building boundary.
        -   Autocad file size limit increased to 200MB for Map Studio import.
-   **Version 1.4.0 - March 2023**
    -   New:
        -   Ability to ignore certain layers or hidden layers from being processed by Map Studio
        -   Ability to simplify map geometries to improve performance
-   **Version 1.3.2 - February 2023**
    -   New:
        -   Copying direction graphs from one floor to multiple floors
        -   Highlighting direction modes
        -   Automatic Campus Boundary computation
        -   Improving CAD previews
        -   Improving AD import errors
        -   Automatically extracting CAD values
        -   Migration of Indoor Mapping data from one instance to another
        -   New "Map editor limited" role available
    -   Fixed: Role related issues
-   **Version 1.2.1 - November 2022**
    -   New:
        -   Ability to copy a direction graph from one floor to another.
        -   View how place entrances and connectors connect to the graph to avoid potential wayfinding errors.
        -   Keyboard Shortcuts to speed up actions in Map Studio.
        -   Map Preview page available to fully test the map before pushing it live to Workplace Service Delivery.
        -   View edition improvements by offering the ability to copy content from one view to another.
        -   Automatic CAD file configuration based on previously imported files.
        -   Ability to automatically close polylines.
    -   Fixed:
        -   Earlier, floor plan import failures were not properly handled by Map Studio, users were still directed to the configuration page without being able to do anything and with no error message. This has been fixed.
-   **Version 1.1.0 - August 2022**
    -   Fixed:
        -   Fixed error handling of map loading issues
        -   Allow geojson source file import in Map Studio
        -   Fixes in Map Studio
            -   Issue with 'Upload new File'
            -   \[i18n Store App Onboarding\] Indoor Mapping: Floorplan sources string is not being externalized for translation
            -   While testing the Indoor Mapping application, the user found inappropriate text on the map that replaced the name of a location
            -   Map is not not adjusted by clicking on pin/building icon
            -   Map Studio - Floor selector under zoom buttons
            -   Default camera lat/lon editor requires tooltip
            -   Floor default zoom is not properly computed by API
            -   Floor's Short title accepts special characters also.
            -   View Editor\_Tool tip text displays incorrectly when mouse hover on it.
            -   View editor\_Marker Icon list is not sorted under Place type Properties
            -   'Upload File' pop-up doesn't appear when user first cancels the selection of one AutoCAD file and then tries to select the same AutoCAD file again.
            -   Updated building and campus names are not displayed on the right side of the page
            -   In View Editor - Add or remove content page, list of selected elements didn't persist on click of 'previous' button.
            -   Editing a route for the second time does not work
            -   Direction Route Edit: "is active" option is not working
            -   Place just created shows: created 3 hours ago
            -   Compute directions when Start and End points in different buildings other than Floor 1
            -   Click on connector is returning a place click on JS SDK
            -   In the building overview the building A icons appear multiple times across the screen when zoomed in
            -   Dates on Safari are displayed as NaN years in the Studio
            -   Zooming on to one of the building in a campus is displaying 2 same building icons and names
            -   Direction steps issues
-   **Version 1.0.14 - June 2022**
    -   Changed:
        -   The Indoor Mapping Studio landing page has been updated.
        -   You can now create a polygon place with only 1 point in Studio.
        -   The 'Outdoor style' is now required in the View type.
        -   The Studio will now open as iFrame within the Polaris page and not as a new page.
        -   You can now create buildings without an address in Studio.
        -   Indoor Mapping Studio:
            -   Create flows - You can upload the floor list configuration screen.
            -   Style editor - You can add bulk content.
            -   Manage flow - Changes to Building page.
            -   Building Map VX is updated.
    -   Fixed:
        -   The direction modes are now saved when creating a connector in Studio.
        -   You can now change the floor name from the studio.
        -   In the Map Studio, the "manage floors" menu on the Manage campus screen now works without any issues.
        -   The duplicate floors in from/to fields in the Direction response are now removed.
        -   The error messages that are displayed when you cannot connect to Map Import Service are improved.
        -   The Domain column is now by default added to the indoor mapping lists/forms even if the domain plugin is not installed.
        -   The Studio sys\_ui\_page is now updated on updating the plugin to the latest version
        -   You can now upload an AutoCAD file of size more than 10MB from Studio UI.
        -   The Studio\_Localisation\_English Static labels are now translated into French \[using pseudo plugin\].
        -   The Portal\_ Localisation\_English Static labels are now translated into French \[using pseudo plugin\]
        -   You can now select a polygon layer \(do not use polygon\) when importing a CAD file.
-   **Version 1.0.0 - May 2022**
    -   ServiceNow Indoor Mapping provides inbuilt indoor maps for indoor navigation. It provides interactive location directories and wayfinding capabilities. End users can visualize in real-time workplace interiors, room reservation states, along with other indoor and outdoor details for a selected campus, building, and floor.
    -   Indoor maps can be created by converting existing architectural or engineering plans, or they can be drawn by hand using an indoor mapping design studio interface. You can start by identifying basic details such as walls, doorways, elevators, and stairwells. Add additional information like places and place types, locations, and points of interest.
    -   Indoor Mapping uses AutoCAD or raster image files \(PNG\) floor plan source to automate the map building process. Define the area of your building and enter the basic information. Drag or import the floor plan source file that represents the structure of your building.
    -   Once existing floor plans are imported, map studio provides all the necessary tools and objects for adding map data and customizing the maps. This includes creating points-of-interest, directions \(routes\), connectors \(elevators, escalators, ramps, or stairs\), accessibility routes, and so on. Changes and updates done in Indoor Mapping are synchronized in real-time with the Workplace Service Delivery application.

