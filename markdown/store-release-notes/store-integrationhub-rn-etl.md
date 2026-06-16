---
title: IntegrationHub ETL release notes
description: Version history for the ServiceNow AI Platform capabilities IntegrationHub ETL application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-etl.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# IntegrationHub ETL release notes

Version history for the ServiceNow AI Platform capabilities IntegrationHub ETL application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.4.0 - June 2026**

    New: Integration Hub ETL is now WCAG2.2 and WCAG2.2AA compliant. Improvements include removal of extra spaces between menu items, addition of required children to ARIA roles, fixes for accessibility warnings, and removal of unnecessary scroll bars. Integration Hub ETL now supports reflow, allowing content to be zoomed up to 400% in a browser without loss of content or functionality. Page layouts automatically transform into a vertical, stacked view at 400% zoom. This update benefits users with low vision and those working across varied devices and environments.

-   **Version 3.3.6 - December 2025**

    Numerous bug fixes.

-   **Version 3.3.2 - May 2025**
    -   Fixed:
        -   Fixes related to conditional classes and their mappings \(PRB1849679, PRB1843627\)
        -   Security fixes
-   **Version 3.3.1 - February 2025**
    -   Fixed:
        -   Performance issues related to loading of "Specify Basic Details" screen when there are a large import sets.
        -   Security fixes
-   **Version 3.2.5 - October 2024**

    Fixed: Added the missing platform plugin as a dependency. No new bug fixes.

-   **Version 3.2.4 - August 2024**

    Issue fixed where renaming an entity and creating a new entity with the previous name can cause data to be incorrectly compressed.

-   **Version 3.2.3 - May 2024**
    -   Fixed the path used to access nested objects in script editor.
    -   Fixed the display of preview size shown in the wizard.
    -   Addressed a security issue.
    -   A few additional minor fixes.
-   **Version 3.2.0 - August 2023**
    -   New
        -   Added the ability to override the sn\_int\_studio.preview.size property from within the IntegrationHub ETL user interface, per ETL transform.
        -   Added ability to override default behavior around loading the schema for performance reasons.
        -   Added the ability to view the ETL mappings without having an import set available to load data.
    -   Changed
        -   Opening IntegrationHub ETL will now default to group by the CMDB Application column value
-   **Version 3.1.0 - February 2023**
    -   New:
        -   IH ETL now has support for non-CMDB tables. Use IH ETL to create IRE payload and insert data to not only CMDB tables but also to non-CMDB tables such has Location and User. Refer to IRE documentation on non-CMDB tables for more detail on IRE support for non-CMDB tables.
        -   IH ETL also added ability to create custom labels on classes as well as various changes around conditional classes and RTE/Data Source schema changes.
    -   Fixed: Includes various fixes around UI, Dark Theme and Schema change handling
-   **Version 2.2.1 - December 2021**
    -   Fixed:
        -   Updating target class retains the mappings and relationships.
        -   Details about affected mappings are now shown when users change a target class from a CMDB class to another CMDB class, or from a non-CMDB class to another non-CMDB class.
-   **Version 2.2.0 - November 2021**

    New: Error logging change to improve the overall debugging experience.

-   **Version 2.1.1 - August 2021**

    Fixed: Miscellaneous fixes. When you map a non-CMDB class, it is initially deactivated and the Activate/Deactivate Mapping toggle switch is disabled until you add an associated class that is active.

-   **Version 2.1.0 - June 2021**

    New: Ability to Activate/Deactivate mappings to ignore a class during the integration run, while preserving all of its mapping configuration.

-   **Version 2.0.1 - March 2021**

    Miscellaneous fixes.

-   **Version 2.0.0 - February 2021**

    New: Support for Nested JSON payloads from the data source. Users are no longer required to flatten data in the data source before processing in IntegrationHub ETL.

-   **Version 1.5.1 - December 2020**

    Fixed: Unable to search/select option while configuring 'Add Conditional Class' step in IntegrationHub ETL.

-   **Version 1.5.0 - November 2020**

    Fixed: A number of issues were fixed in this version.

-   **Version 1.4.2 - October 2020**

    New: Improved the experience when creating class relationships. It shows only valid relationships between two classes and shows the user suggested relationships at the top of the list.

-   **Version 1.3.1 - August 2020**
    -   New:
        -   Added the ability to preview the cmdb\_ci records in the Preview Sample Integration Results section
        -   Implemented class-mapping recommendation engine \(in limited preview\)
-   **Version 1.2.1 - June 2020**
    -   New:
        -   Ability to duplicate the configuration of an existing ETL transform map. This helps create a new version of the ETL transform map for testing or for further development.
        -   Ability to create a new transform for an attribute from a higher level menu dropdown, to improve user experience.
    -   Fixed: A number of usability related issues were addressed.

**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

