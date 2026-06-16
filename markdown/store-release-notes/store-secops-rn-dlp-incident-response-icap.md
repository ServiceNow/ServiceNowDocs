---
title: DLP Incident Response integration with ICAP release notes
description: Version history for the DLP Incident Response integration with ICAP application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-dlp-incident-response-icap.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# DLP Incident Response integration with ICAP release notes

Version history for the DLP Incident Response integration with ICAP application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.3 - June 2026**

    Fixed: Addressed a field name mismatch issue during data ingestion.

-   **Version 1.1.2 - May 2026**
    -   Fixed:
        -   Resolved the issue of the DLP incident evidence files in
        -   Fixed a download failure occurring when file names contained spaces or special characters
        -   Addressed issues related to Cobalt Raven Non-Glide Query ACLs Directive.
        -   Fixed the issue of the Australia recertification failing due to invalid XML.
-   **Version 1.1.1 - January 2026**

    Fixed: Enhanced the Zscaler evidence download handling to work with both the legacy path-based and the new filename-based formats.

-   **Version 1.1.0 - December 2025**

    New: Upgraded all dictionary-level read-only fields to Strict Read-Only, to enhance security and prevent unauthorized changes. This update ensures the server consistently enforces read-only behavior across all UIs, scripts, and integrations.

-   **Version 1.0.20 - October 2025**

    Fixed issue to ensure execution occurs only after Q entry record updates, preventing creation of DLP incidents without proper metadata.

-   **Version 1.0.11 - June 2025**

    Fixed: Keyboard focus would exit the profile creation confirmation modal when navigating through the dialog options using the Tab key. Focus is now properly contained within the modal dialog.

-   **Version 1.0.10 - March 2025**

    Fixed download feature and ingestion for nested bucket structure, added support for folder structure within S3 buckets.

-   **Version 1.0.9 - February 2025**
    -   New:
        -   Evidence File Preview with Download Option:
            -   Added a preview icon for evidence files in the DLP Workspace. Users can now preview evidence files and download them directly from the preview interface, simplifying evidence review and retrieval.
    -   Fixed: Fixed an issue where integration runs were occasionally getting stuck in the running state for the ICAP integration, ensuring consistent and reliable integration behaviour.
-   **Version 1.0.7 - December 2024**

    Fixed: Access Control Lists \(ACLs\) applied to the Data Loss Prevention Incident Response\(DLP IR\) end-user workspace to regulate and manage user permissions and access.

-   **Version 1.0.4 - November 2024**

    An integration between ServiceNow's Data Loss Prevention Incident Response product \(DLP-IR\) and vendors who provide their DLP alerts information using the Internet Content Adaption Protocol \(ICAP\).


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

