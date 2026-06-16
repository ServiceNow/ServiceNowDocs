---
title: DLP Incident Response integration with Microsoft release notes
description: Version history for the Security Operations DLP Incident Response integration with Microsoft on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-dlp-incident-response-integration-ms.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# DLP Incident Response integration with Microsoft release notes

Version history for the Security Operations DLP Incident Response integration with Microsoft on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.5.2 - June 2026**

    Fixed: The read\_only\_options attribute has been moved from IF folder–based plugin configuration to dictionary attributes on the table fields.

-   **Version 1.5.1 - May 2026**
    -   Fixed:
        -   Access issues for security analysts while querying tables.
        -   UI issue in the profile for displaying endpoint evidence file storage type.
        -   Field translation issue for keys which has undefined values.
-   **Version 1.5.0 - February 2026**
    -   New: Support internal storage of Match content in Microsoft Purview Integration.
    -   Fixed: Prevent permanent data loss by adding support to re-process errored contentURI records.
-   **Version 1.3.1 - January 2026**

    Fixed: Removed redundant ACLs from the Match Content field in the Detected Sensitive Info table.

-   **Version 1.2.0 - December 2025**

    New Upgraded dictionary-level read-only fields to Strict Read-Only to enhance security and prevent unauthorized changes. This update ensures the server consistently enforces read-only behavior across all UIs, scripts, and integrations.

-   **Version 1.1.21 - October 2025**

    Fixed:

    -   Release from quarantine feature not functioning when configured with a target state.
    -   Added support for Microsoft DLP integration with GCC, Commercial, DOD, and GCC-High environments.
    -   Resolved issue where Microsoft DLP integration runs containing empty data were not completing successfully.
    -   Improved handling of integration runs where all data in the contentURI is filtered out by profile filters, and implemented timeout handling for contentURI and 'List Available Content' REST calls.
-   **Version 1.1.10 - August 2025**

    Fixed: Release Email from Quarantine Failure for DLP Exchange Online.

-   **Version 1.1.2 - July 2025**
    -   Fixed:
        -   Microsoft DLP Quarantine Release Error Handling:
            -   Resolved an issue where attempting to Release Email from Quarantine for incidents that were already released would cause the DLP Microsoft integration to enter an error state. The system now properly detects already released emails and avoids redundant actions, preventing unnecessary errors in the quarantine flow.
        -   Enhanced Endpoint File Download via Custom Blob Storage:
            -   Updated the file download mechanism for endpoint artifacts from custom blob storage. Previously, requests were made using the user's IP address, which could lead to access issues depending on network rules. With this update, download requests are now routed through the ServiceNow instance IP, ensuring consistent access control and improving compatibility with restricted storage configurations.
        -   Microsoft DLP Ingestion Performance Improvements:
            -   Optimized the Microsoft DLP ingestion pipeline to address slow performance during peak usage periods. Enhancements include better concurrency handling, improved API response management, and resource allocation tuning to ensure faster and more reliable ingestion even under high-load conditions.
-   **Version 1.1.1 - June 2025**
    -   Fixed:
        -   Generation of unnecessary error logs on clicking the Sensitive Information tab in the Workspace.
        -   Bug where multiple Sensitive Information Types with the same name were incorrectly created under the Detective Sensitive tab when different conditions were met simultaneously.
        -   Limitation where the "Incident Response Option Rule" could not be modified for Out-of-the-Box \(OOTB\) configurations. Users can now adjust these rules as expected.
-   **Version 1.1.0 - May 2025**
    -   New:
        -   Provided support for ingesting DLP Endpoint alerts using Microsoft Purview.
        -   Added Purview's user ID field for End User Lookup Rules mapping.
-   **Version 1.0.13 - February 2025**
    -   New:
        -   Evidence File Preview with Download Option:
            -   Added a preview icon for evidence files in the DLP Workspace.
            -   Users can now preview evidence files and download them directly from the preview interface, simplifying evidence review and retrieval.
-   **Version 1.0.11 - January 2025**

    Fixed: During upgrades, scheduled import sets were ignored, causing the data source pool to remain occupied. This resulted in ingestion process failures.

-   **Version 1.0.10 - November 2024**
    -   New: The integration now supports Evidence File Storage in ServiceNow, which includes the implementation of Microsoft Evidence File external storage, enabling better management and accessibility of evidence files.
    -   Fixed:
        -   The Microsoft DLP Incident Profile M2M data mismatch issue, ensuring accurate data representation.
        -   The state was not updating correctly during the release from quarantine after a successful process.
        -   Match content now appears for incidents archival in Microsoft DLP.
-   **Version 1.0.9 - August 2024**
    -   New: Microsoft is now compatible with the DLP core migration changes such as incident status.
    -   Fixed: EnforcementMode field is now available within the incident.
-   **Version 1.0.8 - February 2024**
    -   New: Added correlation ID within the DLP incident table to map the integration ID to the DLP incidents.
    -   Fixed:
        -   The domain ID \(sys\_domain\) is set to undefined when the DLP incidents are created using the import set API.
        -   Enhanced the application logging when a Download File action fails on the DLP incident.
        -   The Release quarantine action on the DLP incident updates the state field when the internal PowerShell command fails.
        -   Integration run record was stuck during the execution for the incidents that are complete.
-   **Version 1.0.5 - December 2023**
    -   Fixed:
        -   Resolved the misleading 403 error in the DLPStorageUtilsAzure script include.
        -   Fixed the issue where the Since Date validation in the Profile was failing when the user was using a different date-time format.
        -   Addressed the issue of parsing of the event failing for Endpoint type of events with no SensitiveInfo.
        -   Fixed the missing BCC field in the Microsoft integration transform mappings.
-   **Version 1.0.4 - August 2023**
    -   New: You can now configure the polling interval in minutes instead of hours, for a DLP incident profile.
-   **Version 1.0.2 - June 2023**
    -   Fixed:
        -   The Match Content option is now visible in the import set attachments section.
        -   The Microsoft Integration Run was getting stuck in the running state when the API returned an error. This issue is now resolved.
-   **Version 1.0.1 - May 2023**
    -   New:
        -   Match content per sensitive info type in MSFT Integration and highlight exact matched text in the content.
        -   Encrypt match content stored in AWS/Azure and delete automatically.
        -   New configuration tile for Azure blob storage and Amazon S3.
    -   Fixed: Implement integration run for Microsoft DLP integration.
-   **Version 1.0.0 - February 2023**
    -   Provides a core framework to import Data Loss Prevention \(DLP\) incidents from multiple sources such as Microsoft purview apps \(Teams, Sharepoint, Email\), endpoint, network, email, and cloud and enables remediation workflow involving end users, managers, and DLP operations team with automated incident assignment and escalations.
    -   It allows DLP administrators to configure email templates for end-user coaching and communication and provides comprehensive reporting on incident trends.

**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

