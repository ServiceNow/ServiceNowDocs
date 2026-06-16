---
title: ArcSight ESM Event Ingestion for Security Operations release notes
description: Version history for the ArcSight ESM Event Ingestion integration for Security Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-arcsight-esm-event-ingestion.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# ArcSight ESM Event Ingestion for Security Operations release notes

Version history for the ArcSight ESM Event Ingestion integration for Security Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.5.1 - June 2026**

    Fixed: Access issues for Security Analyst while querying tables

-   **Version 10.5.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 10.4.19 - August 2025**
    -   Fixed:
        -   Multiple configuration items not mapping to SIR.
        -   sys\_scope issue in Arcsight ESM.
-   **Version 10.4.17 - April 2025**

    Fixed: Issue related to the configuration item mapping.

-   **Version 10.4.15 - November 2024**

    Changed: Migrated default workflows to flows using Flow Designer.

-   **Version 10.4.13 - May 2024**

    The dependency on the new UI is removed.

-   **Version 10.4.11 - March 2024**

    Fixed: Time out issues for integrations in case of longer waiting time is expected for midserver.

-   **Version 10.4.10 - December 2023**

    Fixed: Misconfiguration of table/field ACLs within the com.snc.secops.arcsight plugin. This is now fixed.

-   **Version 10.4.9 - November 2023**

    Fixed: The Restricted Caller Access \(RCA\) record causing duplicate entries when the source was trying to access the target source has been deleted. The platform was reading RCA to check whether cross-scope access is allowed for the target resource, and that's when it noticed a duplicate entry and displayed an error.

-   **Version 10.4.8 - May 2023**
    -   Fixed:
        -   One-Time Retrieval was not working on the scheduling page in the profile when you change the date format to DD-MM-YYYY.
        -   Arcsight event ingestion is truncating values when the ID fields are 19 or more digits.
-   **Version 10.4.6 - September 2022**
    -   Fixed:
        -   Improve the logging for ArcSight ESM Event Ingestion.
        -   POL\_ON tabs were greying out on clicking the continue button.
-   **Version 10.4.5 - May 2022**
    -   Fixed:
        -   When there is a Business Rule on Observable/CI, and task M2M records which update the SIR fields automatically. This occurs since SIR was not persisted at the creation time using SIEM, and the SIR fields are not getting updated. Now SIR would persist first in DB, and then the M2M records are created.
        -   Records were not getting parsed if only one event was generated in ArcSight.
-   **Version 10.4.4 - December 2021**

    Fixed: UI changes.

-   **Version 10.4.2 - August 2020**

    Fixed: Minor bug fixes.

-   **Version 10.4.1 - June 2020**

    New: Added support for ArcSight related lists and actions to be available in the Security Incident Response UI.

-   **Version 10.0.5 - March 2020**

    ArcSight ESM is a market-leading solution for collecting, correlating, and reporting on security event information. This integration with ArcSight ESM will be used automate ingestion of correlated events from ArcSight and improve the ability to automate creation of security incidents in the ServiceNow platform through dynamic mapping.


