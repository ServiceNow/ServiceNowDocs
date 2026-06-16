---
title: Workplace Service Delivery Integration with Mappedin release notes
description: Version history for the Workplace Service Delivery Integration with Mappedin on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-integration-with-mappedin.html
release: store
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Service Delivery Integration with Mappedin release notes

Version history for the Workplace Service Delivery Integration with Mappedin on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.11.0 - August 2024**

    Minor bug fixes.

-   **Version 1.10.12 - May 2024**

    No significant updates.

-   **Version 1.10.9 - February 2024**

    No significant updates.

-   **Version 1.10.7 - November 2023**

    Fix related to security.

-   **Version 1.10.4 - May 2023**

    Fixes.

-   **Version 1.10.1 - February 2023**

    Changed: Default email templates are updated to match the next experience content and style guidelines. The new templates are installed beside the old ones in cases the old ones already exist on the instance.

-   **Version 1.9.2 - November 2022**
    -   Fixed
        -   Earlier, the capacity was set to 0 when importing spaces from Mappedin. This has been fixed now.
        -   Earlier, the source of a floor was not always set equal to the value of the related building when importing spaces. This has been fixed now.
-   **Version 1.9.1 - August 2022**

    Fixed: Few fixes.

-   **Version 1.8.2 - May 2022**

    FIxed: Minor UI issues.

-   **Version 1.7.1 - December 2021**
    -   The release notes for the related plugins can be found in the respective plugins.
-   **Version 1.6.1 - October 2021**
    -   New: Additional support has been added to support all the 22 languages that are currently available across the ServiceNow AI Platform.
    -   Fixed: Few fixes have been made on the Floor map legends translations.
-   **Version 1.5.1 - September 2021**
    -   Fixed: Bug fixes related to security and map legend accessibility
-   **Version 1.4.2 - June 2021**
    -   Fixed: Minor fixes.
-   **Version 1.3.1 - March 2021**
    -   New:
        -   A catalog item, Location directory, is added in the Workplace service portal. The location directory provides an interactive floor map. You can view your buildings, floors, and spaces on the map. You can select a space on the map and request workplace help directly.
        -   You can also get directions to another space on the map.
    -   Changed:
        -   In the Workplace Service Delivery - Suite, from Workplace Safety Management\[workplace-safety-management\] version 2.5.3, the Space type \(space\_type\) choice field is depreciated. After the upgrade, Space types are configured in the Space Type Configuration menu option. The Space type \(space\_type\) field is migrated as Space type \(location\_type\) field in the Space table \[sn\_wsd\_core\_space\]. Customers having customization on the depreciated Space type \(space\_type\) field are advised to manually migrate their flow to use the new Space type \(location\_type\) field. A new fix script, 'Populate Location Type from Space Type' is introduced to execute the scheduled job - 'Populate location\_type from space\_type' on the Space table \[sn\_wsd\_core\_space\] to migrate the depreciated Space type \(space\_type\) field value to the new Space type \(location\_type\) field.
-   **Version 1.2.1 - January 2021**
    -   New:
        -   When Reservation Management is installed:
            -   Reservation admins can enable Mappedin floor maps on the Make a reservation portal page. They can do this by turning on the Show map view checkbox for any reservable module that should include maps.
            -   On the Make a reservation portal page, workplace users can use Mappedin floor plans \(in addition to the card and schedule views\) to make reservations.
-   **Version 1.1.2 - December 2020**
    -   New:
        -   When Reservation Management is installed:
            -   Reservation admins can enable Mappedin floor maps on the Make a reservation portal page. They can do this by turning on the Show map view checkbox for any reservable module that should include maps.
            -   On the Make a reservation portal page, workplace users can use Mappedin floor plans \(in addition to the card and schedule views\) to make reservations.
-   **Version 1.0.2 - November 2020**
    -   Workplace Service Delivery Integration with Mappedin provides an interactive digital mapping solution, enabled by Workplace Space Mapping. The integration allows workplace teams to leverage mapping as part of ServiceNow Workplace Service Delivery. Easily convert and build unique indoor mapping experiences utilizing a robust map editor suite to ensure floor plans remain up to date.
        -   New: Feature parity with Workplace Safety Management mapping solution

## Notice regarding use by organizations

All decisions in connection with the implementation of this application are at the sole decision of the Organization utilizing this application. Organizations agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations' specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to government employees in their individual capacities. Use of the application does not modify any existing, or future entitlements or payment obligations for ServiceNow software or applications otherwise purchased by the government agency. ServiceNow shall not be responsible for any implementation or configuration costs associated with use of the application unless separately purchased. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

