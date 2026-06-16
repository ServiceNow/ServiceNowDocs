---
title: CrowdStrike Falcon Insight Integration for Security Operations release notes
description: Version history for the CrowdStrike Falcon Insight Integration for Security Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-crowdstrike-falcon-insight.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# CrowdStrike Falcon Insight Integration for Security Operations release notes

Version history for the CrowdStrike Falcon Insight Integration for Security Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.5.3 - June 2026**

    Fixed: Access issues for Security Analyst while querying tables.

-   **Version 1.5.2 - March 2026**

    New: Added the block request capability - enabling analysts to block SHA256/MD5 hashes from Security incident.

-   **Version 1.4.1 - January 2026**

    Fixed: Fixed an issue where the Initialise Batch ID action returned no choice values for the Status field in the output.

-   **Version 1.4.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes.This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 1.3.1 - May 2025**

    Fixed: Various bugs have been addressed and resolved as part of this release.

-   **Version 1.3.0 - November 2024**

    Changed: Migrated Workflows to Flow Designer flows.

-   **Version 1.2.3 - November 2023**

    Fixed: When the customer upgrades to the latest capability framework version, previously only one profile gets copied, but now all the profiles will get copied.

-   **Version 1.2.1 - June 2023**

    Fixed: Upgrade issue post migration to capability framework.

-   **Version 1.1.10 - May 2023**

    Changed: Migrated to capability framework.

-   **Version 1.1.8 - February 2023**
    -   Changed: Crowdstrike device API upgrade.
    -   Fixed:
        -   Sighting search is not working and displays a 404 error from the API.
        -   Clean up of worknotes.
-   **Version 1.1.7 - November 2022**
    -   Changed: Utah Mandate: Update snc-app-parent version to 5.0.0.77
    -   Fixed:
        -   CrowdStrike's Get file retrieves the wrong file from the system.
        -   Improve the logging for CrowdStrike Falcon Insight.
-   **Version 1.1.6 - June 2022**
    -   Fixed:
        -   CrowdStrike Falcon Insight Sighting Search is not working in the latest platform versions.
        -   If both Agent Client Collector capabilities and CrowdStrike Falcon Insight capabilities are active, an incorrect window can open when clicking UI action.
-   **Version 1.1.3 - October 2021**
    -   New:
        -   Added new modules: Crowdstrike Approvals, Crowdstrike Notification Configuration, and Crowdstrike Default Setting
        -   New capabilities 'Get File' and 'RTR actions' are available
        -   Added support for Linux endpoints for CI submissions
        -   In the Crowdstrike Additional Actions module:
            -   Admin can create a new record for custom script with all fields editable
            -   Analyst can create a new record with some restricted access
    -   Fixed:
        -   Fixed OS determination while 'Get Logged on Users' is run against a MacOS
        -   Improved performance for CrowdStrike flows
-   **Version 1.0.2 - February 2021**
    -   New:
        -   Falcon Insight delivers continuous, comprehensive endpoint visibility that spans detection, response and forensics to ensure nothing is missed and potential breaches are stopped.
        -   CrowdStrike Falcon Insight Integration for Security Operations provides CI enrichment and host isolation capabilities.

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

