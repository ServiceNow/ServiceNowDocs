---
title: Cornerstone spoke release notes
description: Version history for the Integration Hub Cornerstone spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-cornerstone.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Cornerstone spoke release notes

Version history for the Integration Hub Cornerstone spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.5.1 - May 2026**
    -   New: Added DEAPI-based datastreams for the Training catalog: training\_core, training\_local\_core, and training\_type\_core, replacing the deprecated vw\_rpt\_training Reporting API \(deprecated by Cornerstone in November 2025\).- Added new staging and persistent tables for Training Type data to support the normalized DEAPI structure.- Added type propagation logic that batches Training Type description updates to the target table after transform.- Added a new Integration Service for Training Types.
    -   Changed: Migrated Training catalog ingestion from the deprecated vw\_rpt\_training server-side JOIN to three normalized DEAPI endpoints \(training\_core, training\_local\_core, training\_type\_core\).- Updated the Training transform map with conditional field mapping using delta\_source\_core and delta\_source\_local boolean flags to prevent null overwrites on partial deltas.- Modified the existing Integration Service to handle Core + Local delta and full pulls under the new DEAPI model.- Improved upgrade handling to migrate existing customers from vw\_rpt\_training to the new datastreams without data loss.
    -   Fixed: Completed To-Dos are now pulled correctly via delta pulls.
    -   Removed: Deprecated the vw\_rpt\_training-based datastream in line with Cornerstone’s November 2025 API sunset.
-   **Version 1.4.2 - December 2025**

    Performance improvements.

-   **Version 1.3.2 - August 2025**
    -   Problem: The Cornerstone Spoke OOB Data Stream action Global Search failed when the payload contained only People data, due to missing checks for optional Training and Certification fields, resulting in a runtime error.
        -   New: Added conditional checks in the parser script to safely handle optional People, Training, and Certification data in the response payload.
        -   Changed: Updated the Global Search parser logic to dynamically assign values only when corresponding data is present.
        -   Fixed: Resolved the runtime error by ensuring the script no longer attempts to access undefined properties in the data stream.
        -   Removed: Eliminated hardcoded assumptions about the presence of Training and Certification fields in the payload.
-   **Version 1.3.1 - September 2024**

    Fixed: Removed unnecessary logging at script includes level to conform with coding best practices.

-   **Version 1.3.0 - December 2023**

    Added Auth Template + doc upgrade.

-   **Version 1.2.4 - September 2023**
    -   Fixed:
        -   JSON Injection in multiple Flow actions
        -   'licensable' field set to be true in plugin.xml
-   **Version 1.2.3 - September 2022**

    Fixed: Patch version of Cornerstone Spoke for Integration Hub. This version includes a fix to improve the installation performance of the spoke.

-   **Version 1.2.1 - May 2021**

    The minor release of the Cornerstone spoke for IntegrationHub. This version includes the addition of new actions: Create Assignment and Look up Assignment details.

-   **Version 1.1.1 - February 2021**

    Cornerstone 1.1.1 is a patch release with a couple of fixes on top of its previous version.

-   **Version 1.0.2 - August 2020**

    New: This version includes a new action to get certifications from reporting.

-   **Version 1.0.1 - June 2020**
    -   The Cornerstone spoke provides a list of actions that wraps around the Foundational and Reporting REST APIs. It provides the foundation to:
        -   Retrieve to-dos, assigned trainings, suggested trainings, certifications, and transcripts.
        -   Search on catalog, people, training, and certification.

**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

