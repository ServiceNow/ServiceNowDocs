---
title: ITOM Content Service release notes
description: Version history for the ITOM Content Service application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-content-service.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - ITOM Visibility release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# ITOM Content Service release notes

Version history for the ITOM Content Service application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.8.0 - June 2026**

    New: Control access through predefined query access controls for all ITOM Content Service tables.

-   **Version 1.7.1 - March 2026**

    Fixed: Smart Content Candidates Sync now correctly validates and syncs product and publisher names that contain forward slashes or parentheses.

-   **Version 1.6.3 - December 2025**

    New: Opt in to share the Service Info data of mapped candidates and gain access to the Application Service Candidate \[application\_service\_candidate\] table.

-   **Version 1.5.2 - September 2025**
    -   Changed: Enhanced service info provided to Application Service Candidates in Service Mapping to provide more accurate and useful information.
    -   Fixed: Minor fixes for SAM integration and probe compatibility.
-   **Version 1.5.1 - May 2025**
    -   Fixed:
        -   Added a dependency for File-Based Discovery \(FBD\) to fix the error "Rule entry under cmdb\_ci\_hardware identifier using non-existent tables is ignored during identification" when FBD wasn't installed \(PRB1827349\).
        -   On the Process Classifications form, the "Sync candidates" and the "Sync From CDS" buttons are now displayed only in the Global scope to fix the issue that records get the scope of the current scope during syncing \(PRB1808614\).
        -   Added a delete mechanism for incorrect SNMP OID tagging to clean up unnecessary SNMP OIDs in the customer environment \(PRB1804969\).
-   **Version 1.4.2 - November 2024**
    -   New:
        -   ITOM Content Service using file-based Discovery populates the File Information \[cmdb\_file\_information\] table.
        -   ITOM Content Service records synced from the Continuance Delivery System \(CDS\) display smart\_content as the value in the Updated by field.
    -   Fixed:
        -   CDS better manages downloads across instances.
        -   Sync works even if a product contains special characters.
-   **Version 1.3.1 - August 2024**
    -   New: UT framework
    -   Fixed: SAM Integration improvements
    -   Removed: Smart Content Dashboard deprecation \(See the Content 360 documentation\)
-   **Version 1.2.10 - July 2024**

    Compatibility for the new ITOM Content Service Plugin.

-   **Version 1.2.8 - May 2024**
    -   New:
        -   An application and a Service Mapping visualization map are constructed to gain insights into its constituent components and their interactions
        -   For file-based discovery, the product and publisher information from the classifier is included in the unidentified file information
        -   A predefined list of set-up categories is added to the opt-in activation, to streamline the process
            -   Basic - activate several categories
            -   Advanced - activate more categories
            -   Expert - give the user the option to choose what to activate
        -   A Dynamic Content table is added.
    -   Fixed: The integration of Smart Content with Software Asset Management- the issue of duplicate "FileDetails" records in Trigger Probes is resolved byclassifier fixes.
-   **Version 1.2.4 - February 2024**

    ITOM Content Service Opt-in to share the processes fingerprints and SNMP System OIDs data to the Continuance Delivery System \(CDS\) infrastructure. Shared anonymous datasets from all discovery customers will be used by AI Librarians to create application fingerprints \(process classifiers\) and the curated SNMP OIDs, and application fingerprint data will be delivered back to the customer instances. Content Service deliver new process classifiers / SNMP OIDs every week.


