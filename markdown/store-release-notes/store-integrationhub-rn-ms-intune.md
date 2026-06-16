---
title: Microsoft Intune spoke release notes
description: Version history for the Integration Hub Microsoft Intune spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-ms-intune.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Intune spoke release notes

Version history for the Integration Hub Microsoft Intune spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - June 2026**

    Non Glide Cobalt Raven ACLs added.

-   **Version 1.4.1 - March 2026**

    Fixed: Missing OOB 'report\_view' ACLs for multiple tables.

-   **Version 1.4.0 - February 2026**

    New: Sync Managed device action added

-   **Version 1.3.2 - January 2026**

    New: Added new spoke actions and subflows for CSD Agents.

-   **Version 1.2.0 - November 2025**

    New: Support revocation of installed softwares in SAM table.

-   **Version 1.1.9 - August 2025**

    Fixed: Fix script to drop the index from deployment table. Log error and continue flow if 'Lookup Group record' fails.

-   **Version 1.1.8 - January 2025**

    Fixed: Bug related to Invalid User ID.

-   **Version 1.1.7 - July 2024**
    -   Fixed:
        -   Deploy Application subflow - Intune Spoke - Harmonize the output of prepare software data with input of look up user ID for customer scenario.
        -   Unique key constraint violation in the Microsoft Intune deployment table error.
-   **Version 1.1.6 - May 2024**

    Security fix.

-   **Version 1.1.5 - December 2023**
    -   Fixed:
        -   Fixed length for ID Column in sn\_ms\_intune\_spoke\_deployment Table
        -   Unique Identifier in Client Software Distribution 2.0 Flows
-   **Version 1.1.4 - September 2023**

    Fixed: In subflow "Deploy Application" &amp; "Revoke Application", the mapping of 'username' in 'Look up User ID' action to be changed from 'Display Name' input to 'User Login ID'.

-   **Version 1.1.3 - September 2023**

    Fixed: The license requirements.

-   **Version 1.1.2 - April 2023**

    Patch release of Jamf Spoke for Integration Hub. This version includes deduplication changes.

-   **Version 1.1.0 - September 2022**

    Changed: Minor release for Microsoft Intune Spoke. This version improves action Look up Managed Devices and adds new action Look up Application Assignments.

-   **Version 1.0.0 - October 2020**

    Provides actions to automate retrieving application details and managing devices in Microsoft Intune.


