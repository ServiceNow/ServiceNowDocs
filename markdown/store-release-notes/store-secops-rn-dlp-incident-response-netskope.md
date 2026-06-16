---
title: DLP Incident Response integration with Netskope release notes
description: Version history for the DLP Incident Response integration with Netskope on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-dlp-incident-response-netskope.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# DLP Incident Response integration with Netskope release notes

Version history for the DLP Incident Response integration with Netskope on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.2.2 - June 2026**

    Fixed: Access issues for analysts while querying tables.

-   **Version 1.2.1 - January 2026**

    Fixed: Fixed accessing match content.

-   **Version 1.1.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes. This update ensures the server consistently enforces read-only behavior across all UIs, scripts, and integrations.

-   **Version 1.0.30 - August 2025**

    Fixed: Resolved an intermittent issue during DLP incident ingestion from NetSkope, where incidents were being created with empty values for Integration Source and Domain fields.

-   **Version 1.0.18 - July 2025**
    -   Fixed:
        -   Netskope DLP Status Mapping Overwrite:
            -   Resolved an issue where updates made by customers to the state of a DLP record in the sn\_dlir\_incident table were being automatically overwritten by the system user. With this fix, the system will no longer override the state field if it has been manually updated by the customer, ensuring customer changes are preserved as expected.
-   **Version 1.0.17 - May 2025**
    -   Fixed:
        -   Updated Netskope's acting\_user field for End User Lookup mapping.
        -   Ingestion of Netskope DLP Incidents from when status mapping enabled.
-   **Version 1.0.16 - February 2025**
    -   New:
        -   Evidence File Preview with Download Option:
            -   Added a preview icon for evidence files in the DLP Workspace.
            -   Users can now preview evidence files and download them directly from the preview interface, simplifying evidence review and retrieval.
-   **Version 1.0.14 - December 2024**

    Fixed: Access Control Lists \(ACLs\) applied to the Data Loss Prevention Incident Response\(DLP IR\) end-user workspace to regulate and manage user permissions and access.

-   **Version 1.0.12 - August 2024**
    -   New:
        -   Added support for ingesting DLP incidents.
        -   Deprecated support for alerts ingestion.
        -   View the forensic details \(violating content\) of the DLP Incidents in both DLP IR Analyst workspace and DLP End user workspace.
        -   Downloading evidence file directly from Netskope on demand.
        -   Map the DLP incidents status between Netskope Object Status and ServiceNow incident status.
-   **Version 1.0.4 - February 2024**
    -   New:
        -   Added correlation ID mapping for DLP incidents in the transform map.
        -   Added support for the DLP incidents archival.
-   **Version 1.0.3 - June 2023**

    Fixed: The existing fields in Netskope are not mapped to ServiceNow, this issue is now fixed.

-   **Version 1.0.0 - May 2022**
    -   New:
        -   Import DLP incidents from Netskope to provide an incident response workflow for customers
        -   Support incidents created by data-at-rest scan from Netskope: both near real-time as well as on-demand scan
        -   Provides the ability to perform actions from within DLP end-user portal for end-users

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

