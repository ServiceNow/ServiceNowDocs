---
title: LogRhythm integration release notes
description: Version history for the Security Operations LogRhythm integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-logrhythm.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# LogRhythm integration release notes

Version history for the Security Operations LogRhythm integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.2.3 - June 2026**

    Fixed: Access issues for Security Analyst while querying tables.

-   **Version 11.2.2 - May 2026**
    -   Fixed:
        -   SIRs are not created from SIEM ingestion due to "Secure Notes" access issue to the Crypto module since the Yokohama upgrade was fixed.
        -   Access issues for Security Analyst on querying tables.
-   **Version 11.2.1 - December 2025**
    -   New:
        -   Upgraded all dictionary-level read-only fields to Strict Read-Only to improve security and prevent unauthorized changes. This ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.
        -   Replaced all occurrences of the admin role within the integration logic with the more restrictive sn\_si.admin role to ensure proper access control and adherence to least-privilege principles.
    -   Fixed:
        -   System property "Max Security Incident can be created in a day" not working.
        -   Schedule Script "LogRhythm Data Cleanup" not executing.
-   **Version 11.1.10 - April 2025**

    Fixed:

    -   CMDB\_CI mapping getting failed for "Configuration Item" field on Logrhythm.
    -   Configuring CI Under Mapping Screen SIR Not Getting Created.
-   **Version 11.1.9 - November 2024**

    Changed: Migrated default workflows to flows using Flow Designer.

-   **Version 11.1.8 - April 2024**

    Fixed: Misconfiguration of table/field ACLs is corrected.

-   **Version 11.1.5 - November 2023**

    Changed: Minor UI updates to render the profile mapping page.

-   **Version 11.1.4 - May 2023**

    Fixed: One-Time Retrieval was not working on the scheduling page in LogRhythm profile when we change the date format to DD-MM-YYYY, this is now fixed.

-   **Version 11.1.2 - September 2022**
    -   Fixed:
        -   Error while checking and unchecking the Since date checkbox.
        -   DeDup changes and Invalidate cache cleanup.
        -   If no data is generated within seven days of any rule, then a Warning/Error message should be thrown saying 'No data found' as no alarms were generated recently other than Heartbeat missed.
        -   Tooltip for Pull alarm button says 'This gets sample offense data from IBM Qradar server,' which needs to change to 'This gets sample alarms from Logrhythm.'
        -   Improve the logging for LogRhythm Event Ingestion.
-   **Version 11.1.1 - May 2022**
    -   New: Migration of APIs from REST to SOAP.
    -   Changed:
        -   Updated the integration tile and introduced alarm By ID API in Profile and Scheduled Job.
        -   Removal of alarm rule selection from profile set up.
        -   An additional options section has been introduced in the profile.
-   **Version 11.0.9 - November 2021**

    Fixed: Added additional password related policies

-   **Version 11.0.8 - August 2021**

    Fixed: Resolved an issue with the mapping of alarm fields to SIR reference fields, while creating security incidents from alarms.

-   **Version 11.0.7 - February 2021**

    Fixed: The LogRhythm date fields \[YY-MM-DDTHH:MM:SS\] now map correctly in the ServiceNow AI Platform using the Glide DateTime format.

-   **Version 11.0.6 - December 2020**
    -   New:
        -   Added Related List on the Security Incident Form containing all raw base events related to the LogRhythm Alarm.
        -   Mapping section of the Alarm Profile includes a search function to easily find Alarm Fields by name.
        -   Added a navigation link to the LogRhythm Drilldown Event module to view the list of all raw base events.
        -   Support for multi-valued field mappings of Configuration Item and Observable when multiple raw base events related to the LogRhythm Alarm contain different values for these mapped fields.
    -   Fixed: Mid server routing is maintained based on configured selection\(s\) even in failure scenarios
-   **Version 5.0.4 - July 2019**
    -   New: Recertified for New York
    -   Fixed: Improved exception handling when LogRhythm API returns error code
-   **Version 5.0.3 - November 2018**
    -   Flexibility to create multiple alarm profiles such as phishing and malware
    -   Drag-and-drop mapping of LogRhythm alarm field values to associated SIR security incident fields
    -   A preview of the SIR security incident layout based on sample alarms to validate configuration set-up
    -   Ingest historical alarms as well as ongoing, future alarms on configurable intervals
    -   Automated alarm close out upon incident closure, which includes a SIR security incident ID and URL for easy linking

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

