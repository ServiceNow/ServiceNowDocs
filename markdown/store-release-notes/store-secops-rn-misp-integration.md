---
title: MISP integration for Security Operations release notes
description: Version history for the MISP integration for Security Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-misp-integration.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# MISP integration for Security Operations release notes

Version history for the MISP integration for Security Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.4.6 - June 2026**

    Fixed: Cobalt Raven Non-Glide Query ACLs Directive.

-   **Version 1.4.5 - April 2026**

    Fixed: Optimised queries to reduce database operations and improve performance.

-   **Version 1.4.4 - February 2026**

    Fixed: MISP Events with NULL Attributes or Tags now process correctly from queue tables. Previously, these events failed during automatic creation, causing the queue status to remain stuck at "running" instead of progressing to the next status.

-   **Version 1.4.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes. This update ensures the server consistently enforces read-only behaviour across all UIs, scripts, and integrations.

-   **Version 1.3.11 - August 2025**

    New: Introduced an improvement to Security Incident Response where MITRE ATT&amp;CK Techniques from associated MISP Events are automatically rolled up and reflected in the corresponding Security Incident.

-   **Version 1.2.1 - June 2025**
    -   Fixed:
        -   Sightings Search Flow triggering an error.
        -   REST Action error when called from Script Action: Refresh MISP Galaxies Event Handler.
-   **Version 1.2.0 - November 2024**

    Changed: Migration of Workflows to Flow Designer for MISP integration.

-   **Version 1.1.2 - August 2024**
    -   New:
        -   Migrated workflows to flow designer for MISP enrichment capabilities.
        -   Introduced a new field called Security tags for the automatic MISP profile configuration, and also verifies those observables with the security tags which are not attached to the automatic event created using the profile.
        -   Introduced local and global tags in Automatic MISP profile configuration, which will eventually add the selected tags to the newly created automatic MISP event.
-   **Version 1.1.1 - May 2024**
    -   Fixed:
        -   When the observable has symbol '!' in the starting, MISP enrichment flow was considering it as a filter condition and was not giving proper results. This is now fixed.
        -   When sighting search was triggered for observable with same name but with different type in MISP then the flow was not successful. This is now fixed.
-   **Version 1.0.12 - January 2024**

    Fixed: MISP integration validation was failing when the MISP instance was configured behind SSO. This is now fixed.

-   **Version 1.0.11 - December 2023**

    Changed: Added supporting changes to render MISP forms on SIR workspace.

-   **Version - May 2023**

    Fixed: Implement table cleanup rules for MISP.

-   **Version 1.0.7 - April 2023**

    Changed: Updated to support this integration on the Security Incident Response workspace.

-   **Version 1.0.5 - February 2023**

    New: Updated to support Security Incident Response workspace.

-   **Version 1.0.3 - November 2022**
    -   Fixed:
        -   For editing tags, MISP write role is given in addition to sn\_si read.
        -   POL\_ON\_MISP automatic profile UI.
        -   MITRE-ATT&amp;CK information was not shown for Associated Observables when MISP is installed on an instance.
-   **Version 1.0.1 - August 2021**

    New: MISP integration enables you to investigate security incidents by supporting capabilities like sightings search, observable enrichment, event search, along with the ability to create and update events in MISP.


